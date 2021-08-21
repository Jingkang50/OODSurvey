<a name="top"></a>
# 5. OOD Detection
- [5.1 Classfication-based Method](#5.1)
  - [5.1.0 Baseline](#5.1.0): MSP
  - [5.1.1 Confidence Calibration](#5.1.1)
    - [5.1.1.1 Post-hoc Calibration](#5.1.1.1): ODIN; Generalized-ODIN
    - [5.1.1.2 Bayesian Methods](#5.1.1.2): MC-Dropout; DeepEnsemble; 
    - [5.1.1.3 Other Confidence Enhancement Methods](#5.1.1.3)
  - [5.1.2 Outlier Explosure](#5.1.2)
  - [5.1.3 OOD Data Generation](#5.1.3)
  - [5.1.4 Label Space Redesign](#5.1.4)
  - [5.1.5 Big Pretrained Model](#5.1.5)
- [5.2 Density-based Method](#5.2)
  - [5.2.1 Embedding-based Method](#5.1.1)
  - [5.2.2 Flow-based Methods](#5.1.2)
  - [5.2.3 Energy-based Methods](#5.1.3)
- [5.3 Distance-based Method](#5.3)
- [5.4 Meta-Learning-based Method](#5.4)
- [5.5 Hybrid Methods and Others](#5.5)


<a name="5.1"></a>
## 5.1 Classfication-based Method
<a name="5.1.0"></a>
### 5.1.0 Baseline
**[ICLR-2017]**
[A baseline for detecting misclassified and out-of-distribution examples in neural networks](https://arxiv.org/abs/1610.02136).
<br>
**Authors:** Hendrycks, Dan and Gimpel, Kevin
<br>
**Institution:** University of California, Berkeley; Toyota Technological Institute at Chicago
> <details>
> <summary> The starting point of OOD detection, proposing a baseline simply uses softmax probabilities to detect OOD.</summary>
> <p style="text-align:left">
> Correctly classified examples tend to have greater maximum softmax probabilities than erroneously classified and out-of-distribution examples, allowing for their detection. However, due to the overconfidence characteristics of deep models, the baseline cannot be well performed. The overconfidence property comes from softmax always modeling sharp distribution for predictions.
> </p>
> </details>

<br>

<a name="5.1.1"></a>
### 5.1.1 Confidence Calibration
<a name="5.1.1.1"></a>
#### 5.1.1.1 Post-hoc Calibration
**[ICLR-2018]**
[Enhancing The Reliability of Out-of-distribution Image Detection in Neural Networks](https://github.com/facebookresearch/odin).
<br>
**Authors:** Liang, Shiyu and Li, Yixuan and Srikant, R.
<br>
**Institution:** University of Illinois at Urbana-Champaign; University of Wisconsin-Madison
> <details>
> <summary> Using temperature scaling on softmax probabilities with small perturbations for robustness.</summary>
> <p style="text-align:left">
> Temperature scaling can calibrate the softmax probabilities so the model takes the calibrated maximum softmax probabilities as the indicator for OOD detection. A perturbation on each sample at test time can further exploit the model robustness in detecting ID samples. However, it requires an OOD validation set for hyperparameter tuning.
> </p>
> </details>

**[CVPR-2020]**
[Generalized ODIN: Detecting Out-of-distribution Image without Learning from Out-of-distribution Data](https://arxiv.org/abs/2002.11297).
<br>
**Authors:** Hsu, Yen-Chang and Shen, Yilin and Jin, Hongxia and Kira, Zsolt
<br>
**Institution:** Georgia Institute of Technology; Samsung Research
> <details>
> <summary> Improving ODIN by decomposed confidence scoring and a modified input pre-processing method.</summary>
> <p style="text-align:left">
> The method find that previous work relies on the class posterior probability p(y|x), which does not consider the domain variable at all. Therefore, they use the explicit variable in the classifier, rewriting it as the quotient of the joint class-domain probability and the domain probability using the rule of conditional probability, and take the decomposed confidence scores for OOD detection. The decomposed confidence in the end is the probability of an input being in-distribution, computed by the cosine similarity between sample features and class features. The method also modifies the input preprocessing by only optimizing in-distribution data, therefore extra OOD validation samples are not required.
> </p>
> </details>


<br>

<a name="5.1.1.2"></a>
#### 5.1.1.2 Bayesian Methods
The Bayesian uncertainty methods could be directly applied to reject OOD samples as we would expect the uncertainty to be high on such inputs.

**[ICML-2016]**
[Dropout as a bayesian approximation: Representing model uncertainty in deep learning](https://arxiv.org/abs/1506.02142).
<br>
**Authors:** Gal, Yarin and Ghahramani, Zoubin
<br>
**Institution:** 
> <details>
> <summary>Dropout training as approximate Bayesian inference in deep Gaussian processes.</summary>
> <p style="text-align:left">
> This paper develops a new theoretical framework for deep uncertainty estimation without sacrificing either computational complexity or test accuracy, which is the drawbacks that often occur in deep Bayesian models.
> </p>
> </details>

**[NeurIPS-2017]**
[Simple and scalable predictive uncertainty estimation using deep ensembles](https://arxiv.org/abs/1612.01474).
<br>
**Authors:** Lakshminarayanan, Balaji and Pritzel, Alexander and Blundell, Charles
<br>
**Institution:**
> <details>
> <summary>Ensemble training as an alternative to Bayesian NNs for high-quality predictive uncertainty estimate.</summary>
> <p style="text-align:left">
> First work to investigate their usefulness for predictive uncertainty estimation and compare their performance to current state-of-the-art approximate Bayesian methods on a series of classification and regression benchmark datasets.
> </p>
> </details>


**[NeurIPS-2019]**
[Practical deep learning with Bayesian principles](https://arxiv.org/abs/1906.02506).
<br>
**Authors:** Osawa, Kazuki and Swaroop, Siddharth and Jain, Anirudh and Eschenhagen, Runa and Turner, Richard E and Yokota, Rio and Khan, Mohammad Emtiyaz
<br>
**Institution:** Tokyo Institute of Technology; University of Cambridge; Indian Institute of Technology; University of Osnabrück; RIKEN
> <details>
> <summary></summary>
> <p style="text-align:left">
> This work demonstrates practical training of deep networks by using recently proposed natural-gradient variational inference methods. These methods resemble the Adam optimiser, enabling us to leverage existing techniques for initialisation, momentum, batch normalisation, data augmentation, and distributed training. The results show that, despite using an approximate posterior, the training methods preserve the benefits coming from Bayesian principles. the predictive probabilities are well-calibrated, uncertainties on out-of-distribution inputs are improved, and performance for continual-learning tasks is boosted.
> </p>
> </details>


**[ICMLW-2019]**
['In-Between' Uncertainty in Bayesian Neural Networks](https://arxiv.org/abs/1906.11537).
<br>
**Authors:** Foong, Andrew YK and Li, Yingzhen and Hernandez-Lobato, Jose Miguel and Turner, Richard E
<br>
**Institution:** University of Cambridge; Microsoft Research; Alan Turing Institute
> <details>
> <summary>Linearised Laplace approximation for better ‘in-between’ uncertainty for small network architectures.</summary>
> <p style="text-align:left">
> This work shows that mean-field variational inference (MFVI) fails to give calibrated uncertainty estimates, leading to overconfident predictions when testing on out-of-distribution data. The reason is that it fails to predict with high uncertainty in regions between separated clusters of observations. Then this work finds that a classical technique, the linearised Laplace approximation, can handle ‘in-between’ uncertainty much better for small network architectures.
> </p>
> </details>


**[NeurIPS-2018]**
[Predictive Uncertainty Estimation via Prior Networks](https://arxiv.org/abs/1802.10501).
<br>
**Authors:** Foong, Andrew YK and Li, Yingzhen and Hernandez-Lobato, Jose Miguel and Turner, Richard E
<br>
**Institution:** National University of Singapore
> <details>
> <summary></summary>
> <p style="text-align:left">
> In this work, we propose an alternative approach for a DPN classifier that produces sharp, multi-modal Dirichlet distributions for OOD examples to maximize their representation gap from in-domain examples. We design a new loss function that separately models the mean and the precision of the output Dirichlet distributions by introducing a novel explicit precision regularizer along with the cross-entropy loss.
> </p>
> </details>


**[NeurIPS-2019]**
[Reverse KL-Divergence Training of Prior Networks: Improved Uncertainty and Adversarial Robustness](https://arxiv.org/abs/1905.13472).
<br>
**Authors:** Foong, Andrew YK and Li, Yingzhen and Hernandez-Lobato, Jose Miguel and Turner, Richard E
<br>
**Institution:** National University of Singapore
> <details>
> <summary></summary>
> <p style="text-align:left">
> Predictive uncertainties of DNNs can come from three different sources: model uncertainty, data uncertainty, and distributional uncertainty. Dirichlet Prior Network (DPN) separately models different uncertainty types by producing sharp uni-modal Dirichlet distributions for in-domain examples.
> </p>
> </details>



**[NeurIPS-2020]**
[Towards maximizing the representation gap between in-domain & out-of-distribution examples](https://arxiv.org/abs/2010.10474).
<br>
**Authors:** Foong, Andrew YK and Li, Yingzhen and Hernandez-Lobato, Jose Miguel and Turner, Richard E
<br>
**Institution:** National University of Singapore
> <details>
> <summary></summary>
> <p style="text-align:left">
> Predictive uncertainties of DNNs can come from three different sources: model uncertainty, data uncertainty, and distributional uncertainty. Dirichlet Prior Network (DPN) separately models different uncertainty types by producing sharp uni-modal Dirichlet distributions for in-domain examples.
> </p>
> </details>


<br>

<a name="5.1.1.3"></a>
#### 5.1.1.3 Other Confidence Enhancement Methods

**[arXiv-2018]**
[Learning confidence for out-of-distribution detection in neural networks](https://arxiv.org/abs/1802.04865).
<br>
**Authors:** DeVries, Terrance and Taylor, Graham W
<br>
**Institution:** University of Guelph; Vector Institute
> <details>
> <summary> Neural network augmented with a confidence estimation branch.</summary>
> <p style="text-align:left">
> During training, the predictions are modified according to the confidence of the network such that they are closer to the target probability distribution y. The gradual training procedure helps a better estimation of confidence.
> </p>
> </details>


**[CVPR-2019]**
[Why relu networks yield high-confidence predictions far away from the training data and how to mitigate the problem](???).
<br>
**Authors:** 
<br>
**Institution:**
Authors: Hein, Matthias and Andriushchenko, Maksym and Bitterwolf, Julian
> <details>
> <summary></summary>
> <p style="text-align:left">
> ReLU-networks lead to over-confident predictions even for samples that are far away from the in-domain distributions and propose methods to mitigate this problem
> </p>
> </details>


**[NeurIPS-2020]**
[Certifiably adversarially robust detection of out-of-distribution data](???).
<br>
**Authors:** 
<br>
**Institution:**
Authors: Bitterwolf, Julian and Meinke, Alexander and Hein, Matthias
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



**[NeurIPS-2019]**
[On mixup training: Improved calibration and predictive uncertainty for deep neural networks](???).
<br>
**Authors:** Thulasidasan, Sunil and Chennupati, Gopinath and Bilmes, Jeff and Bhattacharya, Tanmoy and Michalak, Sarah
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> We also observe that mixup-trained DNNs are less prone to over-confident predictions on out-of-distribution and random-noise data.
> </p>
> </details>



**[arXiv-2020]**
[Contrastive training for improved out-of-distribution detection](https://arxiv.org/abs/2007.05566).
<br>
**Authors:** Winkens, Jim and Bunel, Rudy and Roy, Abhijit Guha and Stanforth, Robert and Natarajan, Vivek and Ledsam, Joseph R and MacWilliams, Patricia and Kohli, Pushmeet and Karthikesalingam, Alan and Kohl, Simon and others
<br>
**Institution:** Google Health; DeepMind
> <details>
> <summary>Encourage model to learn as many high-level, task-agnostic, semantic features as possible from ID dataset through contrastive learning.</summary>
> <p style="text-align:left">
> This work proposes a new approach for OOD detection that incorporates contrastive training, which avoids explicit inlier and outlier density modelling in the input space. This work also introduce ‘Confusion Log Probability’ (CLP) as a metric to evaluate OOD detection methods. Using this metric, the proposed method improves OOD detection in both near and far OOD settings, but especially in near OOD settings.
> </p>
> </details>



**[arXiv-2019]**
[Towards neural networks that provably know when they don't know](???).
<br>
**Authors:** Meinke, Alexander and Hein, Matthias
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> We propose a Certified Certain Uncertainty (CCU) model with which one can train deep neural networks that provably make low-confidence predictions far away from the training data.
> </p>
> </details>



**[ECCV-2018]**
[Out-of-Distribution Detection Using an Ensemble of Self Supervised Leave-out Classifiers](https://arxiv.org/abs/1809.03576)
<br>
**Authors:** Vyas, Apoorv and Jammalamadaka, Nataraj and Zhu, Xia and Das, Dipankar and Kaul, Bharat and Willke, Theodore L.
<br>
**Institution:** Intel labs; Idiap Research Institute
> <details>
> <summary>Training multiple classifers by leaving out a random subset of training data as OOD data and the rest as in-distribution for ensembling.</summary>
> <p style="text-align:left">
> They add a novel margin-based loss term to maintain a margin between the average entropy of OOD and ID samples respectively. An ensemble of K leave-out classifiers is used for OOD detection. The weakness is that the large computational cost and extra OOD dataset for hyper-parameter search. 
> </p>
> </details>


**[arXiv-2020]**
[Robust out-of-distribution detection for neural networks](https://arxiv.org/abs/2003.09711).
<br>
**Authors:** Chen, Jiefeng and Li, Yixuan and Wu, Xi and Liang, Yingyu and Jha, Somesh
<br>
**Institution:** University of Wisconsin-Madison; Stanford University; Google
> <details>
> <summary>Add a optimized adversarial perturbations on in-distribution and OOD samples for robust model.</summary>
> <p style="text-align:left">
> This paper shows that existing detection mechanisms can be extremely brittle when evaluating on inputs with minimal adversarial perturbations which don’t change their semantics. To address the problem, the method performs robust training by exposing the model to perturbed adversarial in-distribution and outlier examples.
> </p>
> </details>



**[NeurIPS-2019]**
[Using self-supervised learning can improve model robustness and uncertainty](https://arxiv.org/abs/2003.09711).
<br>
**Authors:** Hendrycks, Dan and Mazeika, Mantas and Kadavath, Saurav and Song, Dawn
<br>
**Institution:** UC Berkeley; UIUC
> <details>
> <summary>An auxiliary self-supervised loss enables the detection of harder OOD examples.</summary>
> <p style="text-align:left">
> While self-supervised learning does not substantially improve accuracy compared to fully labeled training, it can improve several aspects of model robustness, including robustness to adversarial examples, label corruptions, and common input corruptions such as fog, snow, and blur.
Especially, an auxiliary self-supervised rotation loss enables the detection of harder out-of-distribution examples.
> </p>
> </details>



**[CVPR-2021]**
[MOOD: Multi-level Out-of-distribution Detection](???).
<br>
**Authors:** Lin, Ziqian and Roy, Sreya Dutta and Li, Yixuan
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> We explore and establish a direct relationship between the OOD data complexity and optimal exit level, and show that easy OOD examples can be effectively detected early without propagating to deeper layers.
> </p>
> </details>

<br>

[Back to Top](#top)

<br>

<a name="5.1.2"></a>
### 5.1.2 Outlier Exposure

**[NeurIPS-2018]**
[Reducing network agnostophobia](https://arxiv.org/abs/1811.04110).
<br>
**Authors:** Dhamija, Akshay Raj and Gunther, Manuel and Boult, Terrance E
<br>
**Institution:**
> <details>
> <summary>An entropic open-set loss and an OOD-feature-magnitudes-suppression loss on the additional background class.</summary>
> <p style="text-align:left">
> The paper designs novel losses to maximize entropy for unknown inputs while increasing separation in deep feature space by modifying magnitudes of known and unknown samples. In sum, logits entropy and feature magnitudes are used for OOD detection.
> </p>
> </details>


**[NeurIPS-2018]**
[Deep anomaly detection with outlier exposure](https://arxiv.org/abs/1610.02136)
<br>
**Authors:** Hendrycks, Dan and Mazeika, Mantas and Dietterich, Thomas
<br>
**Institution:** University of California, Berkeley; Toyota Technological Institute at Chicago
> <details>
> <summary>A baseline model to produce a uniform posterior distribution on auxiliary dataset of outliers.</summary>
> <p style="text-align:left">
> It can learn effective heuristics for detecting out-of-distribution inputs by exposing the model to OOD examples, thus learning a more conservative concept of the inliers and enabling the detection of novel forms of anomalies. The result is shown effective on both CV and NLP tasks.
> </p>
> </details>


**[ICCV-2019]**
[Unsupervised out-of-distribution detection by maximum classifier discrepancy](https://arxiv.org/abs/1908.04951)
<br>
**Authors:** Yu, Qing and Aizawa, Kiyoharu
<br>
**Institution:** The University of Tokyo
> <details>
> <summary>A network with two branches, between which entropy discrepancy is enlarged for OOD training data.</summary>
> <p style="text-align:left">
> It trains a two-head CNN consisting of one common feature extractor and two classifiers which have different decision boundaries but can classify in-distribution samples correctly. Then it uses the unlabeled data to maximize the discrepancy between the decision boundaries of two classifiers to push OOD samples outside the manifold of the in-distribution samples, which enables to detect OOD samples that are far from the support of the ID samples.
> </p>
> </details>


**[AAAI-2020]**
[Self-Supervised Learning for Generalizable Out-of-Distribution Detection](https://ojs.aaai.org/index.php/AAAI/article/view/5966)
<br>
**Authors:** Mohseni, Sina and Pitale, Mandar and Yadawa, JBS and Wang, Zhangyang
<br>
**Institution:** Texas A&M University; NVIDIA
> <details>
> <summary>Pseudo-labeling external unlabeled set for later OOD training.</summary>
> <p style="text-align:left">
> It simultaneously trains in-distribution classifiers and out-of-distribution detectors in one network. By pseudo-labeling, the unlabeled data can be assigned with label index or reject label for later training.
> </p>
> </details>


**[Neurocomputing-2021]**
[Outlier exposure with confidence control for out-of-distribution detection](https://arxiv.org/abs/1906.03509)
<br>
**Authors:** Papadopoulos, Aristotelis-Angelos and Rajati, Mohammad Reza and Shaikh, Nazim and Wang, Jiamian
<br>
**Institution:** University of Southern California
> <details>
> <summary>Performing prediction confidence calibration on the top of OE.</summary>
> <p style="text-align:left">
> Based on the loss function of OE, this work add the second regularization term to minimize the Euclidean distance between the training accuracy of a DNN and the average confidence in its predictions on the training set.
> </p>
> </details>


**[CVPR-2020]**
[Background data resampling for outlier-aware classification](https://arxiv.org/abs/2006.15207)
<br>
**Authors:** Li, Yi and Vasconcelos, Nuno
<br>
**Institution:** University of California, San Diego
> <details>
> <summary>Using adversarial resampling approach to obtain a compact yet representative set of background data points.</summary>
> <p style="text-align:left">
> This work focuses on training with background and claims that using all background data leads to inefficient or even impractical solution due to imbalance and computational complexity. The resampling algorithm takes inspiration from prior work on hard negative mining, performing an iterative adversarial weighting on the background examples and using the learned weights to obtain the subset of desired size. 
> </p>
> </details>


**[ICMLW-2020]**
[Robust Out-of-distribution Detection via Informative Outlier Mining](https://arxiv.org/abs/2006.15207)
<br>
**Authors:** Chen, Jiefeng and Li, Yixuan and Wu, Xi and Liang, Yingyu and Jha, Somesh
<br>
**Institution:** University of Wisconsin-Madison; Google
> <details>
> <summary>Using adversarial training to select auxiliary outlier data for a tight decision boundary between ID and OOD data.</summary>
> <p style="text-align:left">
> By mining informative auxiliary OOD data, one can significantly improve OOD detection performance, and somewhat surprisingly, generalize to unseen adversarial attack. The key idea is to selectively utilize auxiliary outlier data for estimating a tight decision boundary between ID and OOD data, which leads to robust OOD detection performance.
> </p>
> </details>


**[arXiv-2021]**
[An Effective Baseline for Robustness to Distributional Shift](https://arxiv.org/abs/2105.07107)
<br>
**Authors:** Thulasidasan, Sunil and Thapa, Sushil and Dhaubhadel, Sayera and Chennupati, Gopinath and Bhattacharya, Tanmoy and Bilmes, Jeff
<br>
**Institution:** University of Wisconsin-Madison; Google
> <details>
> <summary>An extra abstention (or rejection class) in combination with outlier training data for effective OoD detection.</summary>
> <p style="text-align:left">
> This work demonstrates the efficacy of using an extra abstention (or rejection class) in combination with outlier training data for effective OoD detection.
> </p>
> </details>



<br>

[Back to Top](#top)

<br>

<a name="5.1.3"></a>
### 5.1.3 OOD Data Generation

**[ICLR-2018]**
[Training confidence-calibrated classifiers for detecting out-of-distribution samples](https://arxiv.org/abs/1711.09325)
<br>
**Authors:** Lee, Kimin and Lee, Honglak and Lee, Kibok and Shin, Jinwoo
<br>
**Institution:** KAIST; University of Michigan, Ann Arbor; Google Brain
> <details>
> <summary>An confidence loss to encourage a uniform prediction of GAN-generated ‘boundary’ OOD samples.</summary>
> <p style="text-align:left">
> It proposes an confidence loss to minimize the KL divergence from the predictive distribution on the GAN-generated OOD samples to the uniform one in order to give less confident predictions on them. The proposed GAN generates ‘boundary’ samples in the in-distribution low-density area.
> </p>
> </details>



**[NeurIPSW-2018]**
[Building robust classifiers through generation of confident out of distribution examples](?)
<br>
**Authors:** Sricharan, Kumar and Srivastava, Ashok
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>


**[CVPR-2019]**
[Out-of-distribution detection for generalized zero-shot action recognition](?)
<br>
**Authors:** Mandal, Devraj and Narayan, Sanath and Dwivedi, Sai Kumar and Gupta, Vikram and Ahmed, Shuaib and Khan, Fahad Shahbaz and Shao, Ling
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>


**[NeurIPSW-2019]**
[Out-of-distribution detection in classifiers via generation]()
<br>
**Authors:** Vernekar, Sachin and Gaurav, Ashish and Abdelzad, Vahdat and Denouden, Taylor and Salay, Rick and Czarnecki, Krzysztof
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



<br>

[Back to Top](#top)

<br>

<a name="5.1.4"></a>
### 5.1.4 Label Space Redesign

**[CVPR-2021]**
[MOS: Towards Scaling Out-of-distribution Detection for Large Semantic Space](https://arxiv.org/abs/2105.01879).
<br>
**Authors:** Huang, Rui and Li, Yixuan.
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>


**[NeurIPS-2018]**
[Out-of-Distribution Detection using Multiple Semantic Label Representations](https://arxiv.org/abs/1808.06664). 
<br>
**Authors:** Shalev, Gabi and Adi, Yossi and Keshet, Joseph.
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> use multiple semantic dense
representations as the target label to train the OOD detection network.
> </p>
> </details>


<br>

[Back to Top](#top)

<br>

<a name="5.1.5"></a>
### 5.1.5 Big Pretrained Model
**[arXiv-2021]**
[Exploring the Limits of Out-of-Distribution Detection](https://arxiv.org/abs/2106.03004)
**Authors:** Fort, Stanislav and Ren, Jie and Lakshminarayanan, Balaji
**Institution:** Stanford University; Google Research
> <details>
> <summary>Large-scale pre-trained transformers significantly improve near-OOD tasks</summary>
> <p style="text-align:left">
> This work explores the effectiveness of large-scale pre-trained transformers, especially when few-shot outlier exposure is available. It also shows that the pre-trained multi-modal image-text transformers CLIP is also effective on OOD detection if using the names of outlier classes as candidate text labels.
> </p>
> </details>



**[arXiv-2020]**
[Pretrained transformers improve out-of-distribution robustness](??)
<br>
**Authors:** Hendrycks, Dan and Liu, Xiaoyuan and Wallace, Eric and Dziedzic, Adam and Krishnan, Rishabh and Song, Dawn
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



**[arXiv-2021]**
[OODformer: Out-Of-Distribution Detection Transformer](??)
<br>
**Authors:** Koner, Rajat and Sinhamahapatra, Poulami and Roscher, Karsten and G{\"u}nnemann, Stephan and Tresp, Volker
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>


<br>

[Back to Top](#top)

<br>

<a name="5.2"></a>
## 5.2 Density-based Method
<a name="5.2.1"></a>
### 5.2.1 Embedding-based Method

**[NeurIPS-2018]**
[A simple unified framework for detecting out-of-distribution samples and adversarial attacks](https://arxiv.org/abs/1807.03888)
<br>
**Authors:** Lee, Kimin and Lee, Kibok and Lee, Honglak and Shin, Jinwoo
<br>
**Institution:** KAIST; University of Michigan; Google Brain; AItrics
> <details>
> <summary>Using the class conditional Gaussian distributions with respect to low- and upper-level features.</summary>
> <p style="text-align:left">
> The model estimates standard class-conditional Gaussian distribution on intermediate activations to detect OOD samples. It makes use of Mahalanobis distance therefore it can be also interpreted as distance-based method.
> </p>
> </details>


**[NeurIPS-2019]**
[Likelihood ratios for out-of-distribution detection](https://arxiv.org/abs/1906.02845)
<br>
**Authors:** Ren, Jie and Liu, Peter J and Fertig, Emily and Snoek, Jasper and Poplin, Ryan and DePristo, Mark A and Dillon, Joshua V and Lakshminarayanan, Balaji
<br>
**Institution:** Google Research; DeepMind
> <details>
> <summary>Using likelihood ratios to cancel out background influence.</summary>
> <p style="text-align:left">
> This work finds the likelihood score is heavily affected by background, so likelihood ratios are used to cancel out background influence. The Likelihood Ratio (LR) is the likelihood that a given test result would be expected in a patient with the target disorder compared to the likelihood that that same result would be expected in a patient without the target disorder.
> </p>
> </details>



**[NeurIPS-2019]**
[Further analysis of outlier detection with deep generative models](?)
<br>
**Authors:** Wang, Ziyu and Dai, Bin and Wipf, David and Zhu, Jun
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



**[NeurIPS-2020]**
[Likelihood regret: An out-of-distribution detection score for variational auto-encoder](?)

Authors: Xiao, Zhisheng and Yan, Qing and Amit, Yali
<br>
**Authors:** 
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



**[NeurIPS-2018]**
[Do deep generative models know what they don't know?](?)
<br>
**Authors:** Nalisnick, Eric and Matsukawa, Akihiro and Teh, Yee Whye and Gorur, Dilan and Lakshminarayanan, Balaji
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> This work shows that even powerful neural generative models often assign higher probabilities to out-of-distribution test examples than to in-distribution test examples.
> </p>
> </details>



**[ICLR-2020]**
[Novelty detection via blurring](?)

Authors: Choi, Sungik and Chung, Sae-Young
<br>
**Authors:** 
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> We discover that such conventional novelty detection schemes are also vulnerable to blurred images.
> </p>
> </details>



**[ICLR-2020]**
[Input complexity and out-of-distribution detection with likelihood-based generative models](?)

Authors: Serra, Joan and Alvarez, David and Gomez, Vicenc and Slizovskaia, Olga and Nunez, Jose F and Luque, Jordi
<br>
**Authors:** 
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



**[arXiv-2020]**
[Probabilistic auto-encoder]()

Authors: B{\"o}hm, Vanessa and Seljak, Uro{\v{s}}
<br>
**Authors:** 
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



**[CVPR-2021]**
[Soft-IntroVAE: Analyzing and Improving the Introspective Variational Autoencoder](?)

Authors: Daniel, Tal and Tamar, Aviv
<br>
**Authors:** 
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



<br>

[Back to Top](#top)

<br>

<a name="5.2.2"></a>
### 5.2.2 Flow-based Method
**[CVPR-2020]**
[Deep residual flow for out of distribution detection](?)
<br>
**Authors:** Zisselman, Ev and Tamar, Aviv
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> It uses a residual flow, a novel flow architecture that learns the residual distribution from a base Gaussian distribution.
> </p>
> </details>



**[NeurIPS-2020]**
[Why normalizing flows fail to detect out-of-distribution data](?)
<br>
**Authors:** Kirichenko, Polina and Izmailov, Pavel and Wilson, Andrew Gordon
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> Conclusion is that flows do not represent images based on their semantic contents, but rather directly encode their visual appearance.
> </p>
> </details>



**[NeurIPS-2020]**
[Understanding anomaly detection with deep invertible networks through hierarchies of distributions and features](?)

Authors: Schirrmeister, Robin Tibor and Zhou, Yuxuan and Ball, Tonio and Zhang, Dan
<br>
**Authors:** 
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



<br>

[Back to Top](#top)

<br>

<a name="5.2.3"></a>
### 5.2.3 Energy-based Method
**[ICLR-2019]**
[Your classifier is secretly an energy based model and you should treat it like one](?)

Authors: Grathwohl, Will and Wang, Kuan-Chieh and Jacobsen, J{\"o}rn-Henrik and Duvenaud, David and Norouzi, Mohammad and Swersky, Kevin
<br>
**Authors:** 
<br>
**Institution:**
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>



**[NeurIPS-2020]**
[Energy-based out-of-distribution detection](https://arxiv.org/abs/2010.03759)
<br>
**Authors:** Liu, Weitang and Wang, Xiaoyun and Owens, John D and Li, Yixuan
<br>
**Institution:** University of California, San Diego; University of California, Davis; University of Wisconsin-Madison
> <details>
> <summary>Using energy scores instead of softmax scores to conveniently achieve good results.</summary>
> <p style="text-align:left">
> Unlike softmax confidence scores, energy scores are theoretically aligned with the probability density of the inputs and are less susceptible to the overconfidence issue. The paper shows that energy can conveniently replace softmax confidence for any pre-trained neural network, and proposes an energy-bounded learning objective to fine-tune the network.
> </p>
> </details>


<br>

[Back to Top](#top)

<br>

<a name="5.3"></a>
## 5.3 Distance-based Method
**[NeurIPS-2018]**
[A simple unified framework for detecting out-of-distribution samples and adversarial attacks](https://arxiv.org/abs/1807.03888)
<br>
**Authors:** Lee, Kimin and Lee, Kibok and Lee, Honglak and Shin, Jinwoo
<br>
**Institution:** KAIST; University of Michigan; Google Brain; AItrics
> <details>
> <summary>OOD detection with Mahalanobis distance</summary>
> <p style="text-align:left">
> This work uses the class conditional Gaussian distributions with respect to low- and upper-level features of the deep models under Gaussian discriminant analysis, which result in a confidence score based on the Mahalanobis distance.
> </p>
> </details>


**[arXiv-2021]**
[A Simple Fix to Mahalanobis Distance for Improving Near-OOD Detection](https://arxiv.org/abs/2106.09022)
<br>
**Authors:** Ren, Jie and Fort, Stanislav and Liu, Jeremiah and Roy, Abhijit Guha and Padhy, Shreyas and Lakshminarayanan, Balaji
<br>
**Institution:** Google Research; Stanford University; Harvard University; Google Health
> <details>
> <summary></summary>
> <p style="text-align:left">
> It proposes a relative Mahalanobis distance (RMD) which improves performance and is more robust to hyperparameter choice. RMD is equivalent to computing a likelihood ratio, which calculates the division between the sophisticated foreground distribution and background distribution as confidence score.
> </p>
> </details>


**[ACCV-2020]**
[Hyperparameter-free out-of-distribution detection using cosine similarity](https://arxiv.org/abs/1905.10628)
<br>
**Authors:** Techapanurak, Engkarat and Suganuma, Masanori and Okatani, Takayuki
<br>
**Institution:** Tohoku University; RIKEN
> <details>
> <summary> Using scaled cosine similarity between test sample features and class features to determine OOD samples. </summary>
> <p style="text-align:left">
> The first work employs softmax of scaled cosine similarity instead of ordinary softmax of logits. Taking the metric learning idea into OOD detection. It is also the concurrent work of Generalized ODIN.
> </p>
> </details>


**[CVPR-2021]**
[Out-of-Distribution Detection Using Union of 1-Dimensional Subspaces](https://github.com/zaeemzadeh/OOD)
<br>
**Authors:** Zaeemzadeh, Alireza and Bisagno, Niccol{\`o} and Sambugaro, Zeno and Conci, Nicola and Rahnavard, Nazanin and Shah, Mubarak
<br>
**Institution:** University of Central Florida; University of Trento
> <details>
> <summary> Calculating class membership probabilities in a union of 1-dimensional subspaces.</summary>
> <p style="text-align:left">
> The cosine similarities between the extracted feature and the class vectors are used to compute the class membership probabilities, using a Union of 1-dimensional subspaces. The 1-dimensional subspaces is spanned by the first singular vector of the feature vectors extracted from the training set. Feature vectors lie on a union of 1-dimensional subspaces helps OOD samples to be robustly detected.
> </p>
> </details>


**[ECCV-2020]**
[A boundary based out-of-distribution classifier for generalized zero-shot learning](https://arxiv.org/abs/2008.04872)

Authors: Chen, Xingyu and Lan, Xuguang and Sun, Fuchun and Zheng, Nanning.


**[arXiv-2020]**
[Feature Space Singularity for Out-of-Distribution Detection](https://arxiv.org/abs/2011.14654)
<br>
**Authors:** Huang, Haiwen and Li, Zhihan and Wang, Lulu and Chen, Sishuo and Dong, Bin and Zhou, Xinyu
<br>
**Institution:** University of Oxford; Peking University; MEGVII Technology; etc.
> <details>
> <summary> Distance to Feature Space Singularity can measure OOD.</summary>
> <p style="text-align:left">
> It is observed that in feature spaces, OOD samples concentrate near a Feature Space Singularity (FSS) point, and the distance from a sample to FSS measures the degree of OOD. It can be exlained that moving speeds of features of other data depend on their similarity to the training data. During training, they use generated uniform noise or validation data as OOD.
> </p>
> </details>


**[ICML-2020]**
[Uncertainty estimation using a single deep deterministic neural network](?)
<br>
**Authors:** Van Amersfoort, Joost and Smith, Lewis and Teh, Yee Whye and Gal, Yarin
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> This method trains a feature extractor without a softmax layer. Instead, it learns a centroid per class and attracts samples towards the centroids of their class, similar to contrastive losses. It uses a Radial Basis Function (RBF) kernel to compute the distance between the input’s embedding and the class centroids. The distance to the closest centroid defines classification, and is also used as the OOD score.
> </p>
> </details>


<br>

[Back to Top](#top)

<br>

<a name="5.4"></a>
## 5.4 Meta-Learning-based Method

**[ICML-2020]**
[Detecting out-of-distribution examples with gram matrices](http://proceedings.mlr.press/v119/sastry20a/sastry20a.pdf)
<br>
**Authors:** Sastry, Chandramouli Shama and Oore, Sageev
<br>
**Institution:** Dalhousie University
> <details>
> <summary>Jointly considering the class assigned at the output layer and the activity patterns in the intermediate layers.</summary>
> <p style="text-align:left">
> It uses activity patterns to detect anomalies, i.e., the path by which it arrived at that prediction. Gram Matrices not only describe the activations at the individual channels but also summarize the pairwise interactions between the channels.
> </p>
> </details>

**[NeurIPS-2020]**
[OOD-MAML: Meta-learning for few-shot out-of-distribution detection and classification](?)

Authors: Jeong, Taewon and Kim, Heeyoung

**[ICLR-2020]**
[Learning to balance: Bayesian meta-learning for imbalanced and out-of-distribution tasks](?)

Authors: Lee, Hae Beom and Lee, Hayeon and Na, Donghyun and Kim, Saehoon and Park, Minseop and Yang, Eunho and Hwang, Sung Ju

<br>

[Back to Top](#top)

<br>

<a name="5.5"></a>
## 5.5 Hybrid Method and Others

Isolation forests exploits the fact that anomalies are scarce and different and while constructing the isolation tree, it is observed that the anomalous samples appear close to the root of the tree. These anomalies are then identified by measuring the length of the path from the root to a terminating node; the closer a node is to the root, the higher is its chance of representing an OOD.

<br>

[Back to Top](#top)

<br>

<a name="5.5"></a>
## 5.6 Discussion
**[BMVC-2019]**
[A Less Biased Evaluation of Out-of-distribution Sample Detectors](https://arxiv.org/abs/1809.04729)
<br>
**Author:** Shafaei, Alireza and Schmidt, Mark and Little, James J
<br>
**Institution:** University of British Columbia
> <details>
> <summary>A three-dataset evaluation scheme as a more reliable strategy to assess progress.</summary>
> <p style="text-align:left">
> Classic OOD detection testing may produce a biased result since the distribution of outliers used in training may not be the same as the distribution of outliers encountered in the application. An exhaustive evaluation shows realistic applications of high-dimensional images the previous techniques have low accuracy and are not reliable in practice.
> </p>
> </details>

<br>

[Back to Top](#top)

<br>

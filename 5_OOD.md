<a name="top"></a>
# 5. OOD Detection
- [5.1 Classfication-based Method](#5.1)
  - [5.1.1 Output-based Methods](#5.1.1)
    - [5.1.1.1 Post-hoc Methods](#5.1.1.1)
    - [5.1.1.2 Confidence Enhancement](#5.1.1.2)
    - [5.1.1.3 Outlier Explosure](#5.1.1.3)
  - [5.1.2 OOD Data Generation](#5.1.2)
  - [5.1.3 Gradient-based Methods](#5.1.3)
  - [5.1.4 Bayesian Models](#5.1.4)
  - [5.1.5 Big Pretrained Model](#5.1.5)
- [5.2 Density-based Method](#5.2)
- [5.3 Distance-based Method](#5.3)


<a name="5.1"></a>
## 5.1 Classfication-based Method

<a name="5.1.1"></a>
### 5.1.1 Output-based Methods
<a name="5.1.1.1"></a>
#### 5.1.1.1 Post-hoc Methods

**[ICLR-2017]**
[A Baseline for Detecting Misclassified and Out-of-Distribution Examples in Neural Networks](https://arxiv.org/abs/1610.02136).
<br>
**Authors:** Dan Hendrycks, Kevin Gimpel
<br>
**Institution:** University of California, Berkeley; Toyota Technological Institute at Chicago
> <details>
> <summary> The starting point of OOD detection, proposing a baseline simply uses softmax probabilities to detect OOD.</summary>
> <p style="text-align:left">
> Correctly classified examples tend to have greater maximum softmax probabilities than erroneously classified and out-of-distribution examples, allowing for their detection. However, due to the overconfidence characteristics of deep models, the baseline cannot be well performed. The overconfidence property comes from softmax always modeling sharp distribution for predictions.
> </p>
> </details>


**[ICLR-2018]**
[Enhancing The Reliability of Out-of-distribution Image Detection in Neural Networks](https://github.com/facebookresearch/odin).
<br>
**Authors:** Shiyu Liang, Yixuan Li, R.rikant
<br>
**Institution:** University of Illinois at Urbana-Champaign; University of Wisconsin-Madison
> <details>
> <summary> Using temperature scaling on softmax probabilities with small perturbations for reliability.</summary>
> <p style="text-align:left">
> Temperature scaling has a strong smoothing effect that transforms the softmax score back to the logit space, which effectively distinguishes ID vs.OOD.  A perturbation on each sample at test time can further increase the separability between ID and OOD data. 
> </p>
> </details>

**[NeurIPS-2020]**
[Energy-based Out-of-distribution Detection](https://arxiv.org/abs/2010.03759).
<br>
**Authors:** Weitang Liu, Xiaoyun Wang, John D. Owens, Yixuan Li
<br>
**Institution:** University of California, San Diego; University of California, Davis; University of Wisconsin-Madison
> <details>
> <summary>Using energy scores instead of softmax scores to conveniently achieve good results.</summary>
> <p style="text-align:left">
> Unlike softmax confidence scores, energy scores are theoretically aligned with the probability density of the inputs and are less susceptible to the overconfidence issue. The paper shows that energy can conveniently replace softmax confidence for any pre-trained neural network, and proposes an energy-bounded learning objective to fine-tune the network.
> </p>
> </details>


**[ICML-2020]**
[Detecting Out-of-Distribution Examples with In-distribution Examples and Gram Matrices](https://arxiv.org/abs/1912.12510).
<br>
**Authors:** Chandramouli Shama Sastry, Sageev Oore
<br>
**Institution:** Dalhousie University, Halifax

**[CVPR-2021]**
[MOOD: Multi-level Out-of-distribution Detection](https://arxiv.org/abs/2104.14726).
<br>
**Authors:** Ziqian Lin, Sreya Dutta Roy, Yixuan Li
<br>
**Institution:** University of Wisconsin-Madison
> <details>
> <summary>Accelerate training by finding optimal exit level via data complexity.</summary>
> <p style="text-align:left">
>We explore and establish a direct relationship between the OOD data complexity and optimal exit level, and show that easy OOD examples can be effectively detected early without propagating to deeper layers.
> </p>
> </details>

**[NeurIPS-2021]**
[React: Out-of-distribution detection with rectified activations](http://pages.cs.wisc.edu/~sharonli/).
<br>
**Authors:** Yiyou Sun, Chuan Guo and Yixuan Li
<br>
**Institution:** University of Wisconsin-Madison, Facebook AI Research


**[NeurIPS-2021]**
[On the Importance of Gradients for Detecting Distributional Shifts in the Wild](https://arxiv.org/abs/2110.00218).
<br>
**Authors:** Rui Huang, Andrew Geng, Yixuan Li
<br>
**Institution:** University of Wisconsin-Madison



**[NeurIPS-2021]**
[Can multi-label classification networks know what they don’t know?](https://arxiv.org/abs/2109.14162).
<br>
**Authors:** Haoran Wang, Weitang Liu, Alex Bocchieri, Yixuan Li
<br>
**Institution:** Carnegie Mellon University; University of California, San Diego; Department of Computer Sciences
University of Wisconsin-Madison



<br>

<a name="5.1.1.2"></a>
#### 5.1.1.2 Confidence Enhancement

**[arXiv-2017]**
[Improved Regularization of Convolutional Neural Networks with Cutout](https://arxiv.org/abs/1708.04552).
<br>
**Authors:** Terrance DeVries, Graham W. Taylor
<br>
**Institution:** University of Guelph; Canadian Institute for Advanced Research and Vector Institute


**[arXiv-2018]**
[Learning Confidence for Out-of-Distribution Detection in Neural Networks](https://arxiv.org/abs/1802.04865).
<br>
**Authors:** Terrance DeVries, Graham W. Taylor
<br>
**Institution:** University of Guelph; Vector Institute
> <details>
> <summary> Neural network augmented with a confidence estimation branch. </summary>
> <p style="text-align:left">
> During training, the predictions are modified according to the confidence of the network such that they are closer to the target probability distribution y. The gradual training procedure helps a better estimation of confidence.
> </p>
> </details>


**[ECCV-2018]**
[Out-of-Distribution Detection Using an Ensemble of Self Supervised Leave-out Classifiers](https://arxiv.org/abs/1809.03576).
<br>
**Authors:** Apoorv Vyas, Nataraj Jammalamadaka, Xia Zhu, Dipankar Das, Bharat Kaul, Theodore L. Willke
<br>
**Institution:** Intel labs, Bangalore, India; Intel labs, Hillsboro; Idiap Research Institute, Switzerland
> <details>
> <summary> Training multiple classifers by leaving out a random subset of training data as OOD data and the rest as in-distribution for ensembling. </summary>
> <p style="text-align:left">
>They add a novel margin-based loss term to maintain a margin between the average entropy of OOD and ID samples respectively. An ensemble of K leave-out classifiers is used for OOD detection. The weakness is that the large computational cost and extra OOD dataset for hyper-parameter search.
> </p>
> </details>


**[CVPR-2019]**
[Why ReLU networks yield high-confidence predictions far away from the training data and how to mitigate the problem](https://arxiv.org/abs/1812.05720).
<br>
**Authors:** Matthias Hein, Maksym Andriushchenko, Julian Bitterwolf
<br>
**Institution:** University of T¨ubingen; Saarland University
> <details>
> <summary>ReLU-networks lead to over-confident predictions </summary>
> <p style="text-align:left">
> ReLU-networks lead to over-confident predictions even for samples that are far away from the in-domain distributions and propose methods to mitigate this problem
> </p>
> </details>


**[NeurIPS-2019]**
[On Mixup Training: Improved Calibration and Predictive Uncertainty for Deep Neural Networks](https://arxiv.org/abs/1905.11001).
<br>
**Authors:** Sunil Thulasidasan, Gopinath Chennupati, Jeff Bilmes, Tanmoy Bhattacharya, Sarah Michalak
<br>
**Institution:** Los Alamos National Laboratory; University of Washington
> <details>
> <summary>Mixup-training helps.</summary>
> <p style="text-align:left">
> We also observe that mixup-trained DNNs are less prone to over-confident predictions on out-of-distribution and random-noise data.
> </p>
> </details>



**[CVPR-2019]**
[CutMix: Regularization Strategy to Train Strong Classifiers with Localizable Features](https://arxiv.org/abs/1905.04899).
<br>
**Authors:** Sangdoo Yun, Dongyoon Han, Seong Joon Oh, Sanghyuk Chun, Junsuk Choe, Youngjoon Yoo
<br>
**Institution:** 1Clova AI Research, NAVER Corp; Clova AI Research, LINE Plus Corp; Yonsei University


**[arXiv-2019]**
[AugMix: A Simple Data Processing Method to Improve Robustness and Uncertainty](https://arxiv.org/abs/1912.02781).
<br>
**Authors:** Dan Hendrycks, Norman Mu, Ekin D. Cubuk, Barret Zoph, Justin Gilmer, Balaji Lakshminarayanan
<br>
**Institution:** DeepMind; Google


**[arXiv-2019]**
[Towards neural networks that provably know when they don't know](https://arxiv.org/abs/1909.12180).
<br>
**Authors:** Alexander Meinke, Matthias Hein
<br>
**Institution:** University of Tübingen
> <details>
> <summary>Certified Certain Uncertainty</summary>
> <p style="text-align:left">
>We propose a Certified Certain Uncertainty (CCU) model with which one can train deep neural networks that provably make low-confidence predictions far away from the training data.
> </p>
> </details>



**[CVPR-W-2020]**
[On Out-of-Distribution Detection Algorithms With Deep Neural Skin Cancer Classifiers](https://openaccess.thecvf.com/content_CVPRW_2020/html/w42/Pacheco_On_Out-of-Distribution_Detection_Algorithms_With_Deep_Neural_Skin_Cancer_Classifiers_CVPRW_2020_paper.html).
<br>
**Authors:** Andre G. C. Pacheco, Chandramouli S. Sastry, Thomas Trappenberg, Sageev Oore, Renato A. Krohling
<br>
**Institution:** Federal University of Espirito Santo; Dalhousie University; Vector Institute


**[CVPR-2020]**
[Generalized ODIN: Detecting Out-of-distribution Image without Learning from Out-of-distribution Data](https://arxiv.org/abs/2002.11297).
<br>
**Authors:** Yen-Chang Hsu, Yilin Shen, Hongxia Jin, Zsolt Kira
<br>
**Institution:** Georgia Institute of Technology; Samsung Research
> <details>
> <summary> Improving ODIN by decomposed confidence scoring and a modified input pre-processing method.</summary>
> <p style="text-align:left">
> The method find that previous work relies on the class posterior probability p(y|x), which does not consider the domain variable at all. Therefore, they use the explicit variable in the classifier, rewriting it as the quotient of the joint class-domain probability and the domain probability using the rule of conditional probability, and take the decomposed confidence scores for OOD detection. The decomposed confidence in the end is the probability of an input being in-distribution, computed by the cosine similarity between sample features and class features. The method also modifies the input preprocessing by only optimizing in-distribution data, therefore extra OOD validation samples are not required.
> </p>
> </details>

**[NeurIPS-2020]**
[Certifiably Adversarially Robust Detection of Out-of-Distribution Data](https://arxiv.org/abs/2007.08473).
<br>
**Authors:** Julian Bitterwolf, Alexander Meinke, Matthias Hein
<br>
**Institution:** University of Tübingen


**[arXiv-2020]**
[Robust Out-of-distribution Detection for Neural Networks](https://arxiv.org/abs/2003.09711).
<br>
**Authors:** Jiefeng Chen, Yixuan Li, Xi Wu, Yingyu Liang, Somesh Jha
<br>
**Institution:** University of Wisconsin-Madison; Stanford University; Google
> <details>
> <summary> Add a optimized adversarial perturbations on in-distribution and OOD samples for robust model. </summary>
> <p style="text-align:left">
>This paper shows that existing detection mechanisms can be extremely brittle when evaluating on inputs with minimal adversarial perturbations which don’t change their semantics. To address the problem, the method performs robust training by exposing the model to perturbed adversarial in-distribution and outlier examples.
> </p>
> </details>

**[ICLR-2020]**
[Novelty Detection Via Blurring](https://arxiv.org/abs/1911.11943).
<br>
**Authors:** Sungik Choi, Sae-Young Chung
<br>
**Institution:** Korea Advanced Institute of Science and Technology



<br>

[Back to Top](#top)

<br>

<a name="5.1.1.3"></a>
#### 5.1.1.3 Outlier Exposure (OE)

**[NeurIPS-2018]**
[Reducing network agnostophobia](https://arxiv.org/abs/1811.04110).
<br>
**Authors:** Akshay Raj Dhamija, Manuel Günther, Terrance E. Boult
<br>
**Institution:** Vision and Security Technology Lab; University of Colorado Colorado Springs
> <details>
> <summary>An entropic open-set loss and an OOD-feature-magnitudes-suppression loss on the additional background class.</summary>
> <p style="text-align:left">
> The paper designs novel losses to maximize entropy for unknown inputs while increasing separation in deep feature space by modifying magnitudes of known and unknown samples. In sum, logits entropy and feature magnitudes are used for OOD detection.
> </p>
> </details>



**[ICLR-2019]**
[Deep anomaly detection with outlier exposure](https://arxiv.org/abs/1812.04606)
<br>
**Authors:** Dan Hendrycks, Mantas Mazeika, Thomas Dietterich
<br>
**Institution:** University of California, Berkeley; University of Chicago; Oregon State University
> <details>
> <summary>A baseline model to produce a uniform posterior distribution on auxiliary dataset of outliers.</summary>
> <p style="text-align:left">
> It can learn effective heuristics for detecting out-of-distribution inputs by exposing the model to OOD examples, thus learning a more conservative concept of the inliers and enabling the detection of novel forms of anomalies. The result is shown effective on both CV and NLP tasks.
> </p>
> </details>



**[ICCV-2019]**
[Unsupervised out-of-distribution detection by maximum classifier discrepancy](https://arxiv.org/abs/1908.04951)
<br>
**Authors:** Qing Yu, Kiyoharu Aizawa
<br>
**Institution:** The University of Tokyo
> <details>
> <summary>A network with two branches, between which entropy discrepancy is enlarged for OOD training data.</summary>
> <p style="text-align:left">
> It trains a two-head CNN consisting of one common feature extractor and two classifiers which have different decision boundaries but can classify in-distribution samples correctly. Then it uses the unlabeled data to maximize the discrepancy between the decision boundaries of two classifiers to push OOD samples outside the manifold of the in-distribution samples, which enables to detect OOD samples that are far from the support of the ID samples.
> </p>
> </details>

**[BMVC-2019]**
[A Less Biased Evaluation of Out-of-distribution Sample Detectors](https://arxiv.org/abs/1809.04729).
<br>
**Authors:** Alireza Shafaei, Mark Schmidt, James J. Little
<br>
**Institution:** University of British Columbia


**[AAAI-2020]**
[Self-Supervised Learning for Generalizable Out-of-Distribution Detection](https://ojs.aaai.org/index.php/AAAI/article/view/5966)
<br>
**Authors:** Sina Mohseni, Mandar Pitale, JBS Yadawa, Zhangyang Wang
<br>
**Institution:** Texas A&M University; NVIDIA
> <details>
> <summary>Pseudo-labeling external unlabeled set for later OOD training.</summary>
> <p style="text-align:left">
> It simultaneously trains in-distribution classifiers and out-of-distribution detectors in one network. By pseudo-labeling, the unlabeled data can be assigned with label index or reject label for later training.
> </p>
> </details>



**[CVPR-2020]**
[Background data resampling for outlier-aware classification](https://openaccess.thecvf.com/content_CVPR_2020/html/Li_Background_Data_Resampling_for_Outlier-Aware_Classification_CVPR_2020_paper.html)
<br>
**Authors:** Yi Li, Nuno Vasconcelos
<br>
**Institution:** University of California, San Diego
> <details>
> <summary>Using adversarial resampling approach to obtain a compact yet representative set of background data points.</summary>
> <p style="text-align:left">
> This work focuses on training with background and claims that using all background data leads to inefficient or even impractical solution due to imbalance and computational complexity. The resampling algorithm takes inspiration from prior work on hard negative mining, performing an iterative adversarial weighting on the background examples and using the learned weights to obtain the subset of desired size.
> </p>
> </details>


**[AAAI-2020]**
[Self-Supervised Learning for Generalizable Out-of-Distribution Detection](https://ojs.aaai.org/index.php/AAAI/article/view/5966)
<br>
**Authors:** Sina Mohseni，Mandar Pitale, JBS Yadawa，Zhangyang Wang
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
**Authors:** Aristotelis-Angelos Papadopoulos, Mohammad Reza Rajati, Nazim Shaikh, Jiamian Wang
<br>
**Institution:** University of Southern California
> <details>
> <summary>Performing prediction confidence calibration on the top of OE.</summary>
> <p style="text-align:left">
> Based on the loss function of OE, this work add the second regularization term to minimize the Euclidean distance between the training accuracy of a DNN and the average confidence in its predictions on the training set.
> </p>
> </details>


**[ICCV-2021]**
[Semantically Coherent Out-of-Distribution Detection](https://arxiv.org/abs/2108.11941).
<br>
**Authors:** Jingkang Yang, Haoqi Wang, Litong Feng, Xiaopeng Yan, Huabin Zheng, Wayne Zhang, Ziwei Liu
<br>
**Institution:** Nanyang Technological University; SenseTime Research, Shanghai Jiaotong Univerisity; Shanghai AI Lab.


**[ECML PKDD-2021]**
[ATOM: Robustifying Out-of-distribution Detection Using Outlier Mining](https://arxiv.org/abs/2006.15207)
<br>
**Authors:** Jiefeng Chen, Yixuan Li, Xi Wu, Yingyu Liang, Somesh Jha
<br>
**Institution:** University of Wisconsin-Madison;  Google
> <details>
> <summary>Using informative auxiliary outlier data to learn a tight decision boundary between ID and OOD data.</summary>
> <p style="text-align:left">
>By mining informative auxiliary OOD data, one can significantly improve OOD detection performance, and somewhat surprisingly, generalize to unseen adversarial attack. The key idea is to selectively utilize auxiliary outlier data for estimating a tight decision boundary between ID and OOD data, which leads to robust OOD detection performance.
> </p>
> </details>
> 
**[arXiv-2021]**
[An Effective Baseline for Robustness to Distributional Shift](https://arxiv.org/abs/2105.07107)
<br>
**Authors:** Sunil Thulasidasan, Sushil Thapa, Sayera Dhaubhadel, Gopinath Chennupati, Tanmoy Bhattacharya, Jeff Bilmes
<br>
**Institution:** Los Alamos; New Mexico Tech; University of Washington
> <details>
> <summary>An extra abstention (or rejection class) in combination with outlier training data for effective OoD detection.</summary>
> <p style="text-align:left">
> This work demonstrates the efficacy of using an extra abstention (or rejection class) in combination with outlier training data for effective OoD detection.
> </p>
> </details>






<br>

[Back to Top](#top)

<br>

<a name="5.1.2"></a>
### 5.1.2 OOD Data Generation

**[ICLR-2018]**
[Training confidence-calibrated classifiers for detecting out-of-distribution samples](https://arxiv.org/abs/1711.09325)
<br>
**Authors:** Kimin Lee, Honglak Lee, Kibok Lee, Jinwoo Shin
<br>
**Institution:** KAIST; University of Michigan, Ann Arbor; Google Brain
> <details>
> <summary>An confidence loss to encourage a uniform prediction of GAN-generated ‘boundary’ OOD samples.</summary>
> <p style="text-align:left">
> It proposes an confidence loss to minimize the KL divergence from the predictive distribution on the GAN-generated OOD samples to the uniform one in order to give less confident predictions on them. The proposed GAN generates ‘boundary’ samples in the in-distribution low-density area.
> </p>
> </details>


**[NeurIPSW-2018]**
[Building robust classifiers through generation of confident out of distribution examples](https://arxiv.org/abs/1812.00239)
<br>
**Authors:** Kumar Sricharan, Ashok Srivastava
<br>
**Institution:** Central Data Science Organization, Intuit Inc


**[NeurIPSW-2019]**
[Out-of-distribution detection in classifiers via generation](https://arxiv.org/abs/1910.04241)
<br>
**Authors:** Sachin Vernekar, Ashish Gaurav, Vahdat Abdelzad, Taylor Denouden, Rick Salay, Krzysztof Czarnecki
<br>
**Institution:** University of Waterloo


**[CVPR-2019]**
[Out-of-distribution detection for generalized zero-shot action recognition](https://arxiv.org/abs/1904.08703)
<br>
**Authors:** Devraj Mandal, Sanath Narayan, Saikumar Dwivedi, Vikram Gupta, Shuaib Ahmed, Fahad Shahbaz Khan, Ling Shao
<br>
**Institution:** Indian Institute of Science, Bangalore; Inception Institute of Artificial Intelligence, UAE; Mercedes-Benz R&D India, Bangalore


**[ICLR-2022]**
[VOS: Learning What You Don't Know By Virtual Outlier Synthesis](https://arxiv.org/abs/2202.01197)
<br>
**Authors:** Xuefeng Du, Zhaoning Wang, Mu Cai, Yixuan Li
<br>
**Institution:** University of Wisconsin - Madison
> <details>
> <summary>A novel framework for OOD detection by adaptively synthesizing virtual outliers that can meaningfully regularize the model's decision boundary during training. </summary>
> <p style="text-align:left">
> VOS samples virtual outliers from the low-likelihood region of the class-conditional distribution estimated in the feature space. VOS achieves strong performance on both object detection and image classification models.
> </p>
> </details>


<br>

[Back to Top](#top)

<br>

<a name="5.1.3"></a>
### 5.1.3 Gradient-based Methods

**[ICLR-2018]**
[Enhancing The Reliability of Out-of-distribution Image Detection in Neural Networks](https://github.com/facebookresearch/odin).
<br>
**Authors:** Shiyu Liang, Yixuan Li, R. Srikant
<br>
**Institution:** University of Illinois at Urbana-Champaign; University of Wisconsin-Madison
> <details>
> <summary> Using temperature scaling on softmax probabilities with small perturbations for robustness.</summary>
> <p style="text-align:left">
> Temperature scaling can calibrate the softmax probabilities so the model takes the calibrated maximum softmax probabilities as the indicator for OOD detection. A perturbation on each sample at test time can further exploit the model robustness in detecting ID samples. However, it requires an OOD validation set for hyperparameter tuning.
> </p>
> </details>

**[NeurIPS-2021]**
[On the Importance of Gradients for Detecting Distributional Shifts in the Wild](https://arxiv.org/abs/2110.00218).
<br>
**Authors:** Rui Huang, Andrew Geng, Yixuan Li
<br>
**Institution:** University of Wisconsin-Madison



<br>

[Back to Top](#top)

<br>


<a name="5.1.4"></a>
### 5.1.4 Bayesian Models

**[ICML-2016]**
[Dropout as a bayesian approximation: Representing model uncertainty in deep learning](http://proceedings.mlr.press/v48/gal16.pdf).
<br>
**Authors:** Yarin Gal , Zoubin Ghahramani
<br>
**Institution:** University of Cambridge



**[NeurIPS-2017]**
[Simple and scalable predictive uncertainty estimation using deep ensembles](https://arxiv.org/pdf/1612.01474.pdf). 
<br>
**Authors:** Balaji Lakshminarayanan , Alexander Pritzel , Charles Blundell
<br>
**Institution:** DeepMind



**[NeurIPS-2018]**
[Predictive Uncertainty Estimation via Prior Networks](https://arxiv.org/pdf/1802.10501.pdf)
<br>
**Authors:** Andrey Malinin, Mark Gales
<br>
**Institution:** University of Cambridge 



**[NeurIPS-2019]**
[Practical deep learning with bayesian principles](https://arxiv.org/pdf/1906.02506.pdf)
<br>
**Authors:** Kazuki Osawa, Siddharth Swaroop, Anirudh Jain, Runa Eschenhagen, Richard E. Turner, Rio Yokota, Mohammad Emtiyaz Khan
<br>
**Institution:** Tokyo Institute of Technology; University of Cambridge; Indian Institute of Technology (ISM); University of Osnabrück; RIKEN Center for AI Project


**[NeurIPS-2019]**
[Reverse kl-divergence training of prior networks: Improved uncertainty and adversarial robustness](https://arxiv.org/pdf/1905.13472.pdf)
<br>
**Authors:** Andrey Malinin, Mark Gales
<br>
**Institution:** Yandex; University of Cambridge



**[NeurIPS-2020]**
[Towards maximizing the representation gap between in-domain & out-of-distribution examples](https://arxiv.org/pdf/2010.10474.pdf)
<br>
**Authors:** Jay Nandy, Wynne Hsu, Mong Li Lee
<br>
**Institution:** National University of Singapore



<br>

[Back to Top](#top)

<br>


<a name="5.1.5"></a>
### 5.1.5 Large-scale OOD Detection

**[CVPR-2021]**
[Mos: Towards scaling out-of-distribution detection for large semantic space](https://openaccess.thecvf.com/content/CVPR2021/papers/Huang_MOS_Towards_Scaling_Out-of-Distribution_Detection_for_Large_Semantic_Space_CVPR_2021_paper.pdf)
<br>
**Authors:** Rui Huang, Yixuan Li
<br>
**Institution:** University of Wisconsin-Madison



**[arXiv-2021]**
[Exploring the limits of out-of-distribution detection](https://arxiv.org/pdf/2106.03004.pdf)
<br>
**Authors:** Stanislav Fort, Jie Ren, Balaji Lakshminarayanan
<br>
**Institution:** Stanford University; Google Research
> <details>
> <summary>Large-scale pre-trained transformers significantly improve near-OOD tasks</summary>
> <p style="text-align:left">
> This work explores the effectiveness of large-scale pre-trained transformers, especially when few-shot outlier exposure is available. It also shows that the pre-trained multi-modal image-text transformers CLIP is also effective on OOD detection if using the names of outlier classes as candidate text labels.
> </p>
> </details>



**[arXiv-2020]**
[Pretrained transformers improve out-of-distribution robustness](https://arxiv.org/pdf/2004.06100.pdf)
<br>
**Authors:** Dan Hendrycks, Xiaoyuan Liu, Eric Wallace, Adam Dziedzic, Rishabh Krishnan, Dawn Song
<br>
**Institution:** UC Berkeley; Shanghai Jiao Tong University; University of Chicago



**[arXiv-2021]**
[Oodformer: Out-of-distribution detection transformer](https://arxiv.org/pdf/2107.08976.pdf)
<br>
**Authors**: Rajat Koner, Poulami Sinhamahapatra, Karsten Roscher, Stephan Günnemann, Volker Tresp 
<br>
**Institution:** Ludwig Maximilian University; Technical University; Fraunhofer, IKS; Siemens AG



<br>

[Back to Top](#top)

<br>

<a name="5.2"></a>
## 5.2 Density-based Methods



**[ICML-2016]**
[Pixel recurrent neural networks](http://proceedings.mlr.press/v48/oord16.pdf)
<br>
**Authors:** Aaron van den Oord, Nal Kalchbrenner, Koray Kavukcuoglu
<br>
**Institution:** Google DeepMind



**[NeurIPS-2018]**
[Generative probabilistic novelty detection with adversarial autoencoders](https://arxiv.org/pdf/1807.02588.pdf)
<br>
**Authors:** Stanislav Pidhorskyi, Ranya Almohsen, Donald A. Adjeroh, Gianfranco Doretto
<br>
**Institution:** West Virginia University



**[NeurIPS-2018]**
[Glow: Generative flow with invertible 1x1 convolutions](https://arxiv.org/pdf/1807.03039.pdf)
<br>
**Authors:** Diederik P. Kingma, Prafulla Dhariwal
<br>
**Institution:** OpenAI




**[ECML/KDD-2018]**
[Image anomaly detection with generative adversarial networks](https://openreview.net/pdf?id=S1EfylZ0Z)
<br>
**Authors:** Lucas Deecke, authorRobert Vandermeulen, Lukas RuffStephan Mandt, Marius Kloft
<br>
**Institution:** University of Edinburgh; TU Kaiserslautern; Hasso Plattner Institute; University of California




**[ICLR-2018]**
[Deep autoencoding gaussian mixture model for unsupervised anomaly detection](https://openreview.net/pdf?id=BJJLHbb0-)
<br>
**Authors:** Bo Zong, Qi Song, Martin Renqiang Min, Wei Cheng, Cristian Lumezanu, Daeki Cho, Haifeng Chen
<br>
**Institution:** NEC Laboratories America; Washington State University

**[NeurIPS-2018]**
[Do deep generative models know what they don’t know?](https://arxiv.org/pdf/1810.09136.pdf)
<br>
**Authors:** Eric Nalisnick, Akihiro Matsukawa, Yee Whye Teh, Dilan Gorur, Balaji Lakshminarayanan
<br>
**Institution:** DeepMind


**[arXiv-2018]**
[Waic, but why? generative ensembles for robust anomaly detection](https://arxiv.org/pdf/1810.01392.pdf)
<br>
**Authors:** Hyunsun Choi, Eric Jang, Alexander A. Alemi
<br>
**Institution:** Google Inc.


**[CVPR-2018]**
[Adversarially learned one-class classifier for novelty detection](https://openaccess.thecvf.com/content_cvpr_2018/papers/Sabokrou_Adversarially_Learned_One-Class_CVPR_2018_paper.pdf)
<br>
**Authors:** Mohammad Sabokrou, Mohammad Khalooei, Mahmood Fathy, Ehsan Adeli
<br>
**Institution:** Institute for Research in Fundamental Sciences; Amirkabir University of Technology; Stanford University



**[NeurIPS-2019]**
[Likelihood ratios for out-of-distribution detection](https://arxiv.org/pdf/1906.02845.pdf)
<br>
**Authors:** Jie Ren, Peter J. Liu, Emily Fertig, Jasper Snoek, Ryan Poplin, Mark A. DePristo, Joshua V. Dillon, Balaji Lakshminarayanan
<br>
**Institution:** Google Research; DeepMind
> <details>
> <summary>Using likelihood ratios to cancel out background influence.</summary>
> <p style="text-align:left">
> This work finds the likelihood score is heavily affected by background, so likelihood ratios are used to cancel out background influence. The Likelihood Ratio (LR) is the likelihood that a given test result would be expected in a patient with the target disorder compared to the likelihood that that same result would be expected in a patient without the target disorder.
> </p>
> </details>


**[CVPR-2019]**
[Latent space autoregression for novelty detection](https://openaccess.thecvf.com/content_CVPR_2019/papers/Abati_Latent_Space_Autoregression_for_Novelty_Detection_CVPR_2019_paper.pdf)
<br>
**Authors:** Davide Abati, Angelo Porrello, Simone Calderara, Rita Cucchiara
<br>
**Institution:** University of Modena and Reggio Emilia



**[CVPR-2020]**
[Deep residual flow for out of distribution detection](?)
<br>
**Authors:** Ev Zisselman, Aviv Tamar
<br>
**Institution:** Technion




**[NeurIPS-2020]**
[Why normalizing flows fail to detect out-of-distribution data](https://arxiv.org/pdf/2006.08545.pdf)
<br>
**Authors:** Polina Kirichenko, Pavel Izmailov, Andrew Gordon Wilson
<br>
**Institution:** New York University




**[ICLR-2020]**
[Input complexity and out-of-distribution detection with likelihood-based generative models](https://arxiv.org/pdf/1909.11480.pdf)
<br>
**Authors:** Joan Serra, David Alvarez, Vicenc¸ Gomez, Olga Slizovskaia, Jose F. Nunez, Jordi Luque
<br>
**Institution:** Dolby Laboratories; Telefonica Research;  Universitat Politecnica de Catalunya; Universitat Pompeu Fabra


**[NeurIPS-2020]**
[Likelihood regret: An out-ofdistribution detection score for variational auto-encoder](https://arxiv.org/pdf/2003.02977.pdf)
<br>
**Authors:** Zhisheng Xiao, Qing Yan, Yali Amit
<br>
**Institution:** University of Chicago


**[TPAMI-2020]**
[Normalizing flows: An introduction and review of current methods](https://arxiv.org/pdf/1908.09257.pdf)
<br>
**Authors:** Ivan Kobyzev, Simon J.D. Prince, Marcus A. Brubaker
<br>
**Institution:** Borealis AI



<br>

[Back to Top](#top)

<br>

<a name="5.3"></a>
## 5.3 Distance-based Methods
**[NeurIPS-2018]**
[A simple unified framework for detecting out-of-distribution samples and adversarial attacks](https://proceedings.neurips.cc/paper/2018/file/abdeb6f575ac5c6676b747bca8d09cc2-Paper.pdf)
<br>
**Authors:** Kimin Lee, Kibok Lee, Honglak Lee, Jinwoo Shin
<br>
**Institution:** Korea Advanced Institute of Science and Technology (KAIST); University of Michigan; Google Brain; AItrics



**[NeurIPS-2019]**
[Likelihood ratios for out-of-distribution detection](https://arxiv.org/pdf/1906.02845.pdf)
<br>
**Authors:** Jie Ren, Peter J. Liu, Emily Fertig, Jasper Snoek, Ryan Poplin, Mark A. DePristo, Joshua V. Dillon, Balaji Lakshminarayanan
<br>
**Institution:** Google Research; DeepMind




**[ACCV-2020]**
[Hyperparameter-free out-of-distribution detection using cosine similarity](https://openaccess.thecvf.com/content/ACCV2020/papers/Techapanurak_Hyperparameter-Free_Out-of-Distribution_Detection_Using_Cosine_Similarity_ACCV_2020_paper.pdf)
<br>
**Authors:** Engkarat Techapanurak, Masanori Suganuma, Takayuki Okatani
<br>
**Institution:** Tohoku University;  RIKEN Center for AIP
> <details>
> <summary> Using scaled cosine similarity between test sample features and class features to determine OOD samples. </summary>
> <p style="text-align:left">
> The first work employs softmax of scaled cosine similarity instead of ordinary softmax of logits. Taking the metric learning idea into OOD detection. It is also the concurrent work of Generalized ODIN.
> </p>
> </details>

**[ECCV-2020]**
[A boundary based out-of-distribution classifier for generalized zero-shot learning](https://arxiv.org/abs/2008.04872)
<br>
**Authors:** Xingyu Chen, Xuguang Lan, Fuchun Sun, Nanning Zheng
<br>
**Institution:** Xian Jiaotong University; Tsinghua University

**[ICML-2020]**
[Uncertainty estimation using a single deep deterministic neural network](https://arxiv.org/abs/2008.04872)
<br>
**Authors:** Joost van Amersfoort, Lewis Smith, Yee Whye Teh, Yarin Gal
<br>
**Institution:** University of Oxford


**[arXiv-2020]**
[Feature Space Singularity for Out-of-Distribution Detection](https://arxiv.org/abs/2011.14654)
<br>
**Authors:** Haiwen Huang, Zhihan Li, Lulu Wang, Sishuo Chen, Bin Dong, Xinyu Zhou
<br>
**Institution:** University of Oxford; Peking University; MEGVII Technology; etc.
> <details>
> <summary> Distance to Feature Space Singularity can measure OOD.</summary>
> <p style="text-align:left">
> It is observed that in feature spaces, OOD samples concentrate near a Feature Space Singularity (FSS) point, and the distance from a sample to FSS measures the degree of OOD. It can be exlained that moving speeds of features of other data depend on their similarity to the training data. During training, they use generated uniform noise or validation data as OOD.
> </p>
> </details>



**[CVPR-2021]**
[Out-of-Distribution Detection Using Union of 1-Dimensional Subspaces](https://openaccess.thecvf.com/content/CVPR2021/papers/Zaeemzadeh_Out-of-Distribution_Detection_Using_Union_of_1-Dimensional_Subspaces_CVPR_2021_paper.pdf)
<br>
**Authors:** Alireza Zaeemzadeh, Niccolò Bisagno, Zeno Sambugaro, Nicola Conci, Nazanin Rahnavard, Mubarak Shah
<br>
**Institution:** University of Central Florida; University of Trento
> <details>
> <summary> Calculating class membership probabilities in a union of 1-dimensional subspaces.</summary>
> <p style="text-align:left">
> The cosine similarities between the extracted feature and the class vectors are used to compute the class membership probabilities, using a Union of 1-dimensional subspaces. The 1-dimensional subspaces is spanned by the first singular vector of the feature vectors extracted from the training set. Feature vectors lie on a union of 1-dimensional subspaces helps OOD samples to be robustly detected.
> </p>
> </details>



**[arXiv-2021]**
[A simple fix to mahalanobis distance for improving near-ood detection](https://arxiv.org/pdf/2106.09022.pdf)
<br>
**Authors:** Jie Ren, Stanislav Fort, Jeremiah Liu, Abhijit Guha Roy, Shreyas Padhy, Balaji Lakshminarayanan
<br>
**Institution:** Google Research; Stanford University; Harvard University; Google Health



<br>

[Back to Top](#top)

<br>

<a name="top"></a>
# 5. OOD Detection
- [5.1 Classfication-based Method](#5.1)
  - [5.1.1 Confidence Calibration](#5.1.1)
    - [5.1.1.1 Post-hoc Calibration](#5.1.1.1)
    - [5.1.1.2 Confidence Enhancement](#5.1.1.2)
    - [5.1.1.3 Outlier Explosure](#5.1.1.3)
  - [5.1.2 OOD Data Generation](#5.1.2)
  - [5.1.3 Gradient-based Methods](#5.1.3)
  - [5.1.4 Bayesian Models](#5.1.4)
  - [5.1.5 Big Pretrained Model](#5.1.5)
- [5.2 Density-based Method](#5.2)
  - [5.2.1 Embedding-based Method](#5.1.1)
  - [5.2.2 Flow-based Methods](#5.1.2)
  - [5.2.3 Energy-based Methods](#5.1.3)
- [5.3 Distance-based Method](#5.3)


<a name="5.1"></a>
## 5.1 Classfication-based Method

<a name="5.1.1"></a>
### 5.1.1 Confidence Calibration
<a name="5.1.1.1"></a>
#### 5.1.1.1 Post-hoc Calibration

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
> <summary> Using temperature scaling on softmax probabilities with small perturbations for robustness.</summary>
> <p style="text-align:left">
> Temperature scaling can calibrate the softmax probabilities so the model takes the calibrated maximum softmax probabilities as the indicator for OOD detection. A perturbation on each sample at test time can further exploit the model robustness in detecting ID samples. However, it requires an OOD validation set for hyperparameter tuning.
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


**[NeurIPS-2021]**
[React: Out-of-distribution detection with rectified activations](http://pages.cs.wisc.edu/~sharonli/).
<br>
**Authors:** Yiyou Sun, Chuan Guo and Yixuan Li
<br>
**Institution:** University of Wisconsin-Madison


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

**[NeurIPS-2018]**
[A Simple Unified Framework for Detecting Out-of-Distribution Samples and Adversarial Attacks](https://arxiv.org/abs/1807.03888).
<br>
**Authors:** Kimin Lee, Kibok Lee, Honglak Lee, Jinwoo Shin
<br>
**Institution:** Korea Advanced Institute of Science and Technology (KAIST); University of Michigan; Google Brain; AItrics


**[NeurIPS-W-2019]**
[Detecting Out-of-Distribution Examples with In-distribution Examples and Gram Matrices](https://arxiv.org/abs/1912.12510).
<br>
**Authors:** Chandramouli Shama Sastry, Sageev Oore
<br>
**Institution:** Dalhousie University, Halifax



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

**[ICML-2020]**
[Detecting Out-of-Distribution Examples with In-distribution Examples and Gram Matrices](https://arxiv.org/abs/1912.12510).
<br>
**Authors:** Chandramouli Shama Sastry, Sageev Oore
<br>
**Institution:** Dalhousie University, Halifax


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


**[ECML PKDD-2021]**
[ATOM: Robustifying Out-of-distribution Detection Using Outlier Mining](https://arxiv.org/abs/2006.15207)
<br>
**Authors:** Jiefeng Chen, Yixuan Li, Xi Wu, Yingyu Liang, Somesh Jha
<br>
**Institution:** University of Wisconsin-Madison;  Google
> <details>
> <summary>Using adversarial training to select auxiliary outlier data for a tight decision boundary between ID and OOD data.</summary>
> <p style="text-align:left">
>By mining informative auxiliary OOD data, one can significantly improve OOD detection performance, and somewhat surprisingly, generalize to unseen adversarial attack. The key idea is to selectively utilize auxiliary outlier data for estimating a tight decision boundary between ID and OOD data, which leads to robust OOD detection performance.
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




<br>

[Back to Top](#top)

<br>

<a name="5.1.3"></a>
### 5.1.3 Gradient-based Methods

**[ICLR-2018]**
[Enhancing The Reliability of Out-of-distribution Image Detection in Neural Networks](https://github.com/facebookresearch/odin).
<br>
**Authors:** Shiyu Liang, Yixuan Li, R.rikant
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

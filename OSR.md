<a name="top"></a>
# 4. Multi-Class Novelty Detection & Open Set Recognition
- [4.1 Classfication-based Method](#4.1)
  - [4.1.1 EVT-based Uncertainty Calibration](#4.1.1): OpenMax
  - [4.1.2 Unknown Class Generation](#4.1.2)
- [4.2 Distance-based Method](#4.2)
- [4.3 Reconstruction-based Method](#4.3)
  - [4.3.1 Sparse Representation Method](#4.3.1)
  - [4.3.2 Reconstruction-Error Method](#4.3.2)
- [4.4 Hybrid Methods and Others](#4.4)


<a name="4.1"></a>
## 4.1 Classfication-based Method

**[TPAMI-2013]**
[Toward Open Set Recognition](https://ieeexplore.ieee.org/abstract/document/6365193)
<br>
**Authors:** Scheirer, Walter J and Jain, Lalit P and Boult, Terrance E
<br>
**Institution:** Harvard University; University of Campinas; University of Colorado, Colorado Springs
> <details>
> <summary>Kicking-off paper using 1-vs-set machine for OSR.</summary>
> <p style="text-align:left">
> This paper highlights the practicality of OSR by showing the difference between classification and recognition: classification only has a given set of classes between which we must discriminate; Recognition has some classes we can recognize in a much larger space of things we do not recognize. The paper shows the validity of 1-class SVM and binary SVM for OSR, and proposes 1-vs-Set SVM to manage the open-set risk by solving a two-plane optimization problem instead of the classic half-space of a binary linear classifier.
> </p>
> </details>

<a name="4.1.1"></a>
### 4.1.1 EVT-based Uncertainty Calibration

**[TPAMI-2014]**
[Probability models for open set recognition](https://ieeexplore.ieee.org/abstract/document/6809169)
<br>
**Authors:** Scheirer, Walter J and Jain, Lalit P and Boult, Terrance E
<br>
**Institution:** Harvard University; University of Colorado, Colorado Springs
> <details>
> <summary>W-SVM using CAP and EVT for score calibration on one-class and binary SVM.</summary>
> <p style="text-align:left">
> CAP explicitly models the probability of class membership abating from ID points to OOD points, as classic probabilistic model lacks the consideration of open space, and EVT exactly focuses on modeling the tailed distribution with extreme high/low values. The novel Weibull-calibrated SVM (W-SVM) algorithm is introduced, combining the useful properties of CAP and EVT.
> </p>
> </details>

**[ECCV-2014]**
[Multi-class open set recognition using probability of inclusion](https://link.springer.com/content/pdf/10.1007/978-3-319-10578-9_26.pdf)
<br>
**Authors:** Jain, Lalit P and Scheirer, Walter J and Boult, Terrance E
<br>
**Institution:** University of Coloradom, Colorado Springs; Harvard University; Securics
> <details>
> <summary>PI-SVM estimating the unnormalized posterior probability of class inclusion.
</summary>
> <p style="text-align:left">
> Modeling positive training data at the decision boundary, where we can invoke the statistical EVT. A new algorithm called the PI-SVM is introduced for estimating the unnormalized posterior probability of multiple class inclusion.
> </p>
> </details>


**[CVPR-2016]**
[Towards open set deep networks](https://www.cv-foundation.org/openaccess/content_cvpr_2016/html/Bendale_Towards_Open_Set_CVPR_2016_paper.html)
<br>
**Authors:** Bendale, Abhijit and Boult, Terrance E
<br>
**Institution:** University of Colorado, Colorado Springs
> <details>
> <summary>OpenMax: Replacing softmax layer with OpenMax and calibrating the confidence to predict novel class.</summary>
> <p style="text-align:left">
> This method uses the scores from the penultimate layer to estimate if the input is “far” from known training data.
> </p>
> </details>


**[BMVC-2017]**
[Adversarial robustness: Softmax versus openmax]()
<br>
**Authors:** Rozsa, Andras and G{\"u}nther, Manuel and Boult, Terrance E
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>


<a name="4.1.2"></a>
### 4.1.2 Unknown Class Generation

**[BMVC-2017]**
[Generative openmax for multi-class open set classification]()
<br>
**Authors:** Ge, ZongYuan and Demyanov, Sergey and Chen, Zetao and Garnavi, Rahil
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ECCV-2018]**
[Open set learning with counterfactual images]()
<br>
**Authors:** Neal, Lawrence and Olson, Matthew and Fern, Xiaoli and Wong, Weng-Keen and Li, Fuxin
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2021]**
[Learning Placeholders for Open-Set Recognition]()
<br>
**Authors:** Zhou, Da-Wei and Ye, Han-Jia and Zhan, De-Chuan
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>


<a name="4.2"></a>
## 4.2 Distance-based Method

**[BMVC-2018]**
[Metric learning for novelty and anomaly detection]()
<br>
**Authors:** Masana, Marc and Ruiz, Idoia and Serrat, Joan and van de Weijer, Joost and Lopez, Antonio M
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2021]**
[Learning Deep Classifiers Consistent With Fine-Grained Novelty Detection]()
<br>
**Authors:** Cheng, Jiacheng and Vasconcelos, Nuno
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2020]**
[Few-shot open-set recognition using meta-learning]()
<br>
**Authors:** Liu, Bo and Kang, Hao and Li, Haoxiang and Hua, Gang and Vasconcelos, Nuno
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ECCV-2020]**
[Learning open set network with discriminative reciprocal points]()
<br>
**Authors:** Chen, Guangyao and Qiao, Limeng and Shi, Yemin and Peng, Peixi and Li, Jia and Huang, Tiejun and Pu, Shiliang and Tian, Yonghong
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Scientific reports-2020]**
[p-oDn: prototype-based open Deep network for open Set Recognition]()
<br>
**Authors:** Shu, Yu and Shi, Yemin and Wang, Yaowei and Huang, Tiejun and Tian, Yonghong
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2021]**
[Few-shot Open-set Recognition by Transformation Consistency]()
<br>
**Authors:** Jeong, Minki and Choi, Seokeon and Kim, Changick
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>


<a name="4.3"></a>
## 4.3 Reconstruction-based Method

<a name="4.3.1"></a>
### 4.3.1 Sparse Representation Method

**[TPAMI-2016]**
[Sparse representation-based open set recognition](https://arxiv.org/abs/1705.02431)
<br>
**Authors:** Zhang, He and Patel, Vishal M
<br>
**Institution:** Rutgers University
> <details>
> <summary>SROSR models the tails of the matched and sum of non-matched reconstruction error distributions.</summary>
> <p style="text-align:left">
> This method model the tail of the above two error distributions using the statistical EVT, and the confidence scores corresponding to the tail distributions of a novel test sample are then fused to determine its identity. Notice that the hidden embedding during reconstruction is regularized by sparsity.
> </p>
> </details>

**[CVPR-2013]**
[Kernel null space methods for novelty detection]()
<br>
**Authors:** Bodesheim, Paul and Freytag, Alexander and Rodner, Erik and Kemmler, Michael and Denzler, Joachim
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>

**[CVPR-2017]**
[Incremental kernel null space discriminant analysis for novelty detection]()
<br>
**Authors:** Liu, Juncheng and Lian, Zhouhui and Wang, Yi and Xiao, Jianguo
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2017]**
[Provable self-representation based outlier detection in a union of subspaces]()
<br>
**Authors:** You, Chong and Robinson, Daniel P and Vidal, Ren{\'e}
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>


<a name="4.3.2"></a>
### 4.3.2 Reconstruction-Error Method

**[CVPR-2019]**
[Classification-reconstruction learning for open-set recognition]()
<br>
**Authors:** Yoshihashi, Ryota and Shao, Wen and Kawakami, Rei and You, Shaodi and Iida, Makoto and Naemura, Takeshi
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[AAAI-2020]**
[Open-Set Recognition with Gaussian Mixture Variational Autoencoders]()
<br>
**Authors:** Cao, Alexander and Luo, Yuan and Klabjan, Diego
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> 
> </p>
> </details>

**[CVPR-2019]**
[C2ae: Class conditioned auto-encoder for open-set recognition]()
<br>
**Authors:** Oza, Poojan and Patel, Vishal M
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> It uses class conditioned auto-encoders and model reconstruction errors using EVT.
> </p>
> </details>

**[CVPR-2020]**
[Conditional gaussian distribution learning for open set recognition]()
<br>
**Authors:** Sun, Xin and Yang, Zhenning and Zhang, Chi and Ling, Keck-Voon and Peng, Guohao
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> It learns conditional Gaussian distributions by forcing different latent features to approximate different Gaussian models, which enables the proposed method to classify known samples as well as reject unknown samples.
> </p>
> </details>

**[CVPR-2021]**
[Counterfactual zero-shot and open-set visual recognition]()
<br>
**Authors:** Yue, Zhongqi and Wang, Tan and Sun, Qianru and Hua, Xian-Sheng and Zhang, Hanwang
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> generates more realistic images to help the model to focus more on semantics.
> </p>
> </details>

<a name="4.4"></a>
### 4.4 Hybrid Method

**[CVPR-2020]**
[Generative-discriminative feature representations for open-set recognition]()
<br>
**Authors:** Perera, Pramuditha and Morariu, Vlad I and Jain, Rajiv and Manjunatha, Varun and Wigington, Curtis and Ordonez, Vicente and Patel, Vishal M
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> It uses self-supervision to make the feature space more descriptive to force open-set samples to separate better from known classes. Second, it augments the input with the representation obtained from the generative model.
> </p>
> </details>

**[ECCV-2020]**
[Open-set adversarial defense]()
<br>
**Authors:** Shao, Rui and Perera, Pramuditha and Yuen, Pong C and Patel, Vishal M
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> First, a decoder is used to ensure that clean images can be reconstructed from the obtained latent features. Then, self-supervision is used to ensure that the latent features are informative enough to carry out an auxiliary task.
> </p>
> </details>

**[ECCV-2020]**
[Representative-Discriminative Learning for Open-set Land Cover Classification of Satellite Imagery]()
<br>
**Authors:** Baghbaderani, Razieh Kaviani and Qu, Ying and Qi, Hairong and Stutts, Craig
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> the transformation from the raw image space to the embedding feature space to apply reconstruction error method and do classification in a transformed abundance space.
> </p>
> </details>

**[ECCV-2020]**
[Hybrid models for open set recognition]()
<br>
**Authors:** Zhang, Hongjie and Li, Ang and Guo, Jie and Guo, Yanwen
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
> It composes of an encoder to encode the input data into a joint embedding space, a classifier to classify samples to inlier classes, and a flow-based density estimator to detect whether a sample belongs to the unknown category.
> </p>
> </details>


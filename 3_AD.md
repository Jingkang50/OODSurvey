 <a name="top"></a>
# 3. Anomaly Detection & One-Class Novelty Detection
- [3.1 Density-based Methods](#3.1)
  - [3.1.1 Classic Density Estimation](#3.1.1)
  - [3.1.2 NN-based Density Estimation](#3.1.2)
  - [3.1.3 Energy-based Models](#3.1.3)
  - [3.1.4 Frequency-based Methods](#3.1.4)
- [3.2 Reconstruction-based Methods](#3.2)
  - [3.2.1 Sparse Representation Methods](#3.2.1)
  - [3.2.2 Reconstruction-Error Methods](#3.2.2)
- [3.3 Classification-based Methods](#3.3)
  - [3.3.1 One-Class Classification](#3.3.1)
  - [3.3.2 Positive-Unlabeled Learning](#3.3.2)
  - [3.3.3 Self-Supervised Learning](#3.3.3)
- [3.4 Distance-based Methods](#3.4)
- [3.5 Gradient-based Methods](#3.5)
- [3.6 Discussion and Theoretical Analysis](#3.6)

<a name="3.1"></a>
## 3.1 Density-based Methods
<a name="3.1.1"></a>
### 3.1.1 Classic Density Estimation ###
**[TPAMI-1998]**
[Parametric model fitting: from inlier characterization to outlier detection](https://ieeexplore.ieee.org/abstract/document/667884)
<br>
**Authors:** Gaudenz Danuser, M. Stricker
<br>
**Institution:** Marine Biological Laboratory; Analytical, and Mathematical Services


**[JESP-2018]**
[Parametric model fitting: from inlier characterization to outlier detection](https://www.sciencedirect.com/science/article/abs/pii/S0022103117302123#!)
<br>
**Authors:** Christophe Leys, Olivier Klein, Yves Dominicy
<br>
**Institution:** Universit¨¦libre de Bruxelles; Ghent University


**[ICML-2000]**
[Anomaly detection over noisy data using learned probability distributions](https://academiccommons.columbia.edu/doi/10.7916/D8C53SKF)
<br>
**Authors:** Eskin Eleazar
<br>
**Institution:** Columbia University


**[ISI-2016]**
[Poisson factorization for peer-based anomaly detection](https://ieeexplore.ieee.org/abstract/document/7745472)
<br>
**Authors:** Melissa Turcotte, Juston Moore, Nick Heard, Aaron McPhall
<br>
**Institution:** Los Alamos National Laboratory; University of Bristol


**[JASA-1991]**
[Review papers: Recent developments in non-parametric density estimation](https://www.tandfonline.com/doi/abs/10.1080/01621459.1991.10475021)
<br>
**Authors:** Alan Julian Izenman
<br>
**Institution:** Temple University


**[TKDE-2018]**
[Anomaly detection using local kernel density estimation and context-based regression](https://ieeexplore.ieee.org/abstract/document/8540843)
<br>
**Authors:** Weiming Hu, Jun Gao, Bing Li, Ou Wu, Junping Du, Stephen Maybank
<br>
**Institution:** Chinese Academy of Sciences; University of Chinese Academy of Sciences; Tianjin University; Birkbeck College


<br>

[Back to Top](#top)

<br>

<a name="3.1.2"></a>
### 3.1.2 NN-based Density Est. ###
**[ICLR-2018]**
[Deep autoencoding gaussian mixture model for Deep autoencoding gaussian mixture model for unsupervised anomaly detection](https://openreview.net/forum?id=BJJLHbb0-)
<br>
**Authors:** Bo Zong, Qi Song, Martin Renqiang Min, Wei Cheng, Cristian Lumezanu, Daeki Cho, Haifeng Chen
<br>
**Institution:** Washington State University; NEC Laboratories America



**[CVPR-2019]**
[Latent Space Autoregression for Novelty Detection](https://openaccess.thecvf.com/content_CVPR_2019/html/Abati_Latent_Space_Autoregression_for_Novelty_Detection_CVPR_2019_paper.html)
<br>
**Authors:** Davide Abati, Angelo Porrello, Simone Calderara, Rita Cucchiara
<br>
**Institution:** University of Modena and Reggio Emilia

**[NeurIPS-2018]**
[Generative probabilistic novelty detection with adversarial autoencoders](https://arxiv.org/abs/1807.02588)
<br>
**Authors:** Stanislav Pidhorskyi, Ranya Almohsen, Donald A Adjeroh, Gianfranco Doretto
<br>
**Institution:** West Virginia University


**[ECMLPKDD-2018]**
[Image anomaly detection with generative adversarial networks](https://link.springer.com/chapter/10.1007/978-3-030-10925-7_1)
<br>
**Authors:** Lucas Deecke, Robert VandermeulenLukas, RuffStephan Mandt, Marius Kloft
<br>
**Institution:** University of EdinburghEdinburghScotland; TU Kaiserslautern; Hasso Plattner Institute; University of California


**[ICML-2015]**
[Variational inference with normalizing flows](http://proceedings.mlr.press/v37/rezende15.html)
<br>
**Authors:** Danilo Rezende, Shakir Mohamed
<br>
**Institution:** Google DeepMind
>

**[TPAMI-2020]**
[Normalizing flows: An introduction and review of current methods](https://ieeexplore.ieee.org/abstract/document/9089305)
<br>
**Authors:** Ivan Kobyzev, Simon J.D. Prince, Marcus A. Brubaker
<br>
**Institution:** Borealis AI


**[CVPR-2021]**
[Cutpaste: Self-supervised learning for anomaly detection and localization](https://openaccess.thecvf.com/content/CVPR2021/html/Li_CutPaste_SelfSupervised_Learning_for_Anomaly_Detection_and_Localization_CVPR_2021_paper.html)
<br>
**Authors:** Chun-Liang Li, Kihyuk Sohn, Jinsung Yoon, Tomas Pfister
<br>
**Institution:** Google Cloud AI Research


**[CVPR-2021]**
[Multiresolution knowledge distillation for anomaly detection](https://openaccess.thecvf.com/content/CVPR2021/html/Salehi_Multiresolution_Knowledge_Distillation_for_Anomaly_Detection_CVPR_2021_paper.html)
<br>
**Authors:** Mohammadreza Salehi, Niousha Sadjadi, Soroosh Baselizadeh, Mohammad H. Rohban, Hamid R. Rabiee
<br>
**Institution:** Sharif University of Technology


**[NeurIPS-2018]**
[A loss framework for calibrated anomaly detection](https://proceedings.neurips.cc/paper/2018/file/959a557f5f6beb411fd954f3f34b21c3-Paper.pdf)
<br>
**Authors:** Aditya Krishna Menon, Robert C. Williamson
<br>
**Institution:** Australian National University


**[CVPR-2021]**
[Multiattentional deepfake detection](https://openaccess.thecvf.com/content/CVPR2021/html/Zhao_Multi-Attentional_Deepfake_Detection_CVPR_2021_paper.html)
<br>
**Authors:** Hanqing Zhao, Wenbo Zhou, Dongdong Chen, Tianyi Wei, Weiming Zhang, Nenghai Yu
<br>
**Institution:** University of Science and Technology of China; Microsoft Cloud AI

**[AAAI-2020]**
[Ml-loo:Detecting adversarial examples with feature attribution](https://ojs.aaai.org/index.php/AAAI/article/view/6140)
<br>
**Authors:** Puyudi Yang, Jianbo Chen, Cho-Jui Hsieh, Jane-Ling Wang, Michael Jordan
<br>
**Institution:** University of California


**[CIKM-2020]**
[Towards generalizable deepfake detection with locality-aware autoencoder](https://dl.acm.org/doi/abs/10.1145/3340531.3411892)
<br>
**Authors:** Mengnan Du, Shiva Pentyala, Yuening Li, Xia Hu
<br>
**Institution:** Texas A&M University


<br>

[Back to Top](#top)

<br>


<a name="3.1.3"></a>
### 3.1.3 Energy-based Models ###
**[ICML-2016]**
[Deep structured energy based models for anomaly detection](http://proceedings.mlr.press/v48/zhai16.html)
<br>
**Authors:** Shuangfei Zhai, Yu Cheng, Weining Lu, Zhongfei Zhang
<br>
**Institution:** Binghamton Univeristy; IBM T. J. Watson Research Center; Tsinghua University


**[2005]**
[Estimation of non-normalized statistical models by score matching](https://www.jmlr.org/papers/volume6/hyvarinen05a/hyvarinen05a.pdf)
<br>
**Authors:** Aapo Hyv¡§arinen 
<br>
**Institution:** BHelsinki Institute for Information Technology

**[ICML-2011]**
[Bayesian learning via stochastic gradient langevin dynamics](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.441.3813&rep=rep1&type=pdf)
<br>
**Authors:** Max Welling, Yee Whye Teh 
<br>
**Institution:** University of California; UCL

<br>

[Back to Top](#top)

<br>

<a name="3.1.4"></a>
### 3.1.4 Frequency-based Models ###

**[CVPR-2020]**
[High-frequency component helps explain the generalization of convolutional neural networks](https://openaccess.thecvf.com/content_CVPR_2020/html/Wang_High-Frequency_Component_Helps_Explain_the_Generalization_of_Convolutional_Neural_Networks_CVPR_2020_paper.html)
<br>
**Authors:** Haohan Wang, Xindi Wu, Zeyi Huang, Eric P. Xing 
<br>
**Institution:** UCarnegie Mellon University

**[CNeurIPS-2019]**
[Adversarial examples are not bugs, they are features](https://arxiv.org/abs/1905.02175)
<br>
**Authors:** Andrew Ilyas, Shibani Santurkar, Dimitris Tsipras, Logan Engstrom, Brandon Tran, Aleksander Madry
<br>
**Institution:** MIT


**[ICCV-2021]**
[Amplitudephase recombination: Rethinking robustness of convolutional neural networks in frequency domain](https://openaccess.thecvf.com/content/ICCV2021/html/Chen_AmplitudePhase_Recombination_Rethinking_Robustness_of_Convolutional_Neural_Networks_in_Frequency_ICCV_2021_paper.html)
<br>
**Authors:** Guangyao Chen, Peixi Peng, Li Ma, Jia Li, Lin Du, Yonghong Tian
<br>
**Institution:** Peking University; Beihang University; AI Application Research Center Huawei

**[CVPR-2021]**
[Spatial-phase shallow learning: rethinking face forgery detection in frequency domain](https://openaccess.thecvf.com/content/CVPR2021/html/Liu_Spatial-Phase_Shallow_Learning_Rethinking_Face_Forgery_Detection_in_Frequency_Domain_CVPR_2021_paper.html)
<br>
**Authors:** Honggu Liu, Xiaodan Li, Wenbo Zhou, Yuefeng Chen, Yuan He, Hui Xue, Weiming Zhang, Nenghai Yu
<br>
**Institution:** University of Science and Technology of China; Alibaba Group


<br>

[Back to Top](#top)

<br>

<a name="3.2"></a>
## 3.2 Reconstruction-based Methods

<a name="3.2.1"></a>
### 3.2.1 Sparse Representation

[//]: 106
**[J. Signal Process. Syst.-2015]**
[Sparse coding with anomaly detection](https://link.springer.com/article/10.1007/s11265-014-0913-0).
<br>
**Authors:** Amir Adler, Michael Elad, Yacov Hel-Or, Ehud Rivlin 
<br>
**Institution:** Technion
 

[//]: 107
**[Multimedia Tools and Applications-2017]**
[Anomaly detection using sparse reconstruction in crowded scenes](https://link.springer.com/article/10.1007/s11042-016-4115-6).
<br>
**Authors:** Ang Li, Zhenjiang Miao, Yigang Cen, Yi Cen 
<br>
**Institution:** Beijing Jiaotong University, Beijing Key Laboratory, Minzu University of China
 

[//]: 108
**[IEEE-2014]**
[Adaptive Sparse Representations for Video Anomaly Detection](https://ieeexplore.ieee.org/abstract/document/6587741).
<br>
**Authors:** Xuan Mo, Vishal Monga, Raja Bala, Zhigang Fan
<br>
**Institution:** Pennsylvania State University
 

[//]: 109
**[Pattern Recognition-2013]**
[AticleL1 norm based kpca for novelty detection](https://www.sciencedirect.com/science/article/pii/S0031320312002877).
<br>
**Authors:** Yingchao Xiao, Huangang Wanga, Wenli Xu, Junwu Zhou
<br>
**Institution:** Tsinghua University, Beijing General Research Institute of Mining & Metallurgy
 

[//]: 110
**[AAAI-2021]**
[Lren: Low-rank embedded network for sample-free hyperspectral anomaly detection](https://www.aaai.org/AAAI21Papers/AAAI-766.JiangK.pdf).
<br>
**Authors:** Kai Jiang, Weiying Xie, Jie Lei, Tao Jiang, Yunsong Li
<br>
**Institution:** Xidian University


<br>

[Back to Top](#top)

<br>
 

<a name="3.2.2"></a>
### 3.2.2 Reconstruction-Error Methods

[//]:89
**[NeurIPS-2018]**
[Generative probabilistic novelty detection with adversarial autoencoders](https://arxiv.org/abs/1807.02588).
<br>
**Authors:** Stanislav Pidhorskyi, Ranya Almohsen, Donald A Adjeroh, Gianfranco Doretto
<br>
**Institution:** West Virginia University
 

[//]: 111
**[Wireless Telecommunications Symposium-2018]**
[Autoencoderbased network anomaly detection](https://ieeexplore.ieee.org/abstract/document/8363930).
<br>
**Authors:** Zhaomin Chen, Chai Kiat Yeo, Bu Sung Lee, Chiew Tong Lau
<br>
**Institution:** Nanyang Technological University
 

[//]: 112
**[Special Lecture on IE-2015]**
[Variational autoencoder based anomaly detection using reconstruction probability](http://dm.snu.ac.kr/static/docs/TR/SNUDM-TR-2015-03.pdf).
<br>
**Authors:** J. An and S. Cho
<br>
**Institution:** cannot open
 

[//]: 113
**[ICLR-W-2018]**
[Efficient GAN-Based Anomaly Detection](https://arxiv.org/abs/1802.06222).
<br>
**Authors:** Houssam Zenati, Chuan Sheng Foo, Bruno Lecouat, Gaurav Manek, Vijay Ramaseshan Chandrasekhar
<br>
**Institution:** CentraleSup¡äelec, Nanyang Technological University, Carnegie Mellon University, Institute for Infocomm Research
 

[//]: 114
**[CVPR-2018]**
[Future frame prediction for anomaly detection¨Ca new baseline](http://openaccess.thecvf.com/content_cvpr_2018/html/Liu_Future_Frame_Prediction_CVPR_2018_paper.html).
<br>
**Authors:** Wen Liu, Weixin Luo, Dongze Lian, Shenghua Gao
<br>
**Institution:** ShanghaiTech University
 

[//]: 115
**[CVPR-2019]**
[Memorizing normality to detect anomaly: Memory-augmented deep autoencoder for unsupervised anomaly detection](https://openaccess.thecvf.com/content_ICCV_2019/html/Gong_Memorizing_Normality_to_Detect_Anomaly_Memory-Augmented_Deep_Autoencoder_for_Unsupervised_ICCV_2019_paper.html).
<br>
**Authors:** Dong Gong, Lingqiao Liu, Vuong Le, Budhaditya Saha, Moussa Reda Mansour, Svetha Venkatesh, Anton van den Hengel
<br>
**Institution:** University of Adelaide, Deakin University, University of Western Australia
 

[//]: 116
**[CVPR-2020]**
[Learning Memory Guided Normality for Anomaly Detection](https://arxiv.org/abs/2101.12382).
<br>
**Authors:** Kevin Stephen, Varun Menon
<br>
**Institution:** Department of Information Technology, Pune Institute of Computer Technology, New York University

 

[//]: 117
**[ICLR-2020]**
[Robust subspace recovery layer for unsupervised anomaly detection](https://arxiv.org/abs/1904.00152).
<br>
**Authors:** Chieh-Hsin Lai, Dongmian Zou, Gilad Lerman
<br>
**Institution:** School of Mathematics University of Minnesota
 

[//]: 118
**[AAAI-2021]**
[Learning semantic context from normal samples for unsupervised anomaly detection](https://www.aaai.org/AAAI21Papers/AAAI-4221.YanX.pdf).
<br>
**Authors:** Xudong Yan, Huaidong Zhang, Xuemiao Xu1, Xiaowei Hu, Pheng-Ann Heng
<br>
**Institution:** South China University of Technology, Ministry of Education Key Laboratory of Big Data and Intelligent Robot, Guangdong Provincial Key Lab of Computational Intelligence and Cyberspace Information
 

[//]: 119
**[ICML-2019]**
[Anomaly detection with multiple-hypotheses predictions](http://proceedings.mlr.press/v97/nguyen19b.html).
<br>
**Authors:** Duc Tam Nguyen, Zhongyu Lou, Michael Klar, Thomas Brox
<br>
**Institution:** University of Freiburg,  Germany Corporate Research
 

[//]: 120
**[AAAI-2019]**
[Learning competitive and discriminative reconstructions for anomaly detection](https://ojs.aaai.org/index.php/AAAI/article/view/4451).
<br>
**Authors:** Kai Tian, Shuigeng Zhou, Jianping Fan, Jihong Guan
<br>
**Institution:** Fudan University, University of North Carolina at Charlotte, Tongji University
 

[//]: 121
**[CVPR-2018]**
[Adversarially learned one-class classifier for novelty detection](https://openaccess.thecvf.com/content_cvpr_2018/html/Sabokrou_Adversarially_Learned_One-Class_CVPR_2018_paper.html).
<br>
**Authors:** Mohammad Sabokrou, Mohammad Khalooei, Mahmood Fathy, Ehsan Adeli
<br>
**Institution:** Institute for Research in Fundamental Sciences, Amirkabir University of Technology, Stanford University
 


[//]: 122
**[IEEE/CVF-2019]**
[Ocgan: One-class novelty detection using gans with constrained latent representations](http://openaccess.thecvf.com/content_CVPR_2019/html/Perera_OCGAN_One-Class_Novelty_Detection_Using_GANs_With_Constrained_Latent_Representations_CVPR_2019_paper.html).
<br>
**Authors:** Pramuditha Perera, Ramesh Nallapati, Bing Xiang
<br>
**Institution:** Johns Hopkins University, AWS AI
 


[//]: 123
**[ECCV-2020]**
[Encoding structure-texture relation with p-net for anomaly detection in retinal images](https://arxiv.org/pdf/2008.03632).
<br>
**Authors:** Kang Zhou, Yuting Xiao, Jianlong Yang, Jun Cheng, Wen Liu, Weixin Luo, Zaiwang Gu, Jiang Liu, Shenghua Gao
<br>
**Institution:** ShanghaiTech University, Chinese Academy of Sciences, Southern University, Shanghai Engineering Research Center of Intelligent Vision and Imaging
 


[//]: 124
**[arXiv preprint arXiv-2020]**
[Gan ensemble for anomaly detection](https://www.aaai.org/AAAI21Papers/AAAI-1883.HanX.pdf).
<br>
**Authors:** Xu Han, Xiaohui Chen, Li-Ping Liu
<br>
**Institution:** Tufts University


<br>

[Back to Top](#top)

<br>


<a name="3.3"></a>
## 3.1 Classification-based Methods
<a name="3.3.1"></a>
### 3.3.1 One-Class Classification
**[Journal of Artificial Intelligence Research-2002]**
[One-class classification: Concept learning in the absence of counter-examples.](https://elibrary.ru/item.asp?id=5230402)
<br>
**Authors:** Tax, David Martinus Johannes
<br>
**Institution:** TU Delft



**[ICML-2018]**
[Deep one-class classification](http://proceedings.mlr.press/v80/ruff18a)
<br>
**Authors:** Ruff, Lukas and Vandermeulen, Robert and Goernitz, Nico and Deecke, Lucas and Siddiqui, Shoaib Ahmed and Binder, Alexander and Muller, Emmanuel and Kloft, Marius
<br>
**Institution:** Humboldt University of Berlin; Hasso Plattner Institute; TU Kaiserslautern; TU Berlin; University of Edinburgh; Singapore University of Technology and Design


**[CVPR-2021]**
[PANDA: Adapting Pretrained Features for Anomaly Detection and Segmentation](https://openaccess.thecvf.com/content/CVPR2021/html/Reiss_PANDA_Adapting_Pretrained_Features_for_Anomaly_Detection_and_Segmentation_CVPR_2021_paper.html)
<br>
**Authors:** Reiss, Tal and Cohen, Niv and Bergman, Liron and Hoshen, Yedid
<br>
**Institution:** The Hebrew University of Jerusalem


**[CVPR-2019]**
[Gods: Generalized one-class discriminative subspaces for anomaly detection](https://openaccess.thecvf.com/content_ICCV_2019/html/Wang_GODS_Generalized_One-Class_Discriminative_Subspaces_for_Anomaly_Detection_ICCV_2019_paper.html)
<br>
**Authors:** Wang, Jue and Cherian, Anoop
<br>
**Institution:** Australian National University; Mitsubishi Electric Research Labs


<br>

[Back to Top](#top)

<br>


<a name="3.3.2"></a>
### 3.3.2 Positive-Unlabeled Learning
**[Machine Learning-2020]**
[Learning from positive and unlabeled data: A survey](https://link.springer.com/article/10.1007/s10994-020-05877-5)
<br>
**Authors:** Bekker, Jessa and Davis, Jesse
<br>
**Institution:** KU Leuven


**[International Symposiums on Information Processing-2008]**
[Learning from positive and unlabeled examples: A survey](https://ieeexplore.ieee.org/abstract/document/4554167)
<br>
**Authors:** Zhang, Bangzuo and Zuo, Wanli
<br>
**Institution:** Jilin University; Northeast Normal University


**[International Conference on Information, Intelligence, Systems and Applications-2019]**
[Positive and unlabeled learning algorithms and applications: A survey](https://ieeexplore.ieee.org/abstract/document/8900698)
<br>
**Authors:** Jaskie, Kristen and Spanias, Andreas
<br>
**Institution:** Arizona State University



**[IJCAI-2003]**
[Learning to classify texts using positive and unlabeled data](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.91.9914&rep=rep1&type=pdf)
<br>
**Authors:** Li, Xiaoli and Liu, Bing
<br>
**Institution:** National University of Singapore; University of Illinois at Chicago 


**[Bioinformatics-2006]**
[PSoL: a positive sample only learning algorithm for finding non-coding RNA genes](https://academic.oup.com/bioinformatics/article/22/21/2590/250725?login=true)
<br>
**Authors:** Wang, Chunlin and Ding, Chris and Meraz, Richard F and Holbrook, Stephen R
<br>
**Institution:** Lawrence Berkeley National Laboratory


**[ICONIP-2012]**
[Learning from positive and unlabelled examples using maximum margin clustering](https://link.springer.com/chapter/10.1007/978-3-642-34487-9_56)
<br>
**Authors:** Chaudhari, Sneha and Shevade, Shirish
<br>
**Institution:** IBM Research; Indian Institute of Science


**[Journal of Computers-2009]**
[Reliable Negative Extracting Based on kNN for Learning from Positive and Unlabeled Examples.](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.415.7161&rep=rep1&type=pdf)
<br>
**Authors:** Zhang, Bangzuo and Zuo, Wanli
<br>
**Institution:** Jilin University; Northeast Normal University


**[Journal of Information Science and Engineering-2014]**
[Clustering-based Method for Positive and Unlabeled Text Categorization Enhanced by Improved TFIDF.](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.684.162&rep=rep1&type=pdf)
<br>
**Authors:** Liu, Lu and Peng, Tao
<br>
**Institution:** University of Illinois at Urbana-Champaign Urbana; Jilin University


**[arXiv-2018]**
[Instance-dependent pu learning by bayesian optimal relabeling](https://arxiv.org/abs/1808.02180)
<br>
**Authors:** He, Fengxiang and Liu, Tongliang and Webb, Geoffrey I and Tao, Dacheng
<br>
**Institution:** University of Sydney


**[AAAI-2019]**
[Learning competitive and discriminative reconstructions for anomaly detection](https://ojs.aaai.org/index.php/AAAI/article/view/4451)
<br>
**Authors:** Tian, Kai and Zhou, Shuigeng and Fan, Jianping and Guan, Jihong
<br>
**Institution:** Fudan University; University of North Carolina; Tongji University


**[CVPR-2019]**
[Graph convolutional label noise cleaner: Train a plug-and-play action classifier for anomaly detection](https://openaccess.thecvf.com/content_CVPR_2019/html/Zhong_Graph_Convolutional_Label_Noise_Cleaner_Train_a_Plug-And-Play_Action_Classifier_CVPR_2019_paper.html)
<br>
**Authors:** Zhong, Jia-Xing and Li, Nannan and Kong, Weijie and Liu, Shan and Li, Thomas H and Li, Ge
<br>
**Institution:** Peking University


**[ICML-2015]**
[Learning from corrupted binary labels via class-probability estimation](http://proceedings.mlr.press/v37/menon15.html)
<br>
**Authors:** Menon, Aditya and Van Rooyen, Brendan and Ong, Cheng Soon and Williamson, Bob
<br>
**Institution:** National ICT Australia; The Australian National University


**[Artificial Intelligence and Statistics-2015]**
[A rate of convergence for mixture proportion estimation, with application to learning from noisy labels](http://proceedings.mlr.press/v38/scott15.html)
<br>
**Authors:** Scott, Clayton
<br>
**Institution:** University of Michigan

<br>

[Back to Top](#top)

<br>

<a name="3.3.3"></a>
### 3.3.3 Self-Supervised Learning
**[ICDM-2008]**
[Isolation forest](https://ieeexplore.ieee.org/abstract/document/4781136)
<br>
**Authors:** Liu, Fei Tony and Ting, Kai Ming and Zhou, Zhi-Hua
<br>
**Institution:** Monash University; Nanjing University


**[NeurIPS-2018]**
[Deep anomaly detection using geometric transformations](https://arxiv.org/abs/1805.10917)
<br>
**Authors:** Golan, Izhak and El-Yaniv, Ran
<br>
**Institution:**  Israel Institute of Technology


**[ICLR-2020]**
[Classification-based anomaly detection for general data](https://arxiv.org/abs/2005.02359)
<br>
**Authors:** Bergman, Liron and Hoshen, Yedid
<br>
**Institution:** The Hebrew University of Jerusalem


**[NeurIPS-2020]**
[Csi: Novelty detection via contrastive learning on distributionally shifted instances](https://arxiv.org/abs/2007.08176)
<br>
**Authors:** Tack, Jihoon and Mo, Sangwoo and Jeong, Jongheon and Shin, Jinwoo
<br>
**Institution:** KAIST



**[CVPR-2021]**
[Anomaly detection in video via self-supervised and multi-task learning](https://openaccess.thecvf.com/content/CVPR2021/html/Georgescu_Anomaly_Detection_in_Video_via_Self-Supervised_and_Multi-Task_Learning_CVPR_2021_paper.html)
<br>
**Authors:** Georgescu, Mariana-Iuliana and Barbalau, Antonio and Ionescu, Radu Tudor and Khan, Fahad Shahbaz and Popescu, Marius and Shah, Mubarak
<br>
**Institution:** University of Bucharest; Abu Dhabi; SecurifAI; University of Central Florida


**[CVPR-2019]**
[Object-centric auto-encoders and dummy anomalies for abnormal event detection in video](https://openaccess.thecvf.com/content_CVPR_2019/html/Ionescu_Object-Centric_Auto-Encoders_and_Dummy_Anomalies_for_Abnormal_Event_Detection_in_CVPR_2019_paper.html)
<br>
**Authors:** Ionescu, Radu Tudor and Khan, Fahad Shahbaz and Georgescu, Mariana-Iuliana and Shao, Ling
<br>
**Institution:** IIAI; University of Bucharest; SecurifAI

<br>

[Back to Top](#top)

<br>

<a name="3.4"></a>
## 3.4 Distance-based Methods 

**[PHM Society European Conference, 2014]**
[Anomaly detection using self-organizing maps-based k-nearest neighbor algorithm](https://papers.phmsociety.org/index.php/phme/article/download/1554/522)
<br>
**Authors:** J. Tian, M. H. Azarian, and M. Pecht
<br>
**Institution:**  Center for Advanced Life Cycle Engineering (CALCE), University of Maryland, College Park, MD, 20742, U.S.A.


**[GI/ITG Workshop MMBnet, pp. 13¨C14, 2007]**
[Traffic anomaly detection using k-means clustering](https://www.net.in.tum.de/projects/dfg-lupus/files/muenz07k-means.pdf)
<br>
**Authors:** G. Munz, S. Li, and G. Carle
<br>
**Institution:** Wilhelm Schickard Institute for Computer Science; University of Tuebingen, Germany


**[International conference on networked digital technologies, pp. 135¨C145, Springer,2012]**
[Unsupervised clustering approach for network anomaly detection](https://eprints.soton.ac.uk/338221/1/Unsupervised_Clustering_and_Outlier_Detection_approach_for_network_anomaly_detection_-_camera_ready_new.pdf)
<br>
**Authors:** I. Syarif, A. Prugel-Bennett, and G. Wills
<br>
**Institution:**  School of Electronics and Computer Science, University of Southampton, UK; Eletronics Engineering Polytechnics Institute of Surabaya, Indonesia 


<a name="3.5"></a>
## 3.5 Gradient-based Methods

**[ECCV-2020]**
[Back-propagated gradient representations for anomaly detection](https://arxiv.org/pdf/2007.09507)
<br>
**Authors:** G. Kwon, M. Prabhushankar, D. Temel, and G. AlRegib
<br>
**Institution:** Georgia Institute of Technology, Atlanta, GA 30332, USA



<a name="3.6"></a>
## 3.6 Discussion and Theoretical Analysis

**[ICML-2018]**
[Open category detection with pac guarantees](http://proceedings.mlr.press/v80/liu18e/liu18e.pdf)
<br>
**Authors:** S. Liu, R. Garrepalli, T. Dietterich, A. Fern, and D. Hendrycks
<br>
**Institution:** Department of Statistics, Oregon State University, Oregn, USA School of EECS, Oregon State University, Oregon, USA University of California, Berkeley, California USA

**[ICML-2021]**
[Learning bounds for open-set learning](http://proceedings.mlr.press/v139/fang21c/fang21c.pdf)
<br>
**Authors:** Z. Fang, J. Lu, A. Liu, F. Liu, and G. Zhang
<br>
**Institution:** AAII, University of Technology Sydney.  

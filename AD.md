 <a name="top"></a>
# 3. Anomaly Detection & One-Class Novelty Detection
- [3.1 Density-based Method](#3.1)
  - [3.1.1 Classic Density Estimation](#3.1.1)
  - [3.1.2 NN-based Density Estimation](#3.1.2)
  - [3.1.3 Energy-based Model](#3.1.3)
- [3.2 Reconstruction-based Method](#3.2)
  - [3.2.1 Sparse Representation Method](#3.2.1)
  - [3.2.2 Reconstruction-Error Method](#3.2.2)
- [3.3 Classification-based Method](#3.3)
  - [3.3.1 One-Class Classification](#3.3.1)
  - [3.3.2 Positive-Unlabeled Learning](#3.3.2)
  - [3.3.3 Self-Supervised Learning](#3.3.3)
- [3.4 Distance-based Method](#3.4)
- [3.5 Meta-Learning-based Method](#3.5)
- [3.6 Hybrid Methods and Others](#3.6)



%% AD Method

**[AAAI-2020]**
[Detecting semantic anomalies]()
<br>
**Authors:** Ahmed, Faruk and Courville, Aaron
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%% AD Probabilistic Model %%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%%% Density Estimation %%%%%%%%%%%%

%%%% parametric %

**[TPAMI-1998]**
[Parametric model fitting: From inlier characterization to outlier detection]()
<br>
**Authors:** Danuser, Gaudenz and Stricker, Markus
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%% - mahalanobis -

**[Chemometrics and intelligent laboratory systems-2000]**
[The mahalanobis distance]()
<br>
**Authors:** De Maesschalck, Roy and Jouan-Rimbaud, Delphine and Massart, D{\'e}sir{\'e} L
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Journal of Experimental Social Psychology-2018]**
[Detecting multivariate outliers: Use a robust variant of the Mahalanobis distance]()
<br>
**Authors:** Leys, Christophe and Klein, Olivier and Dominicy, Yves and Ley, Christophe
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%% - GMM -

**[SIAM review-1984]**
[Mixture densities, maximum likelihood and the EM algorithm]()
<br>
**Authors:** Redner, Richard A and Walker, Homer F
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICML-2000]**
[Anomaly detection over noisy data using learned probability distributions]()
<br>
**Authors:** Eskin, Eleazar
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%% - Poisson -

**[IEEE Conference on Intelligence and Security Informatics (ISI)-2016]**
[Poisson factorization for peer-based anomaly detection]()
<br>
**Authors:** Turcotte, Melissa and Moore, Juston and Heard, Nick and McPhall, Aaron
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%% non-parametric %

**[Journal of the american statistical association-1991]**
[Review papers: Recent developments in nonparametric density estimation]()
<br>
**Authors:** Izenman, Alan Julian
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%% - histogram -

**[Communications in Statistics-Theory and Methods-1973]**
[A histogram method of density estimation]()
<br>
**Authors:** Van Ryzin, J
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICTSPCC-2012]**
[Histogram-based online anomaly detection in hierarchical wireless sensor networks]()
<br>
**Authors:** Xie, Miao and Hu, Jiankun and Tian, Biming
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[IEEE Transactions on Network and Service Management-2009]**
[Histogram-based traffic anomaly detection]()
<br>
**Authors:** Kind, Andreas and Stoecklin, Marc Ph and Dimitropoulos, Xenofontas
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[KI-2012: Poster and Demo Track-2012]**
[Histogram-based outlier score (hbos): A fast unsupervised anomaly detection algorithm]()
<br>
**Authors:** Goldstein, Markus and Dengel, Andreas
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%% - kde -

**[The annals of mathematical statistics-1962]**
[On estimation of a probability density function and mode]()
<br>
**Authors:** Parzen, Emanuel
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Proceedings of the institution of mechanical engineers-1998]**
[Applications of probability density estimation to the detection of abnormal conditions in engineering]()
<br>
**Authors:** Desforges, MJ and Jacob, PJ and Cooper, JE
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[TKDE-2018]**
[Anomaly detection using local kernel density estimation and context-based regression]()
<br>
**Authors:** Hu, Weiming and Gao, Jun and Li, Bing and Wu, Ou and Du, Junping and Maybank, Stephen
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%% old application

**[IEE proceedings C (generation, transmission and distribution)-1982]**
[Dynamic state estimation including anomaly detection and identification for power systems]()
<br>
**Authors:** Nishiya, K and Hasegawa, J and Koike, T
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[IEEE Transactions on software engineering-1993]**
[Statistical foundations of audit trail analysis for the detection of computer misuse]()
<br>
**Authors:** Helman, Paul and Liepins, Gunar
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Computer networks-2007]**
[An overview of anomaly detection techniques: Existing solutions and latest technological trends]()
<br>
**Authors:** Patcha, Animesh and Park, Jung-Min
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2010]**
[Chaotic invariants of lagrangian particle trajectories for anomaly detection in crowded scenes]()
<br>
**Authors:** Wu, Shandong and Moore, Brian E and Shah, Mubarak
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Journal of Computational and Graphical Statistics-2020]**
[Anomaly detection in high-dimensional data]()
<br>
**Authors:** Talagala, Priyanga Dilini and Hyndman, Rob J and Smith-Miles, Kate
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%% Deep Density Estimation %%%%%%%%%%%%

**[ICLR-2018]**
[Deep autoencoding gaussian mixture model for unsupervised anomaly detection]()
<br>
**Authors:** Zong, Bo and Song, Qi and Min, Martin Renqiang and Cheng, Wei and Lumezanu, Cristian and Cho, Daeki and Chen, Haifeng
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%%% - AE -

**[AIChE journal-1991]**
[Nonlinear principal component analysis using autoassociative neural networks]()
<br>
**Authors:** Kramer, Mark A
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%%% - VAE -

**[arXiv-2013]**
[Auto-encoding variational bayes](https://arxiv.org/abs/1312.6114)
<br>
**Authors:** Kingma, Diederik P and Welling, Max
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%%% - GAN -

**[NIPS-2014]**
[Generative adversarial nets]()
<br>
**Authors:** Goodfellow, Ian and Pouget-Abadie, Jean and Mirza, Mehdi and Xu, Bing and Warde-Farley, David and Ozair, Sherjil and Courville, Aaron and Bengio, Yoshua
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Joint european conference on machine learning and knowledge discovery in databases-2018]**
[Image anomaly detection with generative adversarial networks]()
<br>
**Authors:** Deecke, Lucas and Vandermeulen, Robert and Ruff, Lukas and Mandt, Stephan and Kloft, Marius
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2018]**
[Adversarially learned one-class classifier for novelty detection]()
<br>
**Authors:** Sabokrou, Mohammad and Khalooei, Mohammad and Fathy, Mahmood and Adeli, Ehsan
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[NeurIPS-2018]**
[Generative probabilistic novelty detection with adversarial autoencoders]()
<br>
**Authors:** Pidhorskyi, Stanislav and Almohsen, Ranya and Adjeroh, Donald A and Doretto, Gianfranco
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[arXiv-2020]**
[GAN Ensemble for Anomaly Detection](https://arxiv.org/abs/2012.07988)
<br>
**Authors:** Han, Xu and Chen, Xiaohui and Liu, Li-Ping
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition-2019]**
[Ocgan: One-class novelty detection using gans with constrained latent representations]()
<br>
**Authors:** Perera, Pramuditha and Nallapati, Ramesh and Xiang, Bing
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ECCV-2020]**
[Encoding structure-texture relation with P-Net for anomaly detection in retinal images]()
<br>
**Authors:** Zhou, Kang and Xiao, Yuting and Yang, Jianlong and Cheng, Jun and Liu, Wen and Luo, Weixin and Gu, Zaiwang and Liu, Jiang and Gao, Shenghua
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%%% - Flow-based Model -

**[TPAMI-2020]**
[Normalizing flows: An introduction and review of current methods]()
<br>
**Authors:** Kobyzev, Ivan and Prince, Simon and Brubaker, Marcus
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICML-2015]**
[Variational inference with normalizing flows]()
<br>
**Authors:** Rezende, Danilo and Mohamed, Shakir
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%%% - Feature Enhancement -

**[NeurIPS-2018]**
[A loss framework for calibrated anomaly detection]()
<br>
**Authors:** Menon, Aditya Krishna and Williamson, Robert C
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2021]**
[CutPaste: Self-Supervised Learning for Anomaly Detection and Localization]()
<br>
**Authors:** Li, Chun-Liang and Sohn, Kihyuk and Yoon, Jinsung and Pfister, Tomas
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2021]**
[Multiresolution knowledge distillation for anomaly detection]()
<br>
**Authors:** Salehi, Mohammadreza and Sadjadi, Niousha and Baselizadeh, Soroosh and Rohban, Mohammad H and Rabiee, Hamid R
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%% Energy-based Model %%%%%%%%%%%%

**[ICML-2011]**
[Learning deep energy models]()
<br>
**Authors:** Ngiam, Jiquan and Chen, Zhenghao and Koh, Pang Wei and Ng, Andrew Y
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICML-2016]**
[Deep structured energy based models for anomaly detection]()
<br>
**Authors:** Zhai, Shuangfei and Cheng, Yu and Lu, Weining and Zhang, Zhongfei
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICLR-2020]**
[Iterative energy-based projection on a normal data manifold for anomaly localization]()
<br>
**Authors:** Dehaene, David and Frigo, Oriel and Combrexelle, S{\'e}bastien and Eline, Pierre
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-W-2004]**
[Learning generative visual models from few training examples: An incremental bayesian approach tested on 101 object categories]()
<br>
**Authors:** Fei-Fei, Li and Fergus, Rob and Perona, Pietro
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%% Theoretical Analysis %%%%%%%%%%%%

**[ICML-2018]**
[Open category detection with PAC guarantees]()
<br>
**Authors:** Liu, Si and Garrepalli, Risheek and Dietterich, Thomas and Fern, Alan and Hendrycks, Dan
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICML-2021]**
[Learning Bounds for Open-Set Learning]()
<br>
**Authors:** Fang, Zhen and Lu, Jie and Liu, Anjin and Liu, Feng and Zhang, Guangquan
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[NeurIPS-2019]**
[Multivariate triangular quantile maps for novelty detection]()
<br>
**Authors:** Wang, Jingjing and Sun, Sun and Yu, Yaoliang
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%% AD Reconstruction Model %%%%%%%%%%%%%%%%%%%%%%%%%%%%

%%%% Sparse Representation %

**[AAAI-2021]**
[LREN: Low-Rank Embedded Network for Sample-Free Hyperspectral Anomaly Detection]()
<br>
**Authors:** Jiang, Kai and Xie, Weiying and Lei, Jie and Jiang, Tao and Li, Yunsong
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Multimedia Tools and Applications-2017]**
[Anomaly detection using sparse reconstruction in crowded scenes]()
<br>
**Authors:** Li, Ang and Miao, Zhenjiang and Cen, Yigang and Cen, Yi
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[IEEE Transactions on Circuits and Systems for Video Technology-2013]**
[Adaptive sparse representations for video anomaly detection]()
<br>
**Authors:** Mo, Xuan and Monga, Vishal and Bala, Raja and Fan, Zhigang
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Pattern Recognition-2013]**
[L1 norm based KPCA for novelty detection]()
<br>
**Authors:** Xiao, Yingchao and Wang, Huangang and Xu, Wenli and Zhou, Junwu
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%%% Reconstruction Error %

**[Wireless Telecommunications Symposium-2018]**
[Autoencoder-based network anomaly detection]()
<br>
**Authors:** Chen, Zhaomin and Yeo, Chai Kiat and Lee, Bu Sung and Lau, Chiew Tong
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Special Lecture on IE-2015]**
[Variational autoencoder based anomaly detection using reconstruction probability]()
<br>
**Authors:** An, Jinwon and Cho, Sungzoon
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICLR-W-2018]**
[Efficient gan-based anomaly detection]()
<br>
**Authors:** Zenati, Houssam and Foo, Chuan Sheng and Lecouat, Bruno and Manek, Gaurav and Chandrasekhar, Vijay Ramaseshan
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICML-2019]**
[Anomaly detection with multiple-hypotheses predictions]()
<br>
**Authors:** Nguyen, Duc Tam and Lou, Zhongyu and Klar, Michael and Brox, Thomas
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[NeurIPS-2018]**
[Generative probabilistic novelty detection with adversarial autoencoders]()
<br>
**Authors:** Pidhorskyi, Stanislav and Almohsen, Ranya and Adjeroh, Donald A and Doretto, Gianfranco
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2019]**
[Latent space autoregression for novelty detection]()
<br>
**Authors:** Abati, Davide and Porrello, Angelo and Calderara, Simone and Cucchiara, Rita
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[AAAI-2019]**
[Learning competitive and discriminative reconstructions for anomaly detection]()
<br>
**Authors:** Tian, Kai and Zhou, Shuigeng and Fan, Jianping and Guan, Jihong
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2019]**
[Memorizing normality to detect anomaly: Memory-augmented deep autoencoder for unsupervised anomaly detection]()
<br>
**Authors:** Gong, Dong and Liu, Lingqiao and Le, Vuong and Saha, Budhaditya and Mansour, Moussa Reda and Venkatesh, Svetha and Hengel, Anton van den
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[AAAI-2021]**
[Learning Semantic Context from Normal Samples for Unsupervised Anomaly Detection]()
<br>
**Authors:** Yan, Xudong and Zhang, Huaidong and Xu, Xuemiao and Hu, Xiaowei and Heng, Pheng-Ann
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICLR-2020]**
[Robust subspace recovery layer for unsupervised anomaly detection]()
<br>
**Authors:** Lai, Chieh-Hsin and Zou, Dongmian and Lerman, Gilad
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2018]**
[Future frame prediction for anomaly detection--a new baseline]()
<br>
**Authors:** Liu, Wen and Luo, Weixin and Lian, Dongze and Gao, Shenghua
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

<a name="3.3"></a>
## 3.3 Classfication-based Method

**[Journal of Artificial Intelligence Research-2013]**
[Toward supervised anomaly detection](https://www.jair.org/index.php/jair/article/view/10802)
<br>
**Authors:** Gornitz, Nico and Kloft, Marius and Rieck, Konrad and Brefeld, Ulf
<br>
**Institution:** Technische Universitat Berlin; University of Gottingen; Technische Universitat Darmstadt
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

<a name="3.3.1"></a>
### 3.3.1 One-Class Classification
**[Journal of Artificial Intelligence Research-2002]**
[One-class classification: Concept learning in the absence of counter-examples.](https://elibrary.ru/item.asp?id=5230402)
<br>
**Authors:** Tax, David Martinus Johannes
<br>
**Institution:** Technische Universiteit Delft (The Netherlands)
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Irish conference on artificial intelligence and cognitive science-2009]**
[A survey of recent trends in one class classification](https://link.springer.com/chapter/10.1007/978-3-642-17080-5_21)
<br>
**Authors:** Khan, Shehroz S and Madden, Michael G
<br>
**Institution:** National University of Ireland, Galway, Ireland
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICML-2018]**
[Deep one-class classification](http://proceedings.mlr.press/v80/ruff18a)
<br>
**Authors:** Ruff, Lukas and Vandermeulen, Robert and Goernitz, Nico and Deecke, Lucas and Siddiqui, Shoaib Ahmed and Binder, Alexander and M{\"u}ller, Emmanuel and Kloft, Marius
<br>
**Institution:** Humboldt University of Berlin, Germany; Hasso Plattner Institute, Potsdam, Germany; TU Kaiserslautern, Kaiserslautern, Germany; TU Berlin, Germany; University of Edinburgh, Edinburgh; Singapore University of Technology and Design, Singapore
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2021]**
[PANDA: Adapting Pretrained Features for Anomaly Detection and Segmentation](https://openaccess.thecvf.com/content/CVPR2021/html/Reiss_PANDA_Adapting_Pretrained_Features_for_Anomaly_Detection_and_Segmentation_CVPR_2021_paper.html)
<br>
**Authors:** Reiss, Tal and Cohen, Niv and Bergman, Liron and Hoshen, Yedid
<br>
**Institution:** The Hebrew University of Jerusalem, Israel
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2019]**
[Gods: Generalized one-class discriminative subspaces for anomaly detection](https://openaccess.thecvf.com/content_ICCV_2019/html/Wang_GODS_Generalized_One-Class_Discriminative_Subspaces_for_Anomaly_Detection_ICCV_2019_paper.html)
<br>
**Authors:** Wang, Jue and Cherian, Anoop
<br>
**Institution:** Australian National University, Canberra; Mitsubishi Electric Research Labs, Cambridge, MA
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICLR-2020]**
[Deep semi-supervised anomaly detection](https://arxiv.org/abs/1906.02694)
<br>
**Authors:** Ruff, Lukas and Vandermeulen, Robert A and G{\"o}rnitz, Nico and Binder, Alexander and M{\"u}ller, Emmanuel and M{\"u}ller, Klaus-Robert and Kloft, Marius
<br>
**Institution:** Technical University of Berlin, Germany; 123ai.de, Berlin, Germany; Singapore University of Technology & Design, Singapore; Bonn-Aachen International Center for Information Technology, Germany; Korea University, Seoul, Republic of Korea; Max Planck Institute for Informatics, Saarbrücken, Germany; Technical University of Kaiserslautern, Germany
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

<br>

<a name="3.3.2"></a>
### 3.3.2 Positive-Unlabeled Learning
**[Machine Learning-2020]**
[Learning from positive and unlabeled data: A survey](https://link.springer.com/article/10.1007/s10994-020-05877-5)
<br>
**Authors:** Bekker, Jessa and Davis, Jesse
<br>
**Institution:** KU Leuven, Leuven, Belgium
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[International Symposiums on Information Processing-2008]**
[Learning from positive and unlabeled examples: A survey](https://ieeexplore.ieee.org/abstract/document/4554167)
<br>
**Authors:** Zhang, Bangzuo and Zuo, Wanli
<br>
**Institution:** Jilin University, Changchun, China; Northeast Normal University, Changchun, China
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[International Conference on Information, Intelligence, Systems and Applications-2019]**
[Positive and unlabeled learning algorithms and applications: A survey](https://ieeexplore.ieee.org/abstract/document/8900698)
<br>
**Authors:** Jaskie, Kristen and Spanias, Andreas
<br>
**Institution:** Arizona State University, USA
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[IJCAI-2003]**
[Learning to classify texts using positive and unlabeled data]()
<br>
**Authors:** Li, Xiaoli and Liu, Bing
<br>
**Institution:** National University of Singapore/Singapore-MIT Alliance; University of Illinois at Chicago 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Bioinformatics-2006]**
[PSoL: a positive sample only learning algorithm for finding non-coding RNA genes](https://academic.oup.com/bioinformatics/article/22/21/2590/250725?login=true)
<br>
**Authors:** Wang, Chunlin and Ding, Chris and Meraz, Richard F and Holbrook, Stephen R
<br>
**Institution:** Lawrence Berkeley National Laboratory, Berkeley, CA 94720, USA
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICONIP-2012]**
[Learning from positive and unlabelled examples using maximum margin clustering](https://link.springer.com/chapter/10.1007/978-3-642-34487-9_56)
<br>
**Authors:** Chaudhari, Sneha and Shevade, Shirish
<br>
**Institution:** IBM Research LabBangaloreIndia; Indian Institute of ScienceBangaloreIndia
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Journal of Computers-2009]**
[Reliable Negative Extracting Based on kNN for Learning from Positive and Unlabeled Examples.](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.415.7161&rep=rep1&type=pdf)
<br>
**Authors:** Zhang, Bangzuo and Zuo, Wanli
<br>
**Institution:** Jilin University, Changchun, P. R. China; Northeast Normal University, Changchun, P. R. China
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Journal of Information Science and Engineering-2014]**
[Clustering-based Method for Positive and Unlabeled Text Categorization Enhanced by Improved TFIDF.](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.684.162&rep=rep1&type=pdf)
<br>
**Authors:** Liu, Lu and Peng, Tao
<br>
**Institution:** University of Illinois at Urbana-Champaign Urbana, 61801 USA; Jilin University Changchun, 130012 P.R. China
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[arXiv-2018]**
[Instance-dependent pu learning by bayesian optimal relabeling](https://arxiv.org/abs/1808.02180)
<br>
**Authors:** He, Fengxiang and Liu, Tongliang and Webb, Geoffrey I and Tao, Dacheng
<br>
**Institution:** University of Sydney, 6 Cleveland St, Darlington, NSW 2008, Australia
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[AAAI-2019]**
[Learning competitive and discriminative reconstructions for anomaly detection](https://ojs.aaai.org/index.php/AAAI/article/view/4451)
<br>
**Authors:** Tian, Kai and Zhou, Shuigeng and Fan, Jianping and Guan, Jihong
<br>
**Institution:** Fudan University; University of North Carolina at Charlotte; Tongji University
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2019]**
[Graph convolutional label noise cleaner: Train a plug-and-play action classifier for anomaly detection](https://openaccess.thecvf.com/content_CVPR_2019/html/Zhong_Graph_Convolutional_Label_Noise_Cleaner_Train_a_Plug-And-Play_Action_Classifier_CVPR_2019_paper.html)
<br>
**Authors:** Zhong, Jia-Xing and Li, Nannan and Kong, Weijie and Liu, Shan and Li, Thomas H and Li, Ge
<br>
**Institution:**  Peking University
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICML-2015]**
[Learning from corrupted binary labels via class-probability estimation](http://proceedings.mlr.press/v37/menon15.html)
<br>
**Authors:** Menon, Aditya and Van Rooyen, Brendan and Ong, Cheng Soon and Williamson, Bob
<br>
**Institution:** National ICT Australia; The Australian National University, Canberra
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[Artificial Intelligence and Statistics-2015]**
[A rate of convergence for mixture proportion estimation, with application to learning from noisy labels](http://proceedings.mlr.press/v38/scott15.html)
<br>
**Authors:** Scott, Clayton
<br>
**Institution:** University of Michigan
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

<br>

<a name="3.3.3"></a>
### 3.3.3 Self-Supervised Learning
**[ICDM-2008]**
[Isolation forest](https://ieeexplore.ieee.org/abstract/document/4781136)
<br>
**Authors:** Liu, Fei Tony and Ting, Kai Ming and Zhou, Zhi-Hua
<br>
**Institution:** Monash University, VIC, Australia; Nanjing University, Nanjing, China
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[NeurIPS-2018]**
[Deep anomaly detection using geometric transformations](https://arxiv.org/abs/1805.10917)
<br>
**Authors:** Golan, Izhak and El-Yaniv, Ran
<br>
**Institution:**  Israel Institute of Technology, Haifa, Israel
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ICLR-2020]**
[Classification-based anomaly detection for general data](https://arxiv.org/abs/2005.02359)
<br>
**Authors:** Bergman, Liron and Hoshen, Yedid
<br>
**Institution:** The Hebrew University of Jerusalem, Israel
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[NeurIPS-2020]**
[Csi: Novelty detection via contrastive learning on distributionally shifted instances](https://arxiv.org/abs/2007.08176)
<br>
**Authors:** Tack, Jihoon and Mo, Sangwoo and Jeong, Jongheon and Shin, Jinwoo
<br>
**Institution:** Korea Advanced Institute of Science and Technology
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2021]**
[Anomaly detection in video via self-supervised and multi-task learning](https://openaccess.thecvf.com/content/CVPR2021/html/Georgescu_Anomaly_Detection_in_Video_via_Self-Supervised_and_Multi-Task_Learning_CVPR_2021_paper.html)
<br>
**Authors:** Georgescu, Mariana-Iuliana and Barbalau, Antonio and Ionescu, Radu Tudor and Khan, Fahad Shahbaz and Popescu, Marius and Shah, Mubarak
<br>
**Institution:** University of Bucharest, Romania; MBZ University of Artificial Intelligence, Abu Dhabi; SecurifAI, Romania; University of Central Florida, Orlando, FL
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[CVPR-2019]**
[Object-centric auto-encoders and dummy anomalies for abnormal event detection in video](https://openaccess.thecvf.com/content_CVPR_2019/html/Ionescu_Object-Centric_Auto-Encoders_and_Dummy_Anomalies_for_Abnormal_Event_Detection_in_CVPR_2019_paper.html)
<br>
**Authors:** Ionescu, Radu Tudor and Khan, Fahad Shahbaz and Georgescu, Mariana-Iuliana and Shao, Ling
<br>
**Institution:** Inception Institute of Artificial Intelligence (IIAI), Abu Dhabi, UAE; University of Bucharest, 14 Academiei, Bucharest, Romania; SecurifAI, 21 Mircea Voda, Bucharest, Romania
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%% AD Distance Model %%%%%%%%%%%%%%%%%%%%%%

**[ICISA-2011]**
[The anomaly detection by using dbscan clustering with multiple parameters]()
<br>
**Authors:** Thang, Tran Manh and Kim, Juntae
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[AIAA Scitech 2020 Forum-2020]**
[An application of dbscan clustering for flight anomaly detection during the approach phase]()
<br>
**Authors:** Sheridan, Kevin and Puranik, Tejas G and Mangortey, Eugene and Pinon-Fischer, Olivia J and Kirby, Michelle and Mavris, Dimitri N
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%%% Meta-Learning %%%%%%%%%%%%

**[arXiv-2018]**
[Meta-learning: A survey](https://arxiv.org/abs/1810.03548)
<br>
**Authors:** Vanschoren, Joaquin
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[arXiv-2020]**
[Meta-learning in neural networks: A survey](https://arxiv.org/abs/2004.05439)
<br>
**Authors:** Hospedales, Timothy and Antoniou, Antreas and Micaelli, Paul and Storkey, Amos
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

**[ECCV-2020]**
[Backpropagated gradient representations for anomaly detection]()
<br>
**Authors:** Kwon, Gukyeong and Prabhushankar, Mohit and Temel, Dogancan and AlRegib, Ghassan
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>

%% AD Hybrid Model %%%%%%%%%%%%%%%%%%%%%%

**[International Conference on Parallel Problem Solving from Nature-2016]**
[A hybrid autoencoder and density estimation model for anomaly detection]()
<br>
**Authors:** Nicolau, Miguel and McDermott, James and others
<br>
**Institution:** 
> <details>
> <summary></summary>
> <p style="text-align:left">
>
> </p>
> </details>


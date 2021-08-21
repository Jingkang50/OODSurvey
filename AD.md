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


@article{anomalysurvey21ieee,
  title={A unifying review of deep and shallow anomaly detection},
  author={Ruff, Lukas and Kauffmann, Jacob R and Vandermeulen, Robert A and Montavon, Gr{\'e}goire and Samek, Wojciech and Kloft, Marius and Dietterich, Thomas G and M{\"u}ller, Klaus-Robert},
  journal={Proceedings of the IEEE},
  year={2021}
}

@article{anomalyreview20adelaide,
  title={Deep learning for anomaly detection: A review},
  author={Pang, Guansong and Shen, Chunhua and Cao, Longbing and Hengel, Anton van den},
  journal={arXiv preprint arXiv:2007.02500},
  year={2020}
}

@techreport{anomalysurvey20dsong,
  title={Anomalous instance detection in deep learning: A survey},
  author={Bulusu, Saikiran and Kailkhura, Bhavya and Li, Bo and Varshney, P and Song, Dawn},
  year={2020},
  institution={Lawrence Livermore National Lab.(LLNL), Livermore, CA (United States)}
}

@article{anomalysurvey19sydney,
  title={Deep learning for anomaly detection: A survey},
  author={Chalapathy, Raghavendra and Chawla, Sanjay},
  journal={arXiv preprint arXiv:1901.03407},
  year={2019}
}

@article{anomalygan19arxiv,
  title={A survey on gans for anomaly detection},
  author={Di Mattia, Federico and Galeone, Paolo and De Simoni, Michele and Ghelfi, Emanuele},
  journal={arXiv preprint arXiv:1906.11632},
  year={2019}
}

%% AD Method
@inproceedings{semanticanomaly20aaai,
  title={Detecting semantic anomalies},
  author={Ahmed, Faruk and Courville, Aaron},
  booktitle={AAAI},
  year={2020}
}

%% AD Probabilistic Model %%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%% Density Estimation %%%%%%%%%%%%
%%%% parametric %
@article{anomalyparametric98pami,
  title={Parametric model fitting: From inlier characterization to outlier detection},
  author={Danuser, Gaudenz and Stricker, Markus},
  journal={TPAMI},
  year={1998}
}

%%%% - mahalanobis -
@article{mahalanobis00cils,
  title={The mahalanobis distance},
  author={De Maesschalck, Roy and Jouan-Rimbaud, Delphine and Massart, D{\'e}sir{\'e} L},
  journal={Chemometrics and intelligent laboratory systems},
  year={2000}
}

@article{mahalanobis18jesp,
  title={Detecting multivariate outliers: Use a robust variant of the Mahalanobis distance},
  author={Leys, Christophe and Klein, Olivier and Dominicy, Yves and Ley, Christophe},
  journal={Journal of Experimental Social Psychology},
  year={2018}
}

%%%% - GMM -
@article{gmm84siam,
  title={Mixture densities, maximum likelihood and the EM algorithm},
  author={Redner, Richard A and Walker, Homer F},
  journal={SIAM review},
  year={1984},
}

@inproceedings{anomalygmm20icml,
  title={Anomaly detection over noisy data using learned probability distributions},
  author={Eskin, Eleazar},
  booktitle={ICML},
  year={2000}
}

%%%% - Poisson -
@inproceedings{poisson16isi,
  title={Poisson factorization for peer-based anomaly detection},
  author={Turcotte, Melissa and Moore, Juston and Heard, Nick and McPhall, Aaron},
  booktitle={IEEE Conference on Intelligence and Security Informatics (ISI)},
  year={2016},
}


%%%% non-parametric %
@article{nonparametric91jasa,
  title={Review papers: Recent developments in nonparametric density estimation},
  author={Izenman, Alan Julian},
  journal={Journal of the american statistical association},
  year={1991}
}

%%%% - histogram -
@article{histogram73cstm,
  title={A histogram method of density estimation},
  author={Van Ryzin, J},
  journal={Communications in Statistics-Theory and Methods},
  year={1973}
}

@inproceedings{histogram12wireless,
  title={Histogram-based online anomaly detection in hierarchical wireless sensor networks},
  author={Xie, Miao and Hu, Jiankun and Tian, Biming},
  booktitle={ICTSPCC},
  year={2012},
}

@article{histogram09traffic,
  title={Histogram-based traffic anomaly detection},
  author={Kind, Andreas and Stoecklin, Marc Ph and Dimitropoulos, Xenofontas},
  journal={IEEE Transactions on Network and Service Management},
  year={2009}
}

@article{hbos12ki,
  title={Histogram-based outlier score (hbos): A fast unsupervised anomaly detection algorithm},
  author={Goldstein, Markus and Dengel, Andreas},
  journal={KI-2012: Poster and Demo Track},
  year={2012}
}

%%%% - kde -
@article{kde62math,
  title={On estimation of a probability density function and mode},
  author={Parzen, Emanuel},
  journal={The annals of mathematical statistics},
  year={1962}
}

@article{kdeanomaly98ime,
  title={Applications of probability density estimation to the detection of abnormal conditions in engineering},
  author={Desforges, MJ and Jacob, PJ and Cooper, JE},
  journal={Proceedings of the institution of mechanical engineers},
  year={1998},
}

@article{anomalykde18tkde,
  title={Anomaly detection using local kernel density estimation and context-based regression},
  author={Hu, Weiming and Gao, Jun and Li, Bing and Wu, Ou and Du, Junping and Maybank, Stephen},
  journal={TKDE},
  year={2018},
}

%%%% old application
@inproceedings{adpower82iee,
  title={Dynamic state estimation including anomaly detection and identification for power systems},
  author={Nishiya, K and Hasegawa, J and Koike, T},
  booktitle={IEE proceedings C (generation, transmission and distribution)},
  year={1982},
}

@article{admisuse93tse,
  title={Statistical foundations of audit trail analysis for the detection of computer misuse},
  author={Helman, Paul and Liepins, Gunar},
  journal={IEEE Transactions on software engineering},
  year={1993},
}

@article{adoverview07cn,
  title={An overview of anomaly detection techniques: Existing solutions and latest technological trends},
  author={Patcha, Animesh and Park, Jung-Min},
  journal={Computer networks},
  year={2007},
}

@inproceedings{adcrowdedscene10cvpr,
  title={Chaotic invariants of lagrangian particle trajectories for anomaly detection in crowded scenes},
  author={Wu, Shandong and Moore, Brian E and Shah, Mubarak},
  booktitle={CVPR},
  year={2010},
}

@article{adhighdim20jcgs,
  title={Anomaly detection in high-dimensional data},
  author={Talagala, Priyanga Dilini and Hyndman, Rob J and Smith-Miles, Kate},
  journal={Journal of Computational and Graphical Statistics},
  year={2020},
}


%%% Deep Density Estimation %%%%%%%%%%%%
@inproceedings{dagmm18iclr,
  title={Deep autoencoding gaussian mixture model for unsupervised anomaly detection},
  author={Zong, Bo and Song, Qi and Min, Martin Renqiang and Cheng, Wei and Lumezanu, Cristian and Cho, Daeki and Chen, Haifeng},
  booktitle={ICLR},
  year={2018}
}

%%%%% - AE -

@article{ae91aiche,
  title={Nonlinear principal component analysis using autoassociative neural networks},
  author={Kramer, Mark A},
  journal={AIChE journal},
  year={1991},
}



%%%%% - VAE -
@article{vae13arxiv,
  title={Auto-encoding variational bayes},
  author={Kingma, Diederik P and Welling, Max},
  journal={arXiv preprint arXiv:1312.6114},
  year={2013}
}

%%%%% - GAN -
@article{gan14nips,
  title={Generative adversarial nets},
  author={Goodfellow, Ian and Pouget-Abadie, Jean and Mirza, Mehdi and Xu, Bing and Warde-Farley, David and Ozair, Sherjil and Courville, Aaron and Bengio, Yoshua},
  journal={NIPS},
  year={2014}
}

@inproceedings{adgan18ecml,
  title={Image anomaly detection with generative adversarial networks},
  author={Deecke, Lucas and Vandermeulen, Robert and Ruff, Lukas and Mandt, Stephan and Kloft, Marius},
  booktitle={Joint european conference on machine learning and knowledge discovery in databases},
  year={2018},
}

@inproceedings{advrec18cvpr,
  title={Adversarially learned one-class classifier for novelty detection},
  author={Sabokrou, Mohammad and Khalooei, Mohammad and Fathy, Mahmood and Adeli, Ehsan},
  booktitle={CVPR},
  year={2018}
}

@inproceedings{gpnd18nips,
  title={Generative probabilistic novelty detection with adversarial autoencoders},
  author={Pidhorskyi, Stanislav and Almohsen, Ranya and Adjeroh, Donald A and Doretto, Gianfranco},
  booktitle={NeurIPS},
  year={2018}
}

@article{ganesb21aaai,
  title={GAN Ensemble for Anomaly Detection},
  author={Han, Xu and Chen, Xiaohui and Liu, Li-Ping},
  journal={arXiv preprint arXiv:2012.07988},
  year={2020}
}

@inproceedings{ocgan19cvpr,
  title={Ocgan: One-class novelty detection using gans with constrained latent representations},
  author={Perera, Pramuditha and Nallapati, Ramesh and Xiang, Bing},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={2898--2906},
  year={2019}
}

@inproceedings{pnet20eccv,
  title={Encoding structure-texture relation with P-Net for anomaly detection in retinal images},
  author={Zhou, Kang and Xiao, Yuting and Yang, Jianlong and Cheng, Jun and Liu, Wen and Luo, Weixin and Gu, Zaiwang and Liu, Jiang and Gao, Shenghua},
  booktitle={ECCV},
  year={2020},
}



%%%%% - Flow-based Model -
@article{flowreview20pami,
  title={Normalizing flows: An introduction and review of current methods},
  author={Kobyzev, Ivan and Prince, Simon and Brubaker, Marcus},
  journal={TPAMI},
  year={2020},
}

@inproceedings{flows15icml,
  title={Variational inference with normalizing flows},
  author={Rezende, Danilo and Mohamed, Shakir},
  booktitle={ICML},
  year={2015},
}

%%%%% - Feature Enhancement -
@inproceedings{losscalad18nips,
  title={A loss framework for calibrated anomaly detection},
  author={Menon, Aditya Krishna and Williamson, Robert C},
  booktitle={NeurIPS},
  year={2018}
}

@inproceedings{cutpaste21cvpr,
  title={CutPaste: Self-Supervised Learning for Anomaly Detection and Localization},
  author={Li, Chun-Liang and Sohn, Kihyuk and Yoon, Jinsung and Pfister, Tomas},
  booktitle={CVPR},
  year={2021}
}

@inproceedings{distill21cvpr,
  title={Multiresolution knowledge distillation for anomaly detection},
  author={Salehi, Mohammadreza and Sadjadi, Niousha and Baselizadeh, Soroosh and Rohban, Mohammad H and Rabiee, Hamid R},
  booktitle={CVPR},
  pages={14902--14912},
  year={2021}
}

%%% Energy-based Model %%%%%%%%%%%%
@inproceedings{energy11icml,
  title={Learning deep energy models},
  author={Ngiam, Jiquan and Chen, Zhenghao and Koh, Pang Wei and Ng, Andrew Y},
  booktitle={ICML},
  year={2011}
}

@inproceedings{energyad16icml,
  title={Deep structured energy based models for anomaly detection},
  author={Zhai, Shuangfei and Cheng, Yu and Lu, Weining and Zhang, Zhongfei},
  booktitle={ICML},
  year={2016}
}

@article{ebproject20iclr,
  title={Iterative energy-based projection on a normal data manifold for anomaly localization},
  author={Dehaene, David and Frigo, Oriel and Combrexelle, S{\'e}bastien and Eline, Pierre},
  journal={ICLR},
  year={2020}
}

@inproceedings{scorematch04CVPRW,
  title={Learning generative visual models from few training examples: An incremental bayesian approach tested on 101 object categories},
  author={Fei-Fei, Li and Fergus, Rob and Perona, Pietro},
  booktitle={CVPR-W},
  year={2004}
}

%%% Theoretical Analysis %%%%%%%%%%%%
@inproceedings{pac18icml,
  title={Open category detection with PAC guarantees},
  author={Liu, Si and Garrepalli, Risheek and Dietterich, Thomas and Fern, Alan and Hendrycks, Dan},
  booktitle={ICML},
  year={2018},
}

@inproceedings{bound21icml,
  title={Learning Bounds for Open-Set Learning},
  author={Fang, Zhen and Lu, Jie and Liu, Anjin and Liu, Feng and Zhang, Guangquan},
  booktitle={ICML},
  year={2021},
}

@inproceedings{tqm19nips,
  title={Multivariate triangular quantile maps for novelty detection},
  author={Wang, Jingjing and Sun, Sun and Yu, Yaoliang},
  booktitle={NeurIPS},
  year={2019}
}

%% AD Reconstruction Model %%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%% Sparse Representation %
@inproceedings{lren21aaai,
  title={LREN: Low-Rank Embedded Network for Sample-Free Hyperspectral Anomaly Detection},
  author={Jiang, Kai and Xie, Weiying and Lei, Jie and Jiang, Tao and Li, Yunsong},
  booktitle={AAAI},
  year={2021}
}

@article{adsparsecrowd17mta,
  title={Anomaly detection using sparse reconstruction in crowded scenes},
  author={Li, Ang and Miao, Zhenjiang and Cen, Yigang and Cen, Yi},
  journal={Multimedia Tools and Applications},
  year={2017},
}

@article{adsparsevideo13tcsvt,
  title={Adaptive sparse representations for video anomaly detection},
  author={Mo, Xuan and Monga, Vishal and Bala, Raja and Fan, Zhigang},
  journal={IEEE Transactions on Circuits and Systems for Video Technology},
  year={2013},
}

@article{kpca13pr,
  title={L1 norm based KPCA for novelty detection},
  author={Xiao, Yingchao and Wang, Huangang and Xu, Wenli and Zhou, Junwu},
  journal={Pattern Recognition},
  year={2013}
}

%%%% Reconstruction Error %
@inproceedings{recerrae18wts,
  title={Autoencoder-based network anomaly detection},
  author={Chen, Zhaomin and Yeo, Chai Kiat and Lee, Bu Sung and Lau, Chiew Tong},
  booktitle={Wireless Telecommunications Symposium},
  year={2018}
}

@article{recerrvae15ie,
  title={Variational autoencoder based anomaly detection using reconstruction probability},
  author={An, Jinwon and Cho, Sungzoon},
  journal={Special Lecture on IE},
  year={2015}
}

@inproceedings{ganad18iclr,
  title={Efficient gan-based anomaly detection},
  author={Zenati, Houssam and Foo, Chuan Sheng and Lecouat, Bruno and Manek, Gaurav and Chandrasekhar, Vijay Ramaseshan},
  booktitle={ICLR-W},
  year={2018}
}

@inproceedings{conad19icml,
  title={Anomaly detection with multiple-hypotheses predictions},
  author={Nguyen, Duc Tam and Lou, Zhongyu and Klar, Michael and Brox, Thomas},
  booktitle={ICML},
  year={2019}
}

@article{gpnd18nips,
  title={Generative probabilistic novelty detection with adversarial autoencoders},
  author={Pidhorskyi, Stanislav and Almohsen, Ranya and Adjeroh, Donald A and Doretto, Gianfranco},
  journal={NeurIPS},
  year={2018}
}

@inproceedings{autogres19cvpr,
  title={Latent space autoregression for novelty detection},
  author={Abati, Davide and Porrello, Angelo and Calderara, Simone and Cucchiara, Rita},
  booktitle={CVPR},
  year={2019}
}

@inproceedings{cora19aaai,
  title={Learning competitive and discriminative reconstructions for anomaly detection},
  author={Tian, Kai and Zhou, Shuigeng and Fan, Jianping and Guan, Jihong},
  booktitle={AAAI},
  year={2019}
}

@inproceedings{menae19iccv,
  title={Memorizing normality to detect anomaly: Memory-augmented deep autoencoder for unsupervised anomaly detection},
  author={Gong, Dong and Liu, Lingqiao and Le, Vuong and Saha, Budhaditya and Mansour, Moussa Reda and Venkatesh, Svetha and Hengel, Anton van den},
  booktitle={CVPR},
  year={2019}
}

@inproceedings{scadn21aaai,
  title={Learning Semantic Context from Normal Samples for Unsupervised Anomaly Detection},
  author={Yan, Xudong and Zhang, Huaidong and Xu, Xuemiao and Hu, Xiaowei and Heng, Pheng-Ann},
  booktitle={AAAI},
  year={2021}
}

@article{rsr20iclr,
  title={Robust subspace recovery layer for unsupervised anomaly detection},
  author={Lai, Chieh-Hsin and Zou, Dongmian and Lerman, Gilad},
  journal={ICLR},
  year={2020}
}

@inproceedings{framepred18cvpr,
  title={Future frame prediction for anomaly detection--a new baseline},
  author={Liu, Wen and Luo, Weixin and Lian, Dongze and Gao, Shenghua},
  booktitle={CVPR},
  year={2018}
}



%% AD Classification Model %%%%%%%%%%%%%%%%%%%%%%
@article{supervisedad13jair,
  title={Toward supervised anomaly detection},
  author={G{\"o}rnitz, Nico and Kloft, Marius and Rieck, Konrad and Brefeld, Ulf},
  journal={Journal of Artificial Intelligence Research},
  year={2013}
}

%% OCC
@article{occ02tax,
  title={One-class classification: Concept learning in the absence of counter-examples.},
  author={Tax, David Martinus Johannes},
  year={2002}
}

@inproceedings{occsurvey09icaics,
  title={A survey of recent trends in one class classification},
  author={Khan, Shehroz S and Madden, Michael G},
  booktitle={Irish conference on artificial intelligence and cognitive science},
  year={2009},
}


@inproceedings{deepsvdd18icml,
  title={Deep one-class classification},
  author={Ruff, Lukas and Vandermeulen, Robert and Goernitz, Nico and Deecke, Lucas and Siddiqui, Shoaib Ahmed and Binder, Alexander and M{\"u}ller, Emmanuel and Kloft, Marius},
  booktitle={ICML},
  year={2018}
}

@inproceedings{panda21cvpr,
  title={PANDA: Adapting Pretrained Features for Anomaly Detection and Segmentation},
  author={Reiss, Tal and Cohen, Niv and Bergman, Liron and Hoshen, Yedid},
  booktitle={CVPR},
  year={2021}
}

@inproceedings{gods19iccv,
  title={Gods: Generalized one-class discriminative subspaces for anomaly detection},
  author={Wang, Jue and Cherian, Anoop},
  booktitle={CVPR},
  year={2019}
}

@article{deepsad20iclr,
  title={Deep semi-supervised anomaly detection},
  author={Ruff, Lukas and Vandermeulen, Robert A and G{\"o}rnitz, Nico and Binder, Alexander and M{\"u}ller, Emmanuel and M{\"u}ller, Klaus-Robert and Kloft, Marius},
  journal={ICLR},
  year={2020}
}

%% PU-Learning
@article{pusurvey20ml,
  title={Learning from positive and unlabeled data: A survey},
  author={Bekker, Jessa and Davis, Jesse},
  journal={Machine Learning},
  year={2020},
}

@inproceedings{pusurvey08isip,
  title={Learning from positive and unlabeled examples: A survey},
  author={Zhang, Bangzuo and Zuo, Wanli},
  booktitle={International Symposiums on Information Processing},
  year={2008},
}

@inproceedings{pusurvey19iisa,
  title={Positive and unlabeled learning algorithms and applications: A survey},
  author={Jaskie, Kristen and Spanias, Andreas},
  booktitle={International Conference on Information, Intelligence, Systems and Applications},
  year={2019},
}

@inproceedings{rocchio03ijcai,
  title={Learning to classify texts using positive and unlabeled data},
  author={Li, Xiaoli and Liu, Bing},
  booktitle={IJCAI},
  year={2003}
}

@article{psol06bioinfo,
  title={PSoL: a positive sample only learning algorithm for finding non-coding RNA genes},
  author={Wang, Chunlin and Ding, Chris and Meraz, Richard F and Holbrook, Stephen R},
  journal={Bioinformatics},
  year={2006},
}

@inproceedings{pulearncluster12iconip,
  title={Learning from positive and unlabelled examples using maximum margin clustering},
  author={Chaudhari, Sneha and Shevade, Shirish},
  booktitle={ICONIP},
  year={2012},
}

@article{pulearnknn09jcomp,
  title={Reliable Negative Extracting Based on kNN for Learning from Positive and Unlabeled Examples.},
  author={Zhang, Bangzuo and Zuo, Wanli},
  journal={Journal of Computers},
  year={2009}
}

@article{pulearncluster14jise,
  title={Clustering-based Method for Positive and Unlabeled Text Categorization Enhanced by Improved TFIDF.},
  author={Liu, Lu and Peng, Tao},
  journal={Journal of Information Science and Engineering},
  year={2014}
}

@article{bayesianrelabel18arxiv,
  title={Instance-dependent pu learning by bayesian optimal relabeling},
  author={He, Fengxiang and Liu, Tongliang and Webb, Geoffrey I and Tao, Dacheng},
  journal={arXiv preprint arXiv:1808.02180},
  year={2018}
}

@inproceedings{comprec19aaai,
  title={Learning competitive and discriminative reconstructions for anomaly detection},
  author={Tian, Kai and Zhou, Shuigeng and Fan, Jianping and Guan, Jihong},
  booktitle={AAAI},
  year={2019}
}

@inproceedings{gcnclean19cvpr,
  title={Graph convolutional label noise cleaner: Train a plug-and-play action classifier for anomaly detection},
  author={Zhong, Jia-Xing and Li, Nannan and Kong, Weijie and Liu, Shan and Li, Thomas H and Li, Ge},
  booktitle={CVPR},
  year={2019}
}

@inproceedings{puleanclassest15icml,
  title={Learning from corrupted binary labels via class-probability estimation},
  author={Menon, Aditya and Van Rooyen, Brendan and Ong, Cheng Soon and Williamson, Bob},
  booktitle={ICML},
  year={2015}
}

@inproceedings{pulearnmixture15ais,
  title={A rate of convergence for mixture proportion estimation, with application to learning from noisy labels},
  author={Scott, Clayton},
  booktitle={Artificial Intelligence and Statistics},
  year={2015}
}

%% SSL
@inproceedings{isoforest08icdm,
  title={Isolation forest},
  author={Liu, Fei Tony and Ting, Kai Ming and Zhou, Zhi-Hua},
  booktitle={ICDM},
  year={2008}
}

@inproceedings{transform18nips,
  title={Deep anomaly detection using geometric transformations},
  author={Golan, Izhak and El-Yaniv, Ran},
  booktitle={NeurIPS},
  year={2018}
}

@inproceedings{goad20iclr,
  title={Classification-based anomaly detection for general data},
  author={Bergman, Liron and Hoshen, Yedid},
  booktitle={ICLR},
  year={2020}
}

@inproceedings{csi20nips,
  title={Csi: Novelty detection via contrastive learning on distributionally shifted instances},
  author={Tack, Jihoon and Mo, Sangwoo and Jeong, Jongheon and Shin, Jinwoo},
  booktitle={NeurIPS},
  year={2020}
}

@inproceedings{ssmtl21cvpr,
  title={Anomaly detection in video via self-supervised and multi-task learning},
  author={Georgescu, Mariana-Iuliana and Barbalau, Antonio and Ionescu, Radu Tudor and Khan, Fahad Shahbaz and Popescu, Marius and Shah, Mubarak},
  booktitle={CVPR},
  year={2021}
}

@inproceedings{aecluster19cvpr,
  title={Object-centric auto-encoders and dummy anomalies for abnormal event detection in video},
  author={Ionescu, Radu Tudor and Khan, Fahad Shahbaz and Georgescu, Mariana-Iuliana and Shao, Ling},
  booktitle={CVPR},
  year={2019}
}


%% AD Distance Model %%%%%%%%%%%%%%%%%%%%%%


@inproceedings{dbscanad11icisa,
  title={The anomaly detection by using dbscan clustering with multiple parameters},
  author={Thang, Tran Manh and Kim, Juntae},
  booktitle={ICISA},
  year={2011},
}

@inproceedings{dbscan20aiaa,
  title={An application of dbscan clustering for flight anomaly detection during the approach phase},
  author={Sheridan, Kevin and Puranik, Tejas G and Mangortey, Eugene and Pinon-Fischer, Olivia J and Kirby, Michelle and Mavris, Dimitri N},
  booktitle={AIAA Scitech 2020 Forum},
  year={2020}
}

%%% Meta-Learning %%%%%%%%%%%%
@article{metalearningsurvey18arxiv,
  title={Meta-learning: A survey},
  author={Vanschoren, Joaquin},
  journal={arXiv preprint arXiv:1810.03548},
  year={2018}
}

@article{metalearningsurvey20arxiv,
  title={Meta-learning in neural networks: A survey},
  author={Hospedales, Timothy and Antoniou, Antreas and Micaelli, Paul and Storkey, Amos},
  journal={arXiv preprint arXiv:2004.05439},
  year={2020}
}

@inproceedings{gradcon20eccv,
  title={Backpropagated gradient representations for anomaly detection},
  author={Kwon, Gukyeong and Prabhushankar, Mohit and Temel, Dogancan and AlRegib, Ghassan},
  booktitle={ECCV},
  year={2020}
}



%% AD Hybrid Model %%%%%%%%%%%%%%%%%%%%%%
@inproceedings{hybrid16,
  title={A hybrid autoencoder and density estimation model for anomaly detection},
  author={Nicolau, Miguel and McDermott, James and others},
  booktitle={International Conference on Parallel Problem Solving from Nature},
  year={2016}
}

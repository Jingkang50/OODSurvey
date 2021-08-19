# 5. OOD Detection

## 5.1 Classfication-based Method
### 5.1.0 Baseline
**[ICLR-2017]**
[A baseline for detecting misclassified and out-of-distribution examples in neural networks](https://arxiv.org/abs/1610.02136).
Hendrycks, Dan and Gimpel, Kevin
> <details>
> <summary> The starting point of OOD detection, using softmax probabilities.</summary>
> <p class="small" style="text-align:left">
> Correctly classified examples tend to have greater maximum softmax probabilities than erroneously classified and out-of-distribution examples, allowing for their detection.
> </p>
> </details>


### 5.1.1 Confidence Calibration

#### - Post-hoc Calibration
**[ODIN-2017]**
[A baseline for detecting misclassified and out-of-distribution examples in neural networks](https://arxiv.org/abs/1610.02136).
Hendrycks, Dan and Gimpel, Kevin
> <details>
> <summary> The starting point of OOD detection. It uses softmax probabilities.</summary>
> <p class="small" style="text-align:left">
> Correctly classified examples tend to have greater maximum softmax probabilities than erroneously classified and out-of-distribution examples, allowing for their detection.
> </p>
> </details>

---

#### - Bayesian Methods


@inproceedings{mcdropout16icml,
  title={Dropout as a bayesian approximation: Representing model uncertainty in deep learning},
  author={Gal, Yarin and Ghahramani, Zoubin},
  booktitle={ICML},
  year={2016},
}

@article{deepensemble17nips,
  title={Simple and scalable predictive uncertainty estimation using deep ensembles},
  author={Lakshminarayanan, Balaji and Pritzel, Alexander and Blundell, Charles},
  journal={NeurIPS},
  year={2017}
}

@inproceedings{howgoodbnn20icml,
  title={How good is the bayes posterior in deep neural networks really?},
  author={Wenzel, Florian and Roth, Kevin and Veeling, Bastiaan S and {\'S}wi{\k{a}}tkowski, Jakub and Tran, Linh and Mandt, Stephan and Snoek, Jasper and Salimans, Tim and Jenatton, Rodolphe and Nowozin, Sebastian},
  booktitle={ICML},
  year={2020}
}

@inproceedings{practicalbnn19nips,
  title={Practical deep learning with Bayesian principles},
  author={Osawa, Kazuki and Swaroop, Siddharth and Jain, Anirudh and Eschenhagen, Runa and Turner, Richard E and Yokota, Rio and Khan, Mohammad Emtiyaz},
  booktitle={NeurIPS},
  year={2019}
}

@article{bnngeneralization20icml,
  title={Bayesian deep learning and a probabilistic perspective of generalization},
  author={Wilson, Andrew Gordon and Izmailov, Pavel},
  journal={ICML},
  year={2020}
}

@inproceedings{bayesood19nips,
  title={Practical deep learning with Bayesian principles},
  author={Osawa, Kazuki and Swaroop, Siddharth and Jain, Anirudh and Eschenhagen, Runa and Turner, Richard E and Yokota, Rio and Khan, Mohammad Emtiyaz},
  booktitle={NeurIPS},
  year={2019}
}

@inproceedings{inbwnbnn20icmlw,
  title={'In-Between' Uncertainty in Bayesian Neural Networks},
  author={Foong, Andrew YK and Li, Yingzhen and Hern{\'a}ndez-Lobato, Jos{\'e} Miguel and Turner, Richard E},
  booktitle={ICML-W},
  year={2020}
}

---

#### - Other Confidence Enhancement Methods
@inproceedings{ceda19cvpr,
  title={Why relu networks yield high-confidence predictions far away from the training data and how to mitigate the problem},
  author={Hein, Matthias and Andriushchenko, Maksym and Bitterwolf, Julian},
  booktitle={CVPR},
  year={2019}
}

@inproceedings{good20nips,
  title={Certifiably adversarially robust detection of out-of-distribution data},
  author={Bitterwolf, Julian and Meinke, Alexander and Hein, Matthias},
  booktitle={NeurIPS},
  year={2020}
}

@inproceedings{mixup19nips,
  title={On mixup training: Improved calibration and predictive uncertainty for deep neural networks},
  author={Thulasidasan, Sunil and Chennupati, Gopinath and Bilmes, Jeff and Bhattacharya, Tanmoy and Michalak, Sarah},
  booktitle={NeurIPS},
  year={2019}
}

@article{ccu20arxiv,
  title={Towards neural networks that provably know when they don't know},
  author={Meinke, Alexander and Hein, Matthias},
  journal={arXiv preprint arXiv:1909.12180},
  year={2019}
}

@article{aloe20arxiv,
  title={Robust out-of-distribution detection for neural networks},
  author={Chen, Jiefeng and Li, Yixuan and Wu, Xi and Liang, Yingyu and Jha, Somesh},
  journal={arXiv preprint arXiv:2003.09711},
  year={2020}
}

@inproceedings{mood21cvpr,
  title={MOOD: Multi-level Out-of-distribution Detection},
  author={Lin, Ziqian and Roy, Sreya Dutta and Li, Yixuan},
  booktitle={CVPR},
  year={2021}
}


@article{confbranch2018arxiv,
  title={Learning confidence for out-of-distribution detection in neural networks},
  author={DeVries, Terrance and Taylor, Graham W},
  journal={arXiv preprint arXiv:1802.04865},
  year={2018}
}

### 5.1.2 Outlier Exposure
@inproceedings{agnostophobia18nips,
  title={Reducing network agnostophobia},
  author={Dhamija, Akshay Raj and G{\"u}nther, Manuel and Boult, Terrance E},
  booktitle={NeurIPS},
  year={2018}
}

@inproceedings{oe18nips,
  title={Deep anomaly detection with outlier exposure},
  author={Hendrycks, Dan and Mazeika, Mantas and Dietterich, Thomas},
  booktitle={NeurIPS},
  year={2018}
}

@inproceedings{mcd19iccv,
  title={Unsupervised out-of-distribution detection by maximum classifier discrepancy},
  author={Yu, Qing and Aizawa, Kiyoharu},
  booktitle={ICCV},
  year={2019}
}

@inproceedings{pseudolabel20aaai,
  title={Self-supervised learning for generalizable out-of-distribution detection},
  author={Mohseni, Sina and Pitale, Mandar and Yadawa, JBS and Wang, Zhangyang},
  booktitle={AAAI},
  year={2020}
}

@article{oecc21neurocomputing,
  title={Outlier exposure with confidence control for out-of-distribution detection},
  author={Papadopoulos, Aristotelis-Angelos and Rajati, Mohammad Reza and Shaikh, Nazim and Wang, Jiamian},
  journal={Neurocomputing},
  year={2021}
}



### 5.1.3 OOD Data Generation
@inproceedings{confcal18iclr,
  title={Training confidence-calibrated classifiers for detecting out-of-distribution samples},
  author={Lee, Kimin and Lee, Honglak and Lee, Kibok and Shin, Jinwoo},
  journal={ICLR},
  year={2018}
}

@inproceedings{confgan18nipsw,
  title={Building robust classifiers through generation of confident out of distribution examples},
  author={Sricharan, Kumar and Srivastava, Ashok},
  booktitle={NeurIPS-W},
  year={2018}
}

@inproceedings{zsar19cvpr,
  title={Out-of-distribution detection for generalized zero-shot action recognition},
  author={Mandal, Devraj and Narayan, Sanath and Dwivedi, Sai Kumar and Gupta, Vikram and Ahmed, Shuaib and Khan, Fahad Shahbaz and Shao, Ling},
  booktitle={CVPR},
  year={2019}
}

@inproceedings{oodsg19nipsw,
  title={Out-of-distribution detection in classifiers via generation},
  author={Vernekar, Sachin and Gaurav, Ashish and Abdelzad, Vahdat and Denouden, Taylor and Salay, Rick and Czarnecki, Krzysztof},
  booktitle={NeurIPS-W},
  year={2019}
}


### 5.1.4 Label Space Redesign

**[arXiv-2021]** 
[Exploring the Limits of Out-of-Distribution Detection](https://arxiv.org/abs/2106.03004).
Fort, Stanislav and Ren, Jie and Lakshminarayanan, Balaji.


**[CVPR-2021]**
[MOS: Towards Scaling Out-of-distribution Detection for Large Semantic Space](https://arxiv.org/abs/2105.01879).
Huang, Rui and Li, Yixuan.


**[NeurIPS-2018]**
[Out-of-Distribution Detection using Multiple Semantic Label Representations](https://arxiv.org/abs/1808.06664). 
Shalev, Gabi and Adi, Yossi and Keshet, Joseph.


**[CVPR-2018]**
[Hierarchical Novelty Detection for Visual Object Recognition](https://arxiv.org/abs/1804.00722). 
Lee, Kibok and Lee, Kimin and Min, Kyle and Zhang, Yuting and Shin, Jinwoo and Lee, Honglak.


### 5.1.5 Big Pretrained Model

@article{nearood21arxiv,
  title={Exploring the Limits of Out-of-Distribution Detection},
  author={Fort, Stanislav and Ren, Jie and Lakshminarayanan, Balaji},
  journal={arXiv preprint arXiv:2106.03004},
  year={2021}
}

@article{pretransformer20arxiv,
  title={Pretrained transformers improve out-of-distribution robustness},
  author={Hendrycks, Dan and Liu, Xiaoyuan and Wallace, Eric and Dziedzic, Adam and Krishnan, Rishabh and Song, Dawn},
  journal={arXiv preprint arXiv:2004.06100},
  year={2020}
}

@article{oodformer21arxiv,
  title={OODformer: Out-Of-Distribution Detection Transformer},
  author={Koner, Rajat and Sinhamahapatra, Poulami and Roscher, Karsten and G{\"u}nnemann, Stephan and Tresp, Volker},
  journal={arXiv preprint arXiv:2107.08976},
  year={2021}
}




## 5.2 Density-based Method
### 5.2.1 Embedding-based Method
@inproceedings{mahananobis18nips,
  title={A simple unified framework for detecting out-of-distribution samples and adversarial attacks},
  author={Lee, Kimin and Lee, Kibok and Lee, Honglak and Shin, Jinwoo},
  booktitle={NeurIPS},
  year={2018}
}

@inproceedings{likelihoodratio19nips,
  title={Likelihood ratios for out-of-distribution detection},
  author={Ren, Jie and Liu, Peter J and Fertig, Emily and Snoek, Jasper and Poplin, Ryan and DePristo, Mark A and Dillon, Joshua V and Lakshminarayanan, Balaji},
  booktitle={NeurIPS},
  year={2019}
}

@inproceedings{wang2020further,
  title={Further analysis of outlier detection with deep generative models},
  author={Wang, Ziyu and Dai, Bin and Wipf, David and Zhu, Jun},
  booktitle={NeurIPS},
  year={2020},
}

@inproceedings{vae20nips,
  title={Likelihood regret: An out-of-distribution detection score for variational auto-encoder},
  author={Xiao, Zhisheng and Yan, Qing and Amit, Yali},
  booktitle={NeurIPS},
  year={2020}
}

@inproceedings{dgmknow19nips,
  title={Do deep generative models know what they don't know?},
  author={Nalisnick, Eric and Matsukawa, Akihiro and Teh, Yee Whye and Gorur, Dilan and Lakshminarayanan, Balaji},
  booktitle={NeurIPS},
  year={2018}
}

@inproceedings{blur20iclr,
  title={Novelty detection via blurring},
  author={Choi, Sungik and Chung, Sae-Young},
  booktitle={ICLR},
  year={2020}
}

@inproceedings{ratiogm20iclr,
  title={Input complexity and out-of-distribution detection with likelihood-based generative models},
  author={Serr{\`a}, Joan and {\'A}lvarez, David and G{\'o}mez, Vicen{\c{c}} and Slizovskaia, Olga and N{\'u}{\~n}ez, Jos{\'e} F and Luque, Jordi},
  journal={ICLR},
  year={2020}
}

@article{bohm2020probabilistic,
  title={Probabilistic auto-encoder},
  author={B{\"o}hm, Vanessa and Seljak, Uro{\v{s}}},
  journal={arXiv preprint arXiv:2006.05479},
  year={2020}
}

@inproceedings{sintrovae21cvpr,
  title={Soft-IntroVAE: Analyzing and Improving the Introspective Variational Autoencoder},
  author={Daniel, Tal and Tamar, Aviv},
  booktitle={CVPR},
  year={2021}
}

### 5.2.2 Flow-based Method
@inproceedings{residualflow20cvpr,
  title={Deep residual flow for out of distribution detection},
  author={Zisselman, Ev and Tamar, Aviv},
  booktitle={CVPR},
  year={2020}
}

@inproceedings{whyflow20nips,
  title={Why normalizing flows fail to detect out-of-distribution data},
  author={Kirichenko, Polina and Izmailov, Pavel and Wilson, Andrew Gordon},
  booktitle={NeurIPS},
  year={2020}
}

@inproceedings{invert20nips,
  title={Understanding anomaly detection with deep invertible networks through hierarchies of distributions and features},
  author={Schirrmeister, Robin Tibor and Zhou, Yuxuan and Ball, Tonio and Zhang, Dan},
  booktitle={NeurIPS},
  year={2020}
}

### 5.2.3 Energy-based Method
@inproceedings{secretebm20iclr,
  title={Your classifier is secretly an energy based model and you should treat it like one},
  author={Grathwohl, Will and Wang, Kuan-Chieh and Jacobsen, J{\"o}rn-Henrik and Duvenaud, David and Norouzi, Mohammad and Swersky, Kevin},
  booktitle={ICLR},
  year={2019}
}

@inproceedings{energyood20nips,
  title={Energy-based out-of-distribution detection},
  author={Liu, Weitang and Wang, Xiaoyun and Owens, John D and Li, Yixuan},
  booktitle={NeurIPS},
  year={2020}
}

## 5.3 Distance-based Method

**[CVPR-2021]**
[Out-of-Distribution Detection Using Union of 1-Dimensional Subspaces]()
Zaeemzadeh, Alireza and Bisagno, Niccol{\`o} and Sambugaro, Zeno and Conci, Nicola and Rahnavard, Nazanin and Shah, Mubarak
> <details>
> <summary> class membership probabilities in . </summary>
> <p class="small" style="text-align:left">
> The cosine similarities between the extracted feature and the class vectors are used to compute the class membership probabilities, using a Union of 1-dimensional subspaces 
> </p>
> </details>


**[ECCV-2020]**
[A boundary based out-of-distribution classifier for generalized zero-shot learning](https://arxiv.org/abs/2008.04872)
Chen, Xingyu and Lan, Xuguang and Sun, Fuchun and Zheng, Nanning.


**[arXiv-2020]**
[Feature Space Singularity for Out-of-Distribution Detection](https://arxiv.org/abs/2011.14654)
Huang, Haiwen and Li, Zhihan and Wang, Lulu and Chen, Sishuo and Dong, Bin and Zhou, Xinyu
> <details>
> <summary> Distance to Feature Space Singularity can measure OOD.</summary>
> <p class="small" style="text-align:left">
> It is observed that in feature spaces, OOD samples concentrate near a Feature Space Singularity (FSS) point, and the distance from a sample to FSS measures the degree of OOD. It can be exlained that moving speeds of features of other data depend on their similarity to the training data. During training, they use generated uniform noise or validation data as OOD.
> </p>
> </details>


@inproceedings{gram20icml,
  title={Detecting out-of-distribution examples with gram matrices},
  author={Sastry, Chandramouli Shama and Oore, Sageev},
  booktitle={ICML},
  year={2020}
}

@inproceedings{duq20icml,
  title={Uncertainty estimation using a single deep deterministic neural network},
  author={Van Amersfoort, Joost and Smith, Lewis and Teh, Yee Whye and Gal, Yarin},
  booktitle={ICML},
  year={2020}
}


## 5.4 Meta-Learning-based Method
@inproceedings{oodmaml20nips,
  title={OOD-MAML: Meta-learning for few-shot out-of-distribution detection and classification},
  author={Jeong, Taewon and Kim, Heeyoung},
  journal={NeurIPS},
  year={2020}
}

@inproceedings{btaml20iclr,
  title={Learning to balance: Bayesian meta-learning for imbalanced and out-of-distribution tasks},
  author={Lee, Hae Beom and Lee, Hayeon and Na, Donghyun and Kim, Saehoon and Park, Minseop and Yang, Eunho and Hwang, Sung Ju},
  journal={ICLR},
  year={2020}
}

## 5.5 Hybrid Method and Discussion


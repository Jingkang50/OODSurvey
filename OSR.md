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



%% OSR Classification Model %%%%%%%%%%%%%%%%%%%%%%


%%% Post-hoc Calibration %
@article{cap14pami,
  title={Probability models for open set recognition},
  author={Scheirer, Walter J and Jain, Lalit P and Boult, Terrance E},
  journal={TPAMI},
  year={2014}
}


@article{evt90appmath,
  title={Extreme value theory},
  author={Smith, Richard L},
  journal={Handbook of applicable mathematics},
  year={1990},
}

@book{evt12book,
  title={Extreme value theory in engineering},
  author={Castillo, Enrique},
  year={2012},
  publisher={Elsevier}
}


@inproceedings{psvm14eccv,
  title={Multi-class open set recognition using probability of inclusion},
  author={Jain, Lalit P and Scheirer, Walter J and Boult, Terrance E},
  booktitle={ECCV},
  year={2014},
}

@inproceedings{openmax16cvpr,
  title={Towards open set deep networks},
  author={Bendale, Abhijit and Boult, Terrance E},
  booktitle={CVPR},
  year={2016}
}

@inproceedings{advopenmax17bmvc,
  title={Adversarial robustness: Softmax versus openmax},
  author={Rozsa, Andras and G{\"u}nther, Manuel and Boult, Terrance E},
  booktitle={BMVC},
  year={2017}
}


%%% Unknown Class Generation %
@inproceedings{gopenmax17bmvc,
  title={Generative openmax for multi-class open set classification},
  author={Ge, ZongYuan and Demyanov, Sergey and Chen, Zetao and Garnavi, Rahil},
  booktitle={BMVC},
  year={2017}
}

@inproceedings{osrci18eccv,
  title={Open set learning with counterfactual images},
  author={Neal, Lawrence and Olson, Matthew and Fern, Xiaoli and Wong, Weng-Keen and Li, Fuxin},
  booktitle={ECCV},
  year={2018}
}


@inproceedings{proser21cvpr,
  title={Learning Placeholders for Open-Set Recognition},
  author={Zhou, Da-Wei and Ye, Han-Jia and Zhan, De-Chuan},
  booktitle={CVPR},
  year={2021}
}

%% OSR Distance Model %%%%%%%%%%%%%%%%%%%%%%%%%%%%
@inproceedings{metric18bmvc,
  title={Metric learning for novelty and anomaly detection},
  author={Masana, Marc and Ruiz, Idoia and Serrat, Joan and van de Weijer, Joost and Lopez, Antonio M},
  booktitle={BMVC},
  year={2018}
}

@inproceedings{ndcc21cvpr,
  title={Learning Deep Classifiers Consistent With Fine-Grained Novelty Detection},
  author={Cheng, Jiacheng and Vasconcelos, Nuno},
  booktitle={CVPR},
  year={2021}
}

@inproceedings{peeler20cvpr,
  title={Few-shot open-set recognition using meta-learning},
  author={Liu, Bo and Kang, Hao and Li, Haoxiang and Hua, Gang and Vasconcelos, Nuno},
  booktitle={CVPR},
  year={2020}
}

@inproceedings{rpl20eccv,
  title={Learning open set network with discriminative reciprocal points},
  author={Chen, Guangyao and Qiao, Limeng and Shi, Yemin and Peng, Peixi and Li, Jia and Huang, Tiejun and Pu, Shiliang and Tian, Yonghong},
  booktitle={ECCV},
  year={2020}
}

@article{podn2020scireport,
  title={p-oDn: prototype-based open Deep network for open Set Recognition},
  author={Shu, Yu and Shi, Yemin and Wang, Yaowei and Huang, Tiejun and Tian, Yonghong},
  journal={Scientific reports},
  year={2020}
}

@inproceedings{snatcher21cvpr,
  title={Few-shot Open-set Recognition by Transformation Consistency},
  author={Jeong, Minki and Choi, Seokeon and Kim, Changick},
  booktitle={CVPR},
  year={2021}
}

%% OSR reconstruction Model %%%%%%%%%%%%%%%%%%%%%%%%%%%%
% Sparse Representation
@article{srosr16pami,
  title={Sparse representation-based open set recognition},
  author={Zhang, He and Patel, Vishal M},
  journal={TPAMI},
  year={2016},
}

@inproceedings{knda13cvpr,
  title={Kernel null space methods for novelty detection},
  author={Bodesheim, Paul and Freytag, Alexander and Rodner, Erik and Kemmler, Michael and Denzler, Joachim},
  booktitle={CVPR},
  year={2013}
}

@inproceedings{iknda17cvpr,
  title={Incremental kernel null space discriminant analysis for novelty detection},
  author={Liu, Juncheng and Lian, Zhouhui and Wang, Yi and Xiao, Jianguo},
  booktitle={CVPR},
  year={2017}
}

@inproceedings{rgraph17cvpr,
  title={Provable self-representation based outlier detection in a union of subspaces},
  author={You, Chong and Robinson, Daniel P and Vidal, Ren{\'e}},
  booktitle={CVPR},
  year={2017}
}

% Reconstruction Error
@inproceedings{crosr19cvpr,
  title={Classification-reconstruction learning for open-set recognition},
  author={Yoshihashi, Ryota and Shao, Wen and Kawakami, Rei and You, Shaodi and Iida, Makoto and Naemura, Takeshi},
  booktitle={CVPR},
  year={2019}
}

@article{gmvae20aaai,
  title={Open-Set Recognition with Gaussian Mixture Variational Autoencoders},
  author={Cao, Alexander and Luo, Yuan and Klabjan, Diego},
  journal={AAAI},
  year={2020}
}

@inproceedings{c2ae19cvpr,
  title={C2ae: Class conditioned auto-encoder for open-set recognition},
  author={Oza, Poojan and Patel, Vishal M},
  booktitle={CVPR},
  year={2019}
}

@inproceedings{cgdl20cvpr,
  title={Conditional gaussian distribution learning for open set recognition},
  author={Sun, Xin and Yang, Zhenning and Zhang, Chi and Ling, Keck-Voon and Peng, Guohao},
  booktitle={CVPR},
  year={2020}
}

@inproceedings{counterfactual21cvpr,
  title={Counterfactual zero-shot and open-set visual recognition},
  author={Yue, Zhongqi and Wang, Tan and Sun, Qianru and Hua, Xian-Sheng and Zhang, Hanwang},
  booktitle={CVPR},
  year={2021}
}


%% Hybrid Method %%%%%%%%%%%%%%%%%%%%%%%%%%%%
@inproceedings{gdfr20cvpr,
  title={Generative-discriminative feature representations for open-set recognition},
  author={Perera, Pramuditha and Morariu, Vlad I and Jain, Rajiv and Manjunatha, Varun and Wigington, Curtis and Ordonez, Vicente and Patel, Vishal M},
  booktitle={CVPR},
  year={2020}
}

@inproceedings{osad20eccv,
  title={Open-set adversarial defense},
  author={Shao, Rui and Perera, Pramuditha and Yuen, Pong C and Patel, Vishal M},
  booktitle={ECCV},
  year={2020},
}

@inproceedings{rdosr20eccv,
  title={Representative-Discriminative Learning for Open-set Land Cover Classification of Satellite Imagery},
  author={Baghbaderani, Razieh Kaviani and Qu, Ying and Qi, Hairong and Stutts, Craig},
  booktitle={ECCV},
  year={2020}
}

@inproceedings{openhybrid20eccv,
  title={Hybrid models for open set recognition},
  author={Zhang, Hongjie and Li, Ang and Guo, Jie and Guo, Yanwen},
  booktitle={ECCV},
  year={2020},
}
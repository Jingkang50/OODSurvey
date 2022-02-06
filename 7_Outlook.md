# 7. Challenges and Future Direction
- [7.1 Challenges](#7.1)
  - [7.1.1 Proper Evaluation and Benchmarking](#7.1.1)
  - [7.1.2 Outlier-free OOD Detection](#7.1.2)
  - [7.1.3 Tradeoff Between Classification and OOD Detection](#7.1.3)
  - [7.1.4 Real-world Benchmarks and Evaluations](#7.1.4)
- [7.2  Future Directions](#7.2)
  - [7.2.1 Methodologies across Sub-tasks](#7.2.1)
  - [7.2.2 OOD Detection & OOD Generalization](#7.2.2)
  - [7.2.3 OOD Detection & Open-Set Noisy Labels](#7.2.3)
  - [7.2.4 Theoretical Analysis](#7.2.4)

<a name="7.1"></a>
## 7.1 Challenges
<a name="7.1.1"></a>
### 7.1.1 Proper Evaluation and Benchmarking
We hope this survey can clarify the distinctions and connections of various sub-tasks, and help future works properly identify the target problem and benchmarks within the framework. The mainstream OOD detection works primarily focus on detecting semantic shifts.
Admittedly, the field of OOD detection can be very broad due to the diverse nature of distribution shifts. 
Such a broad OOD definition also leads to some challenges and concerns [[1, 2]](#7.1.1.ref), which advocate a clear specification of OOD type in consideration (e.g. semantic OOD, adversarial OOD, etc.) so that proposed solutions can be more specialized.
Besides, the motivation of detecting a certain distribution shift also requires clarification. While rejecting classifying samples with semantic shift is apparent, detecting sensory OOD should be specified to some meaningful scenarios to contextualize the necessity and practical relevance of the task.

We also urge the community to carefully construct the benchmarks and evaluations. It is noticed that early work [[3]](#7.1.1.ref) ignored the fact that some OOD datasets may contain images with ID categories, causing inaccurate performance evaluation. 
Fortunately, recent OOD detection works [[4, 5]](#7.1.1.ref) have realized this flaw and pay special attention to removing ID classes from OOD samples to ensure proper evaluation.

---
<a name="7.1.1.ref"></a>
[1] W. Gan, [“Language guided out-of-distribution detection,”](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2021/EECS-2021-139.pdf) 2021.

[2] F. Ahmed and A. Courville, [“Detecting semantic anomalies,”](https://ojs.aaai.org/index.php/AAAI/article/download/5712/5568) in AAAI, 2020

[3] D. Hendrycks and K. Gimpel, [“A baseline for detecting misclassified and out-of-distribution examples in neural networks,”](https://arxiv.org/pdf/1610.02136) in ICLR, 2017

[4] R. Huang and Y. Li, [“Mos: Towards scaling out-of-distribution detection for large semantic space,”](https://openaccess.thecvf.com/content/CVPR2021/papers/Huang_MOS_Towards_Scaling_Out-of-Distribution_Detection_for_Large_Semantic_Space_CVPR_2021_paper.pdf) in CVPR, 2021

[5] J. Yang, H. Wang, L. Feng, X. Yan, H. Zheng, W. Zhang, and Z. Liu, [“Semantically coherent out-of-distribution detection,”](http://openaccess.thecvf.com/content/ICCV2021/papers/Yang_Semantically_Coherent_Out-of-Distribution_Detection_ICCV_2021_paper.pdf) in ICCV, 2021

<a name="7.1.2"></a>
### 7.1.2 Outlier-free OOD Detection
The outlier exposure approach [[6]](#7.1.2.ref) imposes a strong assumption of the availability of OOD training data, which can be difficult to obtain in practice. Moreover, one needs to perform careful de-duplication to ensure that the outlier training data does not contain ID data. These restrictions may lead to inflexible solutions and prevent the adoption of methods in the real world. As with the recent taken-down of TinyImages dataset [[7]](#7.1.2.ref), it poses a reproducibility crisis for OE-based methods. Going forward, a major challenge for the field is to devise outlier-free learning objectives that are less dependent on auxiliary outlier dataset. 

---
<a name="7.1.2.ref"></a>
[6] D. Hendrycks, M. Mazeika, and T. Dietterich, [“Deep anomaly detection with outlier exposure,”](https://arxiv.org/pdf/1812.04606) in ICLR, 2019

[7] A. Torralba, R. Fergus, and W. T. Freeman, [“80 million tiny images: A large data set for nonparametric object and scene recognition,”](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.73.4858&rep=rep1&type=pdf) TPAMI, 2008.

<a name="7.1.3"></a>
### 7.1.3 Tradeoff Between Classification and OOD Detection
In OSR and OOD detection, it is important to achieve the dual objectives simultaneously: one for the ID task (e.g. image classification), another for the OOD detection task. For a shared network, an inherent trade-off may exist between the two tasks. Promising solutions should strive for both. These two tasks may or may not contradict each other, depending on the methodologies. For example, [[8]](#7.1.3.ref) advocated the integration of image classification and open-set recognition so that the model will possess the capability of discriminative recognition on known classes and sensitivity to novel classes at the same time.
[[9]](#7.1.3.ref) also showed that the ability of detecting novel classes can be highly correlated with its accuracy on the closed-set classes.
[[10]](#7.1.3.ref) demonstrated that optimizing for the cluster compactness of ID classes may facilitate both improved classification and distance-based OOD detection performance. Such solutions may be more desirable than ND, which develops a binary OOD detector separately from the classification model, and requires deploying two models. 

---
<a name="7.1.3.ref"></a>
[8] Z. Liu, Z. Miao, X. Zhan, J. Wang, B. Gong, and S. X. Yu, [“Largescale long-tailed recognition in an open world,”](http://openaccess.thecvf.com/content_CVPR_2019/papers/Liu_Large-Scale_Long-Tailed_Recognition_in_an_Open_World_CVPR_2019_paper.pdf)
 in CVPR, 2019.
[9] S. Vaze, K. Han, A. Vedaldi, and A. Zisserman, [“Open-set recognition: A good closed-set classifier is all you need,”](https://arxiv.org/pdf/2110.06207) arXiv preprint arXiv:2110.06207, 2021.

[10] J. Yang, H. Wang, L. Feng, X. Yan, H. Zheng, W. Zhang, and Z. Liu, [“Semantically coherent out-of-distribution detection,”](http://openaccess.thecvf.com/content/ICCV2021/papers/Yang_Semantically_Coherent_Out-of-Distribution_Detection_ICCV_2021_paper.pdf) in ICCV, 2021. 

<a name="7.1.4"></a>
### 7.1.4 Real-world Benchmarks and Evaluations
Current methods have been primarily evaluated on small data sets such as CIFAR.
It's been shown that approaches developed on the CIFAR benchmark might not translate effectively into ImageNet benchmark with a large semantic space, highlighting the need to evaluate OOD detection in a large-scale real-world setting.
Therefore, we encourage future research to evaluate on ImageNet-based OOD detection benchmark [[11]](#7.1.4.ref), as well as large-scale OSR benchmark [[12]](#7.1.4.ref), and test the limits of the method developed. Moreover, real-world benchmarks that go beyond image classification can be valuable for the research community. In particular, for safety-critical settings such as autonomous driving and medical imaging diagnosis, more specialized benchmarks are needed and should be carefully constructed. 

---
<a name="7.1.4.ref"></a>
[11] R. Huang and Y. Li, [“Mos: Towards scaling out-of-distribution detection for large semantic space,”](https://openaccess.thecvf.com/content/CVPR2021/papers/Huang_MOS_Towards_Scaling_Out-of-Distribution_Detection_for_Large_Semantic_Space_CVPR_2021_paper.pdf) in CVPR, 2021.

[12] S. Vaze, K. Han, A. Vedaldi, and A. Zisserman, [“Open-set recognition: A good closed-set classifier is all you need,”](https://arxiv.org/pdf/2110.06207) arXiv preprint arXiv:2110.06207, 2021.


<a name="7.2"></a>
## 7.2  Future Directions
<a name="7.2.1"></a>
### 7.2.1 Methodologies across Sub-tasks
Due to the inherent connections among different sub-tasks, their solution space can be shared and inspired from each other. For example, the recent emerging density-based OOD detection research can draw insights from the density-based AD methods that have been around for a long time.

<a name="7.2.2"></a>
### 7.2.2 OOD Detection & OOD Generalization
An open-world classifier should consider two tasks, i.e., being robust to covariate shift while being aware of the semantic shift. Existing works pursue these two goals independently. Recent work proposes a semantically coherent OOD detection framework [[1]](#7.2.2.ref) that encourages detecting semantic OOD samples while being robust to negligible covariate shift. Given the vague definition of OOD, [[2]](#7.2.2.ref) proposed a new formalization of OOD detection by explicitly taking into account the separation
between invariant features (semantic related) and environmental features (non-semantic). The work highlighted that spurious environmental features in the training set can significantly impact
OOD detection, especially when the label-shifted OOD data contains the spurious feature. Recent works on open long-tailed recognition [[3]](#7.2.2.ref), open compound domain adaptation [[4]](#7.2.2.ref), open-set domain adaptation [[5]](#7.2.2.ref) and open-set domain generalization [[6]](#7.2.2.ref) consider the potential existence of open-class samples.
Looking ahead, we envision great research opportunities on how OOD detection and OOD generalization can better enable each other [[7]](#7.2.2.ref), in terms of both algorithmic design and comprehensive performance evaluation.

---
<a name="7.2.2.ref"></a>
[1] J. Yang, H. Wang, L. Feng, X. Yan, H. Zheng, W. Zhang, and Z. Liu, [“Semantically coherent out-of-distribution detection,”](http://openaccess.thecvf.com/content/ICCV2021/papers/Yang_Semantically_Coherent_Out-of-Distribution_Detection_ICCV_2021_paper.pdf)  in ICCV, 2021.

[2] Y. Ming, H. Yin, and Y. Li, [“On the impact of spurious correlation for out-of-distribution detection,”](https://arxiv.org/pdf/2109.05642) in AAAI, 2022

[3] Z. Liu, Z. Miao, X. Zhan, J. Wang, B. Gong, and S. X. Yu, [“Large scale long-tailed recognition in an open world,”](http://openaccess.thecvf.com/content_CVPR_2019/papers/Liu_Large-Scale_Long-Tailed_Recognition_in_an_Open_World_CVPR_2019_paper.pdf) in CVPR, 2019.

[4] Z. Liu, Z. Miao, X. Pan, X. Zhan, D. Lin, S. X. Yu, and B. Gong, [“Open compound domain adaptation,”](http://openaccess.thecvf.com/content_CVPR_2020/papers/Liu_Open_Compound_Domain_Adaptation_CVPR_2020_paper.pdf) in CVPR, 2020.

[5] P. Panareda Busto and J. Gall, [“Open set domain adaptation,”](http://openaccess.thecvf.com/content_ICCV_2017/papers/Busto_Open_Set_Domain_ICCV_2017_paper.pdf) in ICCV, 2017.

[6] Y. Shu, Z. Cao, C. Wang, J. Wang, and M. Long, [“Open domain generalization with domain-augmented meta-learning,”](https://openaccess.thecvf.com/content/CVPR2021/papers/Shu_Open_Domain_Generalization_with_Domain-Augmented_Meta-Learning_CVPR_2021_paper.pdf) in CVPR, 2021

[7] Z. Liu, Z. Miao, X. Zhan, J. Wang, B. Gong, and S. X. Yu, [“Largescale long-tailed recognition in an open world,”](http://openaccess.thecvf.com/content_CVPR_2019/papers/Liu_Large-Scale_Long-Tailed_Recognition_in_an_Open_World_CVPR_2019_paper.pdf)
 in CVPR, 2019.
<a name="7.2.3"></a>
### 7.2.3 OOD Detection & Open-Set Noisy Labels
Existing methods of learning from open-set noisy labels focus on suppressing the negative effects of noise [[1, 2]](#7.2.3.ref). However,
the open-set noisy samples can be useful for outlier exposure [[3]](#7.2.3.ref) and potentially benefit OOD detection.
With a similar idea, the setting of open-set semi-supervised learning can be promising for OOD detection.
We believe the combination between OOD detection and the previous two fields can provide more insights and possibilities.

---
<a name="7.2.3.ref"></a>
[1] Y. Wang, W. Liu, X. Ma, J. Bailey, H. Zha, L. Song, and S.-T. Xia, [“Iterative learning with open-set noisy labels,”](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Iterative_Learning_With_CVPR_2018_paper.pdf)
 in CVPR, 2018.
 
[2] J. Li, C. Xiong, and S. C. Hoi, [“Mopro: Webly supervised learning with momentum prototypes,”](https://arxiv.org/pdf/2009.07995)
 ICLR, 2021.
 
[3] Z.-F. Wu, T. Wei, J. Jiang, C. Mao, M. Tang, and Y.-F. Li, [“Ngc: A unified framework for learning with open-world noisy data,”](https://openaccess.thecvf.com/content/ICCV2021/papers/Wu_NGC_A_Unified_Framework_for_Learning_With_Open-World_Noisy_Data_ICCV_2021_paper.pdf) in ICCV, 2021.

<a name="7.2.4"></a>
### 7.2.4 Theoretical Analysis
While most of the existing OOD detection works focus on developing effective approaches to obtain better empirical performance, the theoretical analysis remains largely underexplored. We hope future research can also contribute theoretical analyses and provide in-depth insights that help guide algorithmic development with rigorous guarantees. 

[1] Z. Fang, J. Lu, A. Liu, F. Liu, G. Zhang, [“Learning Bounds for Open-Set Learning”](https://arxiv.org/abs/2106.15792) in ICML, 2021.

[2] Peyman Morteza and Yixuan Li, [“Provable Guarantees for Understanding Out-of-distribution Detection,”](https://arxiv.org/abs/2112.00787) in AAAI, 2022


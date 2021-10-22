<a name="top"></a>
# 4. Multi-Class Novelty Detection & Open Set Recognition
- [4.1 Classfication](#4.1)
  - [4.1.1 EVT-based Calibration](#4.1.1)
  - [4.1.2 EVT-free Calibration](#4.1.2)
  - [4.1.3 Unknown Generation](#4.1.3)
  - [4.1.4 Label Space Redesign](#4.1.4)
- [4.2 Distance-based Method](#4.2)
- [4.3 Reconstruction](#4.3)
  - [4.3.1 Sparse Representation](#4.3.1)
  - [4.3.2 Reconstruction-Error](#4.3.2)



<a name="4.1"></a>
## 4.1 Classfication

**[TPAMI-2013]**
[Toward Open Set Recognition](https://ieeexplore.ieee.org/abstract/document/6365193)
<br>
**Authors:** Walter J. Scheirer, Anderson de Rezende Rocha, Archana Sapkota, Terrance E. Boult
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
**Authors:** Walter J. Scheirer, Lalit P. Jain, Terrance E. Boult
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
**Authors:** Lalit P. Jain, Walter J. Scheirer, Terrance E. Boult
<br>
**Institution:** University of Colorado, Colorado Springs; Harvard University; Securics
> <details>
> <summary>PI-SVM estimating the unnormalized posterior probability of class inclusion.</summary>
> <p style="text-align:left">
> Modeling positive training data at the decision boundary, where we can invoke the statistical EVT. A new algorithm called the PI-SVM is introduced for estimating the unnormalized posterior probability of multiple class inclusion.
> </p>
> </details>


**[CVPR-2016]**
[Towards open set deep networks](https://www.cv-foundation.org/openaccess/content_cvpr_2016/html/Bendale_Towards_Open_Set_CVPR_2016_paper.html)
<br>
**Authors:** Abhijit Bendale, Terrance E. Boult
<br>
**Institution:** University of Colorado, Colorado Springs
> <details>
> <summary>OpenMax: Replacing softmax layer with OpenMax and calibrating the confidence to predict novel class.</summary>
> <p style="text-align:left">
> This method uses the scores from the penultimate layer to estimate if the input is “far” from known training data.
> </p>
> </details>


**[BMVC-2017]**
[Adversarial robustness: Softmax versus openmax](https://arxiv.org/abs/1708.01697)
<br>
**Authors:** Andras Rozsa, Manuel Gunther, Terrance E. Boult
<br>
**Institution:** University of Colorado, Colorado Springs

<a name="4.1.2"></a>
### 4.1.2 EVT-free Calibration

**[CVPR-2019]**
[Deep transfer learning for multiple class novelty detection](https://openaccess.thecvf.com/content_CVPR_2019/html/Perera_Deep_Transfer_Learning_for_Multiple_Class_Novelty_Detection_CVPR_2019_paper.html)
<br>
**Authors:** Pramuditha Perera, Vishal M. Patel
<br>
**Institution:** Johns Hopkins University
 


**[CVPR-2020]**
[Generative-discriminative feature representations for open-set recognition](https://openaccess.thecvf.com/content_CVPR_2020/html/Perera_Generative-Discriminative_Feature_Representations_for_Open-Set_Recognition_CVPR_2020_paper.html)
<br>
**Authors:** Pramuditha Perera, Vlad I. Morariu, Rajiv Jain, Varun Manjunatha, Curtis Wigington, Vicente Ordonez, Vishal M. Patel
<br>
**Institution:** Johns Hopkins University; Adobe Research; University of Virginia
 


**[arXiv-2021]**
[M2iosr: Maximal mutual information open set recognition](https://arxiv.org/abs/2108.02373)
<br>
**Authors:** Xin Sun, Henghui Ding, Chi Zhang, Guosheng Lin, Keck-Voon Ling
<br>
**Institution:** Nanyang Technological University
 

<a name="4.1.3"></a>
### 4.1.3 Unknown Generation

**[BMVC-2017]**
[Generative openmax for multi-class open set classification](https://arxiv.org/abs/1707.07418)
<br>
**Authors:** ZongYuan Ge, Sergey Demyanov, Zetao Chen, Rahil Garnavi
<br>
**Institution:** IBM Research; Vision for Robotics Lab
 

**[ECCV-2018]**
[Open set learning with counterfactual images](https://openaccess.thecvf.com/content_ECCV_2018/html/Lawrence_Neal_Open_Set_Learning_ECCV_2018_paper.html)
<br>
**Authors:** Lawrence Neal, Matthew Olson, Xiaoli Fern, Weng-Keen Wong, Fuxin Li;
<br>
**Institution:** Oregon State University
 

**[CVPR-2021]**
[Learning Placeholders for Open-Set Recognition](https://openaccess.thecvf.com/content/CVPR2021/html/Zhou_Learning_Placeholders_for_Open-Set_Recognition_CVPR_2021_paper.html)
<br>
**Authors:** Da-Wei Zhou, Han-Jia Ye, De-Chuan Zhan
<br>
**Institution:** Nanjing University
 

**[TKDE-2020]**
[Collective decision for open set recognition](https://ieeexplore.ieee.org/abstract/document/9023939/)
<br>
**Authors:** Chuanxing Geng, Songcan Chen
<br>
**Institution:** Nanjing University
 

**[arXiv-2020]**
[One-vs-rest network-based deep probabil- ity model for open set recognition](https://arxiv.org/abs/2004.08067)
<br>
**Authors:** Jaeyeon Jang, Chang Ouk Kim
<br>
**Institution:** Yonsei University
 

**[EUSIPCO-2019]**
[Open-set recognition using intra-class splitting](https://ieeexplore.ieee.org/abstract/document/8902738)
<br>
**Authors:** Patrick Schlachter, Yiwen Liao, Bin Yang
<br>
**Institution:** University of Stuttgart
 

<a name="4.1.4"></a>
### 4.1.4 Label Space Redesign

**[Report-2021]**
[Language guided out-of-distribution detection](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2021/EECS-2021-139.pdf)
<br>
**Authors:** William Gan
<br>
**Institution:** UC, Berkeley
 

**[CVPR-2018]**
[Hierarchical novelty detection for visual object recognition](https://openaccess.thecvf.com/content_cvpr_2018/html/Lee_Hierarchical_Novelty_Detection_CVPR_2018_paper.html)
<br>
**Authors:** Kibok Lee, Kimin Lee† Kyle Min, Yuting Zhang, Jinwoo Shin† Honglak Lee
<br>
**Institution:** University of Michigan; Korea Advanced Institute of Science and Technology; Google Brain
 

**[CVPR-2021]**
[Mos: Towards scaling out-of-distribution detection for large semantic space](https://openaccess.thecvf.com/content/CVPR2021/html/Huang_MOS_Towards_Scaling_Out-of-Distribution_Detection_for_Large_Semantic_Space_CVPR_2021_paper.html)
<br>
**Authors:** Rui Huang, Yixuan Li
<br>
**Institution:** University of Wisconsin-Madison
 


**[NeurIPS-2018]**
[Out-of-distribution detection using multiple semantic label representations](https://arxiv.org/abs/1808.06664)
<br>
**Authors:** Gabi Shalev, Yossi Adi, Joseph Keshet
<br>
**Institution:** Bar-Ilan University 
 

**[arXiv-2021]**
[Learning transferable visual models from natural language supervision](https://arxiv.org/abs/2103.00020)
<br>
**Authors:** Alec Radford, Jong Wook Kim, Chris Hallacy, Aditya Ramesh, Gabriel Goh, Sandhini Agarwal, Girish Sastry, Amanda Askell, Pamela Mishkin, Jack Clark, Gretchen Krueger, Ilya Sutskever 
<br>
**Institution:** OpenAI
 


**[arXiv-2021]**
[Exploring the limits of out-of-distribution detection](https://arxiv.org/abs/2106.03004)
<br>
**Authors:** Stanislav Fort, Jie Ren, Balaji Lakshminarayanan
<br>
**Institution:** Stanford University; Google Research
 



<a name="4.2"></a>
## 4.2 Distance-based Method

**[BMVC-2018]**
[Metric learning for novelty and anomaly detection](https://arxiv.org/abs/1808.05492)
<br>
**Authors:** Masana, Marc and Ruiz, Idoia and Serrat, Joan and van de Weijer, Joost and Lopez, Antonio M
<br>
**Institution:** Universitat Autonoma de Barcelona, Bellaterra, Spain
 

**[Report]**
[p-odn: prototype- based open deep network for open set recognition](https://www.nature.com/articles/s41598-020-63649-6)
<br>
**Authors:** Yu Shu, Yemin Shi, Yaowei Wang, Tiejun Huang, Yonghong Tian
<br>
**Institution:** Peking University; Peng Cheng Laboratory
 

**[CVPR-2020]**
[Few-shot open-set recognition using meta-learning](https://openaccess.thecvf.com/content_CVPR_2020/html/Liu_Few-Shot_Open-Set_Recognition_Using_Meta-Learning_CVPR_2020_paper.html)
<br>
**Authors:** Bo Liu, Hao Kang, Haoxiang Li, Gang Hua, Nuno Vasconcelos
<br>
**Institution:** Wormpex AI Research; UC, San Diego
 

**[ECCV-2020]**
[Learning open set network with discriminative reciprocal points](https://link.springer.com/chapter/10.1007%2F978-3-030-58580-8_30)
<br>
**Authors:** Guangyao Chen, Limeng Qiao, Yemin Shi, Peixi Peng, Jia Li, Tiejun Huang, Shiliang Pu, Yonghong Tian
<br>
**Institution:** Peking University; Beihang University; Peng Cheng Laboratory; Hikvision Research Institute
 



**[CVPR-2019]**
[Classification-reconstruction learning for open-set recognition](https://openaccess.thecvf.com/content_CVPR_2019/html/Yoshihashi_Classification-Reconstruction_Learning_for_Open-Set_Recognition_CVPR_2019_paper.html)
<br>
**Authors:** Ryota Yoshihashi, Wen Shao, Rei Kawakami, Shaodi You2, Makoto Iida, Takeshi Naemura1
<br>
**Institution:** The University of Tokyo; Data61-CSIRO
 


**[AAAI-2020]**
[Open-set recognition with gaussian mixture variational autoencoders](https://www.aaai.org/AAAI21Papers/AAAI-3823.CaoA.pdf)
<br>
**Authors:** Alexander Cao, Yuan Luo, Diego Klabjan
<br>
**Institution:** Northwestern University
 

**[Machine Learning-2017]**
[Nearest neighbors distance ratio open-set classifier](https://link.springer.com/article/10.1007/s10994-016-5610-8)
<br>
**Authors:** Pedro R. Mendes Junior, Rafael de O. Werneck, Bernardo V. Stein, Daniel V. Pazinato, Waldir R. de Almeida, Otavio A. B. Penatti, Ricardo da S. Torres, Anderson Rocha, Roberto M. de Souza, Otavio A. B. Penatti
<br>
**Institution:** University of Campinas; SAMSUNG Research Institute
 



<a name="4.3"></a>
## 4.3 Reconstruction

<a name="4.3.1"></a>
### 4.3.1 Sparse Representation 

**[TPAMI-2016]**
[Sparse representation-based open set recognition](https://ieeexplore.ieee.org/abstract/document/7577876)
<br>
**Authors:** He Zhang, Vishal M. Patel
<br>
**Institution:** Rutgers University
> <details>
> <summary>SROSR models the tails of the matched and sum of non-matched reconstruction error distributions.</summary>
> <p style="text-align:left">
> This method model the tail of the above two error distributions using the statistical EVT, and the confidence scores corresponding to the tail distributions of a novel test sample are then fused to determine its identity. Notice that the hidden embedding during reconstruction is regularized by sparsity.
> </p>
> </details>

**[CVPR-2013]**
[Kernel null space methods for novelty detection](https://openaccess.thecvf.com/content_cvpr_2013/html/Bodesheim_Kernel_Null_Space_2013_CVPR_paper.html)
<br>
**Authors:** Paul Bodesheim, Alexander Freytag, Erik Rodner, Michael Kemmler, Joachim Denzler
<br>
**Institution:** University Jena; UC Berkeley


**[CVPR-2017]**
[Incremental kernel null space discriminant analysis for novelty detection](https://openaccess.thecvf.com/content_cvpr_2017/html/Liu_Incremental_Kernel_Null_CVPR_2017_paper.html)
<br>
**Authors:** Juncheng Liu, Zhouhui Lian, Yi Wang, Jianguo Xiao
<br>
**Institution:** Peking University; Dalian University 
 



<a name="4.3.2"></a>
### 4.3.2 Reconstruction-Error 


**[CVPR-2019]**
[C2AE: Class Conditioned Auto-Encoder for Open-Set Recognition](https://openaccess.thecvf.com/content_CVPR_2019/html/Oza_C2AE_Class_Conditioned_Auto-Encoder_for_Open-Set_Recognition_CVPR_2019_paper.html)
<br>
**Authors:** Poojan Oza, Vishal M. Patel
<br>
**Institution:** Johns Hopkins University
 


**[CVPR-2020]**
[Conditional gaussian distribution learning for open set recognition](https://openaccess.thecvf.com/content_CVPR_2020/html/Sun_Conditional_Gaussian_Distribution_Learning_for_Open_Set_Recognition_CVPR_2020_paper.html)
<br>
**Authors:** Xin Sun, Zhenning Yang, Chi Zhang, Keck-Voon Ling, Guohao Peng
<br>
**Institution:** Nanyang Technological University
 

**[CVPR-2021]**
[Counterfactual zero-shot and open-set visual recognition](https://openaccess.thecvf.com/content/CVPR2021/html/Yue_Counterfactual_Zero-Shot_and_Open-Set_Visual_Recognition_CVPR_2021_paper.html)
<br>
**Authors:** Zhongqi Yue, Tan Wang, Qianru Sun, Xian-Sheng Hua, Hanwang Zhang
<br>
**Institution:** Nanyang Technological University; Singapore Management University; Alibaba Damo Academy



**[ECCV-2020]**
[Open-set adversarial defense](https://link.springer.com/chapter/10.1007%2F978-3-030-58520-4_40)
<br>
**Authors:** Rui Shao, Pramuditha Perera, Pong C. Yuen, Vishal M. Patel
<br>
**Institution:** Hong Kong Baptist University; AWS AI Labs; Johns Hopkins University

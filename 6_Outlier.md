 <a name="top"></a>
# 6. Outlier Detection
- [6.1 Density-based Method](#6.1)
- [6.2 Distance](#6.2)
  - [6.2.1 Cluster-based Method](#6.2.1)
  - [6.2.2 Graph-based Method](#6.2.2)
- [6.3 Classification-based Method](#6.3)


Outlier detection (OD) requires the observation of all samples and aims to detect those that deviate significantly from the majority distribution.
Therefore, their approaches are usually transductive, rather than inductive.



<a name="6.1"></a>
## 6.1 Density-based Method

**[BMC-2014]**
[Estimating the sample mean and standard deviation from the sample size, median, range and/or interquartile range](https://link.springer.com/article/10.1186/1471-2288-14-135).
<br>
**Authors:** Xiang Wan, Wenqian Wang, Jiming Liu, Tiejun Tong
<br>
**Institution:** Hong Kong Baptist University; Northwestern University
 

**[SIGMOD-2000]**
[Lof: identifying density-based local outliers](https://dl.acm.org/doi/abs/10.1145/342009.335388).
<br>
**Authors:** Markus M. Breunig, Hans-Peter Kriegel, Raymond T. Ng, Jorg Sander
<br>
**Institution:** University of Munich; University of British Columbia
 

**[PAKDD-2002]**
[Enhancing effectiveness of outlier detections for low density patterns](https://link.springer.com/chapter/10.1007/3-540-47887-6_53).
<br>
**Authors:** Jian Tang, Zhixiang Chen, Ada Wai-chee Fu, David W. Cheung
<br>
**Institution:** Chinese University of Hong Kong; University of Texas; University of Hong Kong
 

**[ACM-2009]**
[Loop: local outlier probabilities](https://dl.acm.org/doi/abs/10.1145/1645953.1646195).
<br>
**Authors:** Hans-Peter Kriegel, Peer Kroger, Erich Schubert, Arthur Zimek
<br>
**Institution:** Ludwig-Maximilians University
 

**[DMKD-2012]**
[Local outlier detection reconsidered: a generalized view on locality with applications to spatial, video, and network outlier detection](https://link.springer.com/article/10.1007/s10618-012-0300-z).
<br>
**Authors:** Erich Schubert, Arthur Zimek, Hans-Peter Kriegel 
<br>
**Institution:** Ludwig-Maximilians-University; University of Alberta
 

**[ACM-1981]**
[Random sample consensus: a paradigm for model fitting with applications to image analysis and automated cartography](https://dl.acm.org/doi/abs/10.1145/358669.358692).
<br>
**Authors:** Martin A. Fischler, Robert C. Bolles
<br>
**Institution:** SRI International
 

**[WIREs-2011]**
[Robust statistics for outlier de- tection](https://wires.onlinelibrary.wiley.com/doi/abs/10.1002/widm.2).
<br>
**Authors:** Peter J. Rousseeuw, Mia Hubert
<br>
**Institution:** Katholieke University
 


**[NeurIPS-2018]**
[Efficient anomaly detection via matrix sketching](https://arxiv.org/abs/1804.03065).
<br>
**Authors:** Vatsal Sharan, Parikshit Gopalan, Udi Wieder
<br>
**Institution:** Stanford University; VMware Research
 
<a name="6.2"></a>
## 6.2 Distance


<a name="6.2.1"></a>
### 6.2.1 Cluster-based Method
The most basic OD method model the entire dataset with the Gaussian distribution, and flag the samples over three standard deviations from the mean.


**[KDD-1996]**
[A density-based algorithm for discovering clusters in large spatial databases with noise](https://www.aaai.org/Papers/KDD/1996/KDD96-037.pdf?source=post_page).
<br>
**Authors:** Martin Ester, Hans-Peter Kriegel, Jiirg Sander, Xiaowei Xu
<br>
**Institution:** University of Munich
 


**[ECML-2007]**
[Class noise mitigation through instance weighting](https://link.springer.com/chapter/10.1007/978-3-540-74958-5_71).
<br>
**Authors:** Umaa Rebbapragada, Carla E. Brodley
<br>
**Institution:** Tufts University
 



<a name="6.2.2"></a>
### 6.2.2 Graph-based Method
Similar to "three standard deviations" rules under the assumption that the data follows normal distribution, interquartile range can also be used to identify outliers.

**[DMKD-2014]**
[Graph based anomaly detection and description: a survey](https://link.springer.com/article/10.1007/s10618-014-0365-y).
<br>
**Authors:** Leman Akoglu; Hanghang Tong; Danai Koutra 
<br>
**Institution:** Stony Brook University, City University of New York, Carnegie Mellon University
 


**[SIGKDD-2003]**
[Graph-based anomaly detection](https://dl.acm.org/doi/abs/10.1145/956750.956831).
<br>
**Authors:** Caleb C. Noble, Diane J. Cook
<br>
**Institution:** University of Texas
 


**[ICTAI-2007]**
[Spatial outlier detection: a graph-based approach](https://ieeexplore.ieee.org/abstract/document/4410296).
<br>
**Authors:** Yufeng Kou, Chang-Tien Lu, Raimundo F. Dos Santos
<br>
**Institution:** Virginia Polytechnic Institute and State University
 


**[ICCSE-2012]**
[A graph-based clustering algorithm for anomaly intrusion detection](https://ieeexplore.ieee.org/abstract/document/6295306).
<br>
**Authors:** Zhou Mingqiang, Huang Hui, Wang Qian
<br>
**Institution:** Chongqing University
 


**[ACM-2020]**
[Webly supervised image classification with metadata: Automatic noisy label correction via visual-semantic graph](https://dl.acm.org/doi/abs/10.1145/3394171.3413952).
<br>
**Authors:** Jingkang Yang, Weirong Chen, Litong Feng, Xiaopeng Yan, Huabin Zheng, Wayne Zhang
<br>
**Institution:** Sensetime Research; Rice University; The Chinese University of Hong Kong; Shanghai Jiao Tong University
 



<a name="6.3"></a>
## 6.3 Classification-based Method

**[-2002]**
[One-class classification: Concept learning in the absence of counter-examples](https://www.elibrary.ru/item.asp?id=5230402).
<br>
**Authors:** Tax D.M.J
<br>
**Institution:** Technische Universiteit Delft
 

**[ICMI-2018]**
[Deep one-class classification](http://proceedings.mlr.press/v80/ruff18a).
<br>
**Authors:** Lukas Ruff, Robert Vandermeulen, Nico Goernitz, Lucas Deecke, Shoaib Ahmed Siddiqui, Alexander Binder, Emmanuel Muller, Marius Kloft 
<br>
**Institution:** Humboldt University; Hasso Plattner Institute; TU Kaiserslautern; TU Berlin; University of Edinburgh; DFKI GmbH; Singapore University of Technology and Design
 

**[ICDM-2008]**
[Isolation forest](https://ieeexplore.ieee.org/abstract/document/4781136/).
<br>
**Authors:** Fei Tony Liu, Kai Ming Ting, Zhi-Hua Zhou
<br>
**Institution:** Monash University; Nanjing University
 

**[CVPR-2017]**
[Learning from noisy labels with distillation](https://openaccess.thecvf.com/content_iccv_2017/html/Li_Learning_From_Noisy_ICCV_2017_paper.html).
<br>
**Authors:** Yuncheng Li, Jianchao Yang, Yale Song, Liangliang Cao, Jiebo Luo, Li-Jia Li
<br>
**Institution:** Snap Inc.; Yahoo Research
 

**[ICLR-2020]**
[Self: Learning to filter noisy labels with self-ensembling](https://arxiv.org/abs/1910.01842).
<br>
**Authors:** Duc Tam Nguyen, Chaithanya Kumar Mummadi, Thi Phuong Nhung Ngo, Thi Hoai Phuong Nguyen, Laura Beggel, Thomas Brox
<br>
**Institution:**  University of Freiburg; Bosch Research; Bosch Center for AI; Karlsruhe Institute of Technology
 

**[NIPS-2018]**
[Co-teaching: Robust training of deep neural networks with extremely noisy labels](https://arxiv.org/abs/1804.06872).
<br>
**Authors:** Bo Han, Quanming Yao, Xingrui Yu, Gang Niu, Miao Xu, Weihua Hu, Ivor Tsang, Masashi Sugiyama
<br>
**Institution:** University of Technology Sydney; RIKEN; 4Paradigm Inc.; Stanford University; University of Tokyo
 

**[ECCV-2020]**
[Webly supervised image classification with self- contained confidence](https://link.springer.com/chapter/10.1007%2F978-3-030-58598-3_46).
<br>
**Authors:** Jingkang Yang, Litong Feng, Weirong Chen, Xiaopeng Yan, Huabin Zheng, Ping Luo, Wayne Zhang
<br>
**Institution:** SenseTime Research; Rice University; The Chinese University of Hong Kong; The University of Hong Kong
 






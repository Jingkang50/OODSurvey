 <a name="top"></a>
# 2. Taxonomy
- [2.1 Anomaly Detection](#2.1)
  - [2.1.1 Sensory Anomaly Detection](#2.1.1)
  - [2.1.2 Semantic Anomaly Detection](#2.1.2)
- [2.2 Novelty Detection](#2.2)
  - [2.2.1 One-Class Novelty Detection](#2.2.1)
  - [2.2.2 Multi-Class Novelty Detection](#2.2.2)
- [2.3 Open Set Recognition](#2.3)
- [2.4 Out-of-Distribution Detection](#2.4)
- [2.5 Outlier Detection](#2.5)


<a name="2.1"></a>
## 2.1 Anomaly Detection
> *"All normals are alike; each anomaly is abnormal in its own way." - Adapted from "Anna Karenina", by Leo Tolstoy*

Anomaly detection (AD) aims to detect any anomalous samples that are deviated from the predefined normality during testing. The deviation can happen due to either covariate shift or semantic shift, while assuming the other distribution shift do not exist. This leads to two sub-tasks: sensory AD and semantic AD, respectively.

<a name="2.1.1"></a>
### 2.1.1 Sensory AD
Sensory AD detects test samples with covariate shift, under the assumption that normalities come from the same covariate distribution. No semantic shift takes place in sensory AD settings. 

<a name="2.1.2"></a>
### 2.1.2 Semantic AD
Semantic AD detects test samples with label shift, assuming that normalities come from the same semantic distribution (category), i.e., normalities should belong to only one class. No covariate shift happens in semantic AD settings.

Two broad categories of anomaly detection techniques exist. In the standard unsupervised AD setting, all given training samples are normal samples. The (semi-)supervised AD setting requires a dataset that has been labeled as `normal` and `abnormal`, and involves training a model explicitly. 


<a name="2.2"></a>
## 2.2 Novelty Detection
> *"Admitting one’s ignorance is the first step in acquiring knowledge.” - Socrates*

Novelty detection aims to detect any test samples that do not fall into any training category.
The detected novel samples are usually prepared for future constructive procedures, such as later specialized analysis, or incremental learning of the model itself.
Based on the number of training classes, ND contains two different settings:
<a name="2.2.1"></a>
### 2.2.1 One-class novelty detection
One-class novelty detection (`one-class ND`): only one class exists in the training set;
<a name="2.2.2"></a>
### 2.2.2 Multi-class novelty detection
Multi-class novelty detection (`multi-class ND`): multiple classes exist in the training set. It is worth noting that despite having many ID classes, the goal of multi-class ND is only to distinguish novel samples from ID. 

Both one-class and multi-class ND are formulated as binary classification problems.

<a name="2.3"></a>
## 2.3 Open Set Recognition
> *”To know what you know and what you do not know, that is true knowledge.” - Confucius*

OSR requires the multi-class classifier to simultaneously: 
1) accurately classify test samples that from `known known classes`;
2) detect test samples from `unknown unknown classes`.


<a name="2.4"></a>
## 2.4 Out-of-Distribution Detection
Out-of-distribution detection aims to detect test samples with non-overlapping labels w.r.t training data. 
Formally, test samples in the OOD detection setting come from the distribution with semantic shift from ID.
The ID can contain a single class or multiple classes.
When multiple classes exist in training, OOD detection should NOT harm the ID classification capability.


<a name="2.5"></a>
## 2.5 Outlier Detection
> *”Outliers: Escape from Ordinary.”*

Different from all previous sub-tasks, whose in-distribution is defined during training, the `in-distribution` for outlier detection refers to the majority of the observations. Outliers may exist due to semantic shift or covariate shift.

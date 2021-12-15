# Wealy-supervised lesion analysis with a CNN-based framework for COVID-19

## Abstract
Lesions of COVID-19 can be visualized clearly by chest CT images, therefore, providing valuable evidence for clinicians when making a diagnosis. However, due to the variety of COVID-19 lesions and the complexity of the manual delineation procedure, automatic analysis of lesions with unknown and diverse types from a CT image remains a challenging task. In this paper we propose a weakly-supervised framework for this task, requiring only a series of normal and abnormal CT images without the need for annotations of the specific locations and types of lesions. Specifically, this framework employs a deep learning-based diagnosis branch for the classification of the CT image and then leverages a lesion identification branch to capture multiple types of lesions. We verify our framework on publicly available datasets and CT data collected from 13 patients of the First Affiliated Hospital of Shantou University Medical College, China. The results show that the proposed framework can achieve state-of-the-art diagnosis prediction, and the extracted lesion features are capable of distinguishing between lesions showing ground glass opacity and consolidation. Further exploration also demonstrates that this framework has the potential to discover lesion types that have not been reported and can potentially be generalized to lesion detection of other chest-based diseases.

![截屏2021-12-07 20 11 14](https://user-images.githubusercontent.com/61356011/145026947-c8f8693a-7b92-4e0c-bad7-ca55aa7fbef0.png)
	

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; **The proposed framework**



# Dataset 
I did not update the original dataset that support our findings in this repository, but those datasets can easily obtained from: Radio-1 repository at http://medicalsegmentation.com/covid19/, COVIDx2a repository at https://github.com/haydengunraj/COVIDNet-CT,  CNCB repository at http://medicalsegmentation.com/covid19/. Besides, the subset of preprocessed lung CT images can be download from https://ieee-dataport.org/documents/covid-19-lung-images. If you find this data useful we will be happy if you cite 'Kaichao Wu, April 20, 2021, "COVID-19 Lung images", IEEE Dataport, doi: https://dx.doi.org/10.21227/fxcx-zh58. More details about the dataset can be seen in our paper: [Weakly-supervised lesion analysis with a CNN-based framework for COVID-19](http://iopscience.iop.org/article/10.1088/1361-6560/ac4316)
 
And if you find this repo is helpful to you, please cite our paper by:
```
@Article{Wu2021,
 author   = {Wu, Kaichao and Jelfs, Beth and Ma, Xiangyuan and Ke, Ruitian and Tan, Xuerui and Fang, Qiang},
 journal  = {Physics in Medicine & Biology},
 title    = {Weakly-supervised lesion analysis with a CNN-based framework for COVID-19},
 year     = {2021},
 url      = {http://iopscience.iop.org/article/10.1088/1361-6560/ac4316}
 }
```
 
# Model
The general structure of souce file for our model follows the below steps: 
#### 1. Preprocessing: Get lung area using Morphological operation
#### 2. Traing branch for diagnosis
#### 3. Lesion analysis branch
#### 4. Model evaluation
#### 5. Showing detected lesion
#### 6. Capture the detected lesion feature 
#### 7. Clustering the feature 
#### 8. Visualization
#### 9. Model comparsion
The complete framework can be seen in **Model\COVID_lesion.ipynb**, and the initial feature clustering method can be seen in **Model\lesion feature clustering and showing.ipynb**. In the Model folder，the lesion folder contains the lesion clustering and viuslization results. The diagnosis model weights and kmeans weights can be seen in 
**Model\models** folder. You can load "FeCNN-fold1-09-0.9940.hdf5" to fine tune the model.


**More detalis realted to the framework can be seen in a PPT file named seventh.pptx, which I reported it in my seventh weekly group meeting.**


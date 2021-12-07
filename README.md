# Wealy-supervised lesion analysis with a CNN-based framework for COVID-19

## Abstract
Lesions of COVID-19 can be visualized clearly by chest CT images, therefore, providing valuable evidence for clinicians when making a diagnosis. However, due to the variety of COVID-19 lesions and the complexity of the manual delineation procedure, automatic analysis of lesions with unknown and diverse types from a CT image remains a challenging task. In this paper we propose a weakly-supervised framework for this task, requiring only a series of normal and abnormal CT images without the need for annotations of the specific locations and types of lesions. Specifically, this framework employs a deep learning-based diagnosis branch for the classification of the CT image and then leverages a lesion identification branch to capture multiple types of lesions. We verify our framework on publicly available datasets and CT data collected from 13 patients of the First Affiliated Hospital of Shantou University Medical College, China. The results show that the proposed framework can achieve state-of-the-art diagnosis prediction, and the extracted lesion features are capable of distinguishing between lesions showing ground glass opacity and consolidation. Further exploration also demonstrates that this framework has the potential to discover lesion types that have not been reported and can potentially be generalized to lesion detection of other chest-based diseases.


	


![截屏2021-12-07 20 11 14](https://user-images.githubusercontent.com/61356011/145026947-c8f8693a-7b92-4e0c-bad7-ca55aa7fbef0.png)
	&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; **The proposed framework**


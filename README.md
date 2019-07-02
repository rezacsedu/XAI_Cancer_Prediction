## Explainable Prediction of Cancer Types Based on Gene Expression Data
Code and supplementary materials for the following paper:

* "Explainable Prediction of Cancer Types Based on Gene Expression Data" submitted to The 19th annual IEEE International Conference on Bioinformatics and Bioengineering(BIBE 2019) to be held in Greece. 

### Methods
In this paper, we collect genomics data about 9,074 cancer patients covering 33 different cancer types from The Cancer Genome Atlas(TCGA) and train a CNN and VGG16 networks using guided-gradient class activation map(GradCAM). Then we identify most significant biomarkers and rank top genes across different cancer types based on mean absolute impact. Both models show high confidence at predicting different cancer types correctly at least 94% of the cases. To provide comparison with baselines, we further identify top genes for each cancer type and cancer specific driver genes using gradient boosted trees and SHapley Additive exPlanations(SHAP), which are further validated with the annotation from the TumorPortal.

### Data collections
Gene expression about 33 different tumor types have been downloaded from The Cancer Genome Atlas(TCGA) portal covering 9,074 samples. Refer to https://github.com/rezacsedu/XAI_Cancer_Pred/tree/master/Data for details about the data. 

### Data availability
The preprocessed data can be downloaded from the following link with the password of '123' (without quote). 

### A quick instructions on using GradCAM and ranking important biomarkers
A quick example on a small dataset can be performed as follows: 
* $ cd GradCAM_FI
* $ python3 load_data.py (make sure that the data in CSV format in the 'data' folder)
* $ python3 model.py
* $ python3 grad_cam.py

### Examples of using SHAP and Gradient Boosted Trees
Refer the Python notebook (https://github.com/rezacsedu/XAI_Cancer_Pred/blob/master/Notebooks/GeneExpression_Classification_SHAP_XBoost.ipynb) to get an idea how to use SHAP and Gradient Boosted Trees to generate feature importance. 

### Citation request
If you use the code of this repository in your research, please consider citing the folowing papers:

    @inproceedings{karim2019XAI,
        title={Explainable Prediction of Cancer Types Based on Gene Expression Data},
        author={Karim, Md Rezaul and Beyan Deniz and Decker, Stefan},
        booktitle={The 19th annual IEEE International Conference on Bioinformatics and Bioengineering (BIBE 2019)},
        year={2019}
    }

### Contributing
For any questions, feel free to open an issue or contact at rezaul.karim@rwth-aachen.de

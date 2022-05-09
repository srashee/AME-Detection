# AME-Detection

## Objective
The objective of this project is to implement a context aware RNN based on
the original authors' work modified with the data being trained and
validated with MIMIC III data

## Prerequisites
Word Embeddings created from MIMIC III Dicharge notes
Labeled MIMIC III discharge notes
Conda Environment created with conda-final-project.yml

### Creating a Conda environment for this project
```
conda env create -f conda-final-project.yml
conda activate dlh-ame-detection
```

### Creating Word Embeddings for Input
Discharge Notes from MIMIC III as a csv file located at
../data/disch_notes_small.csv

OR from MIMIC III using this repository
https://github.com/3778/icd-prediction-mimic

### Word2Vec Model
You can follow the Jupyter Notebook to generate word embeddings from
MIMIC III discharge notes. In our project we implemented the same 
model as the original authors. A skipgram gensim.models.Word2Vec 
to create the word embeddings. 

### Creating labeled data
For the reproduction of this paper we manually labeled discharge notes
that indicated an adverse medical event. The definition of an adverse
medical event can be found below

### Definition of AME as concerned with this project 
Regarding the target AME, we selected the three typical types of
adverse cardiac events of CVD as the classification labels, i.e., ischemia
(including myocardial infarction and angina), revascularization (e.g.,
the surgery of Percutaneous Coronary Intervention (PCI) and Coronary
Artery Bypass Graft (CABG)) and bleeding events (including puncture
site bleeding, gastrointestinal bleeding and intracranial hemorrhage)

## Usage
The code can be run as a Jupyter Notebook by running ame-detection-final.ipynb
if the prerequisites are met.

## Model
The context aware RNN model can now be trained and evaluated after 
completing the steps above. We load the discharge note word embeddings,
labeled word embeddings and we fit the model. 


## Citation

Chu, J., Dong, W., He, K., Duan, H.,; Huang, Z. (2018). Using neural attention networks to detect adverse medical events from electronic health records. Journal of Biomedical Informatics, 87, 118–130. https://doi.org/10.1016/j.jbi.2018.10.002 


Zju-Bmi. (n.d.). Zju-BMI/Ame-detection. GitHub. Retrieved May 8, 2022, from https://github.com/ZJU-BMI/AME-detection 

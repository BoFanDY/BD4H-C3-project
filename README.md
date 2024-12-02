# Final project
# Bo Fan, Surya Garikipati
# Team C3

# code file: 
main_distcare_reproduce.ipynb
gru_transfer_distcare.ipynb
mlp_distcare.ipynb

## Description
In this work, we reproduced the work shown in the paper "Distilling Knowledge from Publicly Available Online EMR Data to Emerging Epidemic for Prognosis". We reproduce the DistCare model, perfomed data processing, conducted experimetns and obtained reproduced results. Additionally, we developed and implemented some customized models using similar ideas from the paper and achieved comparable results. All codes, datasets and pre-trained files are available in our repo
https://github.com/BoFanDY/BD4H-C3-project

## Data files
THJ covid-19 data file
training data: ""/data/Tongji/time_series_375_prerpocess_en.xlsx"
test data: "data/Tongji/time_series_test_110_preprocess_en.xlsx"

## Packages used
1. pandas
2. torch
3. sklearn
4. numpy
5. matplotlib
6. random
7. copy
8. pickle

## Download instruction
Please go to our GitHub repo or our google drive folder to download all the files
GitHub: https://github.com/BoFanDY/BD4H-C3-project
Google drive: https://drive.google.com/drive/folders/1ARy06DLXwpaSkOj6r8AoAD5P_UjpZIa4?usp=share_link


## pretrained model files
pre-trained models are in the folder "/model" folder
The pre-trained mdoel file we used is
".model/pretrained-challenge-front-fill-2covid-noteacher"



## Functionality of scripts.
# "main_distcare_reproduce.ipynb"
- `def generate_clearn_train_datasets`: function for data post processing.

- 'class MLP': class of multi-layer neural netowrk model.

- "def evaluate_different_training_volume": function to conduct experiments that generates performance of TJH test data with model trained with different training dataset volumnes.

- "def categorize": function to categorize label to defined groups

- "PCA": code blocks to perform PCA clustering

- "class single attention": class of creating attention layer in distcare model

- "class Final_AttentionQKV": class of creating qkv attention layer in distcare model

- "class MultiHeadedAttention": class of creating multihead attention layer in distcare model.

- "class LayerNorm": customized normalization layer

- "class sublayerconnection": customized layer containing one normalziation layer and one dropout layer

- "class distcare_teacher": the class of distcare teacher model

- "class distcare_student": the class of distcare student model

- "class distcare_target": the class of the distcare target model

# "gru_transfer_distcare.ipynb"
- "def generate_clearn_train_datasets": function for data post processing.

- "class GRUTeacherModel": class of teacher model in our customized GRU transfer learning model

- "class GRUStudentModel": class of student model in our customized GRU transfer learning model

- "def evaluate_different_training_volume": function to conduct experiments that generates performance of TJH test data with model trained with different training dataset volumnes.

- "def categorize": function to categorize label to defined groups

- "def plot_confusion_matrix": function to generate confusion matrix and plot

# "mlp_distcare.ipynb"
- "def generate_clearn_train_datasets": function for data post processing.

- "class MLP": class of our customized multi-layer neural network model.

- "def categorize": function to categorize label to defined groups



## Usage
1. train and test on TJH dataset using DistCare model:
Run entire "main_distcare_reproduce.ipynb" file to load and post-process data, create, train DistCare model and obtained results on tjh test data.

2. train and test on TJH dataset using custermized GRU transfer model:
Run entire "gru_trainsfer_distcare.ipynb" file to load and post-process data, create, train GRU transfer learning model and obtained results on tjh test 

3. train and test on TJH dataset using custermized MLP:
Run entire "mlp_distcare.ipynb" file to load and post-process data, create, train MLP model and obtained results on tjh test 


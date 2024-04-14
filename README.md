# CS598 DLH Group 104

Will Charles(wc40@illinois.edu) 
Hanfei Deng(hdeng11@illinois.edu) 
Stefan Wang(yifanw23@illinois.edu)


# PyTorch implementation of **CASS**, from the following papers for:


[CASS: Cross Architectural Self-Supervision for Medical Image Analysis](https://arxiv.org/abs/2206.04170). 

# Original Github Repo
https://github.com/pranavsinghps1/CASS

# Dateset Used
[Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset). 

# Explanation of Files 

## requirements.txt

This file includes all packages we use for this model

##
### DL4H_Team_104.ipynb
This file contains the everything you might need to run CASS. It uses the brain tumor MRI dataset and contains the model configuration, training and decleration. This file is a jupyter notebook. Please run it sequentially.

### cass-r50-isic.pt

This file contains the CNN model after the CASS pretraining

### cass-r50-vit-isic.pt

This file contains the Vit model after the CASS pretraining

### CASS-ViT-part-ft.pt
This file contains the Vit model after fine tuning for one epoche.

### CASS-CNN-part-ft.pt
This file contains the CNN model after fine tuning for one epoche.


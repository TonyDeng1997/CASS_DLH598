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

# Instructions 
To run with our exact configuration, first set up a virtual machine on Google’s compute engine. 
- Select V100 for the GPU, 30GB of RAM for the CPU,  and for the machine image select Deep Learning VM with CUDA 11.8, M116, Debian 11, Python 3.10.
- Enable “Allow HTTP traffic” and “Allow HTTPS traffic”. 
- Then reserve a static external IP and create a new Firewall rule.  In the firewall rule under Protocols and ports, select “Specified protocols and ports” and enter 5000 in the TCP section.
- Open the SHH terminal enter the following commands:
	wget https://repo.anaconda.com/archive/Anaconda3-2023.03-1-Linux-x86_64.sh
	bash Anaconda3-2023.03-1-Linux-x86_64.sh
	source ~/.bashrc
	jupyter notebook --generate-config
	vim ~/.jupyter/jupyter_notebook_config.py
- Add the following lines of code to the configuration file:
	c.NotebookApp.ip = '*'
	c.NotebookApp.open_browser = False
	c.NotebookApp.port = 5000
- Then open the jupyter notebook with:
	jupyter-notebook --no-browser --port=5000
- Go to your browser
- Now run the notebook.


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


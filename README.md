# DS4002-Project3

## Repository Contents
This repository contains the following contents:
- ***SCRIPTS***: this folder contains all scripts used to perform the EDA and pre-processing steps, build our CNN model to classify images, and generate visualizations.
- ***DATA***: this folder contains instructions to obtain the images used to train our CNN model and two datasets of corresponding labels for each image specifying the flower type. The original dataset of flower type labels is called 'flowerimagelabels.csv' and contains a numeric code for each type of flower, while 'label_to_name.csv' contains the actual names of the flowers in our image data. It also houses an appendix of our data and visualizations. 
- ***OUTPUT***: this folder contains outputs produced from our EDA and building our CNN model, such as tables and graphs. 

### Section 1: Software and platform section

***Software Used***:
For this project, we used python as the primary language for performing our EDA and building our CNN model. Coding was completed through Google Collab. 

***Packages***:

Python Packages used: tarfile, PIL, matplotlib, seaborn, pandas, numpy, tempfile, shutil

***Platform***: 
All members of this project used Mac as their platform. 

### Section 2: Documentation Map


### Section 3: Reproduction Steps 

##### **1. Download the Dataset**  
- Within the DATA folder on this repo, follow the instructions under the 'Dataset_Acquisition.md' file (steps are briefly described below).
- Download the images from the website linked in the file: https://www.robots.ox.ac.uk/~vgg/data/flowers/102/index.html
- Original image labels are also available on this website, but are provided within the DATA folder on this repo.

##### **2. Perform Exploratory Data Analysis (EDA)**  
   - Within the SCRIPTS folder, locate 'project_3_eda.ipynb' to perform the EDA. (Note: the following steps are carried out within this script)
   - Install necessary Python libraries: tarfile, PIL, matplotlib, seaborn, pandas, numpy, tempfile, shutil
   - Load in the images and image label dataset to collect image information.
   - Create the following visualizations: (1) Image Width & Height Distribution (log scale) (2) Image Area Distribution (3) Aspect Ratio (width/height) Distribution (4) Flower Class Label Distribution (5) Random Sample Images

##### **3. Preprocessing Steps**  
   - Within the SCRIPTS folder, locate (filename) to prepare the data to create our CNN model. (Note: the rest of the reproducibility steps for this project are performed within this script)
   - Resize all images to 224x224 pixels to standardize image inputs.
   - Create 4 datasets per image based on its orientation: the original image and three rotated versions at a 90° angle, a 120° angle, and a 270° angle.

##### **4. Train CNN Model**  
   - Continuing to work within the (filename) script, implement a lightweight CNN architecture with three convolutional layers (32, 64, and 128 filters) with 3x3 kernels followed by ReLU activation, batch normalization, and 2x2 max pooling.
   - Split the data into 70% for training, 15% for validation, and the remaining 15% for testing.
   - Train the model for 30 epochs using the Adam optimizer, focusing on comparing model performance across the four orientation datasets.

##### **5. Evaluate Model Performance**  
   - Evaluate the model perofmrance by obtaining its accuracy.
   - Achieve 80% accuracy of correct classifications regardless of image orientation in order to answer our research question.

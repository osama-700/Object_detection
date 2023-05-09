# Object Detection in an Urban Environment



## Submission Template

### Project overview
This section should contain a brief description of the project and what we are trying to achieve. Why is object detection such an important component of self driving car systems?
This project aim to establish object detection for a self driving car by training model then validate to be able to detect car and people
object detection is really important for self driving system because it rely on the ability to recognize and avoid obstacle in real time with help of LIDAR, radar and cameras to detect and identify objects




### Set up
This section should contain a brief description of the steps to follow to run the code for this repository.
Step 1 - Exploratory Data Analysis (EDA)
The ipynb file can found in Exploratory_Data_Analysis.ipynb
The 10 Desired output of the display_images function are in images file as
images/Step1-1
images/Step1-2
images/Step1-3
images/Step1-4
images/Step1-5
images/Step1-6
images/Step1-7
images/Step1-8
images/Step1-9
images/Step1-10
The Class Count, Distribution of object center in image, Distribution of object area in image and Distribution of object center in image can be found in image file as
images/Step1-11
images/Step1-12
images/Step1-13
images/Step1-14

Note the image distribution show that although object center is usually in the center of image, 
but it's bounding boxes sometimes cover corners of the image. Since the dist shows high values in center, 
it also suggests that most bounding boxes cover center of the image.
Also, surfing through the dataset suggests fewer samples in darker/foggy conditions compared to day/clear conditions. 
So, random brightness, contrast and color shift should help.


Step2 - Edit the config file
The config file can be found under (pipeline_new.config) and (pipeline.config)

Step 3 - Model Training and Evaluation
expriment graph (Loss chart) can be found under images/Step 3 Loss

Step 4- Step 4 - Improve the performances
The ipynb file can found in Explore augmentations.ipynb


### Dataset
Front Camera Images from Waymo Open Dataset. Data are in TFRecord Format, the TFRecord format is a simple format for storing a sequence of binary records, which helps in data reading and processing efficiency.

### Training
 a three conifgration has been tested all of them can be checked in Model1.config, Model2.config and Model3.config files 
 The first Model have 0.08 Learning rata and 300000 steps, The second model have 0.04 learning rate and 25000 steps while the last modle have 0.08 learning rate and 50000 steps
 The loss result can be seen in 3 Model loss show.png
 and it can clearly see the first modle have the least loss because of n increase while the second and third model have higher loss
 
 For the IOU image/IOU.png shows the IOU different between each model which can clearly see model one has the best IOU overall

so at the end we can clearly see if we increased number of steps, the learning will be better also if we use data augemntation like flipping, scaling, and random cropping that will help to improve the accuracy 

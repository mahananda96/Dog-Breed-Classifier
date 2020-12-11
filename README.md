# Udacity's Data Scientist Nanodegree Capstone Project: Dog Breed Classifier

### Table of Contents:
1) Project Overview
2) Problem Statement
3) Libraries
4) Data Description
5) File Description
6) Algorithm and Implementation
7) Model Evaluation
8) Justification
9) Results
10) Improvements and Refinement
9) Acknowledgements


### Project Overview:
This project is part of Udacity Data Scientist Nanodegree Program and is one of the most popular Udacity projects across machine learning and artificial intellegence nanodegree programs. The goal is to classify images of dogs according to their breed. Here we are preparing a model to identify dog faces, human faces and their breeds also. 

### Problem Statement :
Here we are focussing to use CNN to detect dog images.
	1) In this, the model should detect that the input image is of a dog or human or none of them. 
	2) If it is detected as dog, than detect the breed of dog.
	3) If it is detected as human, then detect the breed of dog which closely resemble to that image.
### Libraries:
The libraries used in this project are:
	Keras
	OpenCV
	Matplotlib
	Numpy

### Data Description:
There are following datasets available for this Model:
	Dog Images :- There is dataset of dog images where there 8351 images with 133 breeds.
			8351 dog images are divided into 3 datasets:
			Train Dataset with 6680 images.
			Validation Dataset with 835 images.
			Test Dataset with 836 images.
	Human Images :- There is a dataset with 13233 images in it.

### File Description:
	dog_app.ipynb: Jupyter notebook containing the algorithm and process used to create it.
	dog_app.html: A copy of dog_app.ipynb in html format.
	Haarcascades folder: Xml file for use with the OpenCv face detector class.
	Image Dataset : Images in jpg and jpeg format used to test the algorithm's predictions.
	
### Algorithm and Implementation
dog_breed_algorithm function contains the final algorithm which execute the whole functionality. 
	Step 1: Firstly we are using "dog_detector" model to detect is it a dog face or not. In this RestNet50 is used to do the detection.
		If it comes dog, then it will detect its breed.
	Step 2: If it is not detected as a dog face, then "face_detector" is detecting it as a human face or not.Here we have used CV2 implementation of Haar feature-based cascade classifiers to detect the human faces
		If it is detected as human, then detect the dog breed that closely resemble to it.
	Step 3: If it neither detected as human or dog, then show that message. 

### Model Evaluation
Here we have used CNN with VGG19 BottleNeck Feature to identify the the 133 dog breeds. 
	1) One GlobalAveragePooling2D layer is used to get the VGG output.
	2) One dense layer is used using relu activation and 200 nodes.
	3) As the size of dataset is small, we have used a Dropout Layer.
	4) Lastly one more Dense Layer with Softmax 
The aim was to attain atleast 66% acurracy. This model gave a 70.2% of accuracy on test data.

### Justifiaction
	Adding a layer of Relu Activation has substantially increased the metric(Accuracy) of the model. Since, the dataset is small, there was a chance 
	of overfitting which can decrease the performance for unknown data. Thus we have used a dropout rate of 30%. Lastly we preferred 20 epochs for training.

### Results
	The algo is detecting dog image correctly.
	The algo is detecting human image correctly.
	The algo gave a 70.2153% test accuracy
	Github link: https://github.com/mahananda96/Dog-Breed-Classifier
	Blog link: https://mahananda96.medium.com/udacity-data-scientist-nanodegree-capstone-project-dog-breed-classifier-project-3bff0c6cbd78

### Improvements and Refinements
	More classification among dog breed will be nice. This can be done by feeding it with more variation in train dataset. Particularly 
	classification of special and minute features as tere are breeds with almost 805 simmilarity in apearance.
	
### Acknowledgements:
	I sincerely acknowledgement udacity constant help and support in this project.


![image](https://user-images.githubusercontent.com/66901757/119221827-e3294100-bb0e-11eb-8595-749a1dd9c932.png) 
![image](https://user-images.githubusercontent.com/66901757/119222398-d528ef80-bb11-11eb-836a-30dd3ee3ec64.png)
## Welcome to the project- "Development of a Visual Recognition Model for Aztec Hieroglyphs."
This project is developed by Tarun Subhash Nagdeve for Google Summer of Code 2021 with Red Hen Labs
### Project Description
This project aims to develop a recognition system that'll identify Aztec glyphs. Aztec is pictographic and ideographic photo-writing. It has no alphabets but different symbolic signs that have different meanings. The dataset currently consists of 1261 color images and growing. The dataset contains three types of images: Simplex, Compound, and Atomic images. As the name, suggests Simplex and Atomic contain simple and atomic images, respectively, and Compound images are the combination of simple and atomic ones. So the main task here would be creating a neural network that'll take in an image, compare it with the ones in our system, and finally give out the five most similar images matching with the input image. Here, we'll be using pre-trained Neural Networks for training our model, like MobileNet, InceptionV3, VGG16, etc. And finally, the trained model will be deployed online so that it's accessible easily. 

### Timeline
#### Coding Period Before the First Evaluation
* [ Week 1 (7th June- 14th June 2021)](#Project-Description)
* [Week 2 (15th June- 22th June 2021)](##Week-2)
* [Week 3 (23th June- 30th June 2021)](##Week-3)
* [Week 4 (1st July- 8th July 2021)](##Week-4)





## Week 1
(7th June- 14th June 2021)
  
### Tasks to be accomplished:-
 1. Renaming the images in the dataset. <br />
 2. Preprocessing the images. <br />

### Estimated Time Required:- 1 week  <br />
#### Abstract
The dataset currently consists of 1261 color images and growing. We first need to rename the photos, as some of them have identical names that can create problems while giving the output. Also, we need some preprocessing on the images, like resizing each image to the same size, turning each image to a similar color scale, etc.
#### Status - All tasks Completed Successfully!

## Week 2 
(15th June- 22th June 2021)
   
### Tasks to be accomplished:-
  1. Selecting a model to train the dataset.
  2. Developing a prototype

### Estimated Time Required:- 2 week  <br />
#### Abstract
After comparing the results from various models, It can be concluded that the VGG16 model is giving the best results so far. The VGG16 model has 16 layers and about 138 million (approx) parameters. Here we'll  be using the last layer, i.e., the 'fc2' layer for predictions. 
#### Status - Task 1 Completed Successfully!

## Week 3 
(23th June- 30th June 2021)
Week 2 Continued..
### Tasks to be accomplished:-
  1. Selecting a model to train the dataset.
  2. Developing a prototype


#### Abstract
A working prototype can be seen here-https://github.com/TrunnMosby/GSoC-2021/blob/gh-pages/Aztec_Glyph_Detection.ipynb

#### Status - All tasks Completed Successfully!

## Week 4 
(1st July- 8th July 2021)
Note- The dataset has been updated, and more images have been added.

### Tasks to be accomplished:-
  1. Implimenting different techniques to increase the accuracy of the model.
  2. Using the updated dataset to train the model.
 
### Estimated Time Required:- 2 week  <br />
  





         


![image](https://user-images.githubusercontent.com/66901757/119221827-e3294100-bb0e-11eb-8595-749a1dd9c932.png) 
![image](https://user-images.githubusercontent.com/66901757/119222398-d528ef80-bb11-11eb-836a-30dd3ee3ec64.png)
## Welcome to the project- "Development of Visual Recognition Model for Aztec Hieroglyphs."
This project is developed by Tarun Subhash Nagdeve for Google Summer of Code 2021 with Red Hen Labs
### Project Description
This project aims to develop a recognition system that'll identify Aztec glyphs. Aztec is pictographic and ideographic photo-writing. It has no alphabets but different symbolic signs that have different meanings. The dataset currently consists of 1261 color images and growing. The dataset contains three types of images: Simplex, Compound, and Atomic images. As the name, suggests Simplex and Atomic contain simple and atomic images, respectively, and Compound images are the combination of simple and atomic ones. So the main task here would be creating a neural network that'll take in an image, compare it with the ones in our system, and finally give out the five most similar images matching with the input image. Here, we'll be using pre-trained Neural Networks for training our model, like MobileNet, InceptionV3, VGG16, etc. And finally, the trained model will be deployed online so that it's accessible easily. 

### Timeline
#### Coding Period Before the First Evaluation
* [ Week 1 (7th June- 14th June 2021)](#Week-1)
* [Week 2 (15th June- 22th June 2021)](#Week-2)
* [Week 3 (23th June- 30th June 2021)](#Week-3)
* [Week 4 (1st July- 8th July 2021)](#Week-4)

## Week 1
(7th June- 14th June 2021)
  
#### Abstract
The dataset currently consists of 1261 color images and growing. We first need to rename the photos, as some of them have identical names that can create problems while giving the output. Also, we need some preprocessing on the images, like resizing each image to the same size, turning each image to a similar color scale, etc.
### Tasks Accomplished:-
 * Renaming the images in the dataset. <br />
 * Preprocessing the images. <br />

## Week 2 
(15th June- 22th June 2021)
   
#### Abstract
The dataset has 1261 images, out of which only a few have more than one copy; this makes it very difficult for us to compare the results as we cannot split the data into train and test. But we visually compare the output given by each model and the time taken by them to train. Four pre-trained models have been considered here- The VGG16 model, MobileNet model, ResNet101, and Inception V3.
* ### VGG16 model 
VGG16 is a convolution neural net (CNN ) architecture which was used to win ILSVR(Imagenet) competition in 2014.Most unique thing about VGG16 is that instead of having a large number of hyper-parameter they focused on having convolution layers of 3x3 filter with a stride 1 and always used same padding and maxpool layer of 2x2 filter of stride 2. It follows this arrangement of convolution and max pool layers consistently throughout the whole architecture. In the end it has 2 FC(fully connected layers) followed by a softmax for output. The 16 in VGG16 refers to it has 16 layers that have weights. This network is a pretty large network and it has about 138 million (approx) parameters. Here, we'll be using the FC2 layer for training our model.
#### NOTE- The set 'result images' shows the 5 most similar images to the 'query image' in descending order. 
#### Output-1
![Screenshot (90)](https://user-images.githubusercontent.com/66901757/124781568-2295da80-df61-11eb-8096-a87258a91765.png)
#### Output-2
![Screenshot (93)](https://user-images.githubusercontent.com/66901757/124782083-8fa97000-df61-11eb-9f0e-d89102c85afd.png)
#### Output-3
![Screenshot (94)](https://user-images.githubusercontent.com/66901757/124782177-a51e9a00-df61-11eb-8aa8-db68ff9b88ba.png)
#### Output 4
![Screenshot (109)](https://user-images.githubusercontent.com/66901757/124785024-1eb78780-df64-11eb-98cc-40d3dfd905d3.png)


#### Time taken for training is 552.6561 seconds.
![Screenshot (96)](https://user-images.githubusercontent.com/66901757/124782556-f3cc3400-df61-11eb-8c2e-1bf108f25eb3.png)

* ### MobileNet model 
MobileNet is a class of CNN that was open-sourced by Google, and therefore, this gives us an excellent starting point for training our classifiers that are insanely small and insanely fast. MobileNet uses depthwise separable convolutions. It significantly reduces the number of parameters when compared to the network with regular convolutions with the same depth in the nets. This results in lightweight deep neural networks. Here, we'll be using the last layer for training our model.
#### NOTE- The set 'result images' shows the 5 most similar images to the 'query image' in descending order. 
#### Output-1
![Screenshot (101)](https://user-images.githubusercontent.com/66901757/124784045-2e829c00-df63-11eb-9ee1-79988e6bd526.png)
#### Output-2
![Screenshot (103)](https://user-images.githubusercontent.com/66901757/124784379-802b2680-df63-11eb-9353-67a242dd1a0f.png)

#### Output-3
![Screenshot (102)](https://user-images.githubusercontent.com/66901757/124784185-51ad4b80-df63-11eb-923f-496abff161ec.png)
### Output-4
![Screenshot (105)](https://user-images.githubusercontent.com/66901757/124784447-91743300-df63-11eb-8bd6-90c69520d29c.png)

#### Time taken for training is 57.8996 seconds.
![Screenshot (107)](https://user-images.githubusercontent.com/66901757/124784649-c08aa480-df63-11eb-8bfd-370b14de9979.png)


* ### ResNet101 model 
ResNet is one of the most powerful deep neural networks which has achieved fantabulous performance results in the ILSVRC 2015 classification challenge. ResNet has achieved excellent generalization performance on other recognition tasks and won the first place on ImageNet detection, ImageNet localization, COCO detection and COCO segmentation in ILSVRC and COCO 2015 competitions.There are many variants of ResNet architecture i.e. same concept but with a different number of layers. We have ResNet-18, ResNet-34, ResNet-50, ResNet-101, ResNet-110, ResNet-152, ResNet-164, ResNet-1202 etc. The name ResNet followed by a two or more digit number simply implies the ResNet architecture with a certain number of neural network layers. 
#### NOTE- The set 'result images' shows the 5 most similar images to the 'query image' in descending order. 
#### Output-1
![Screenshot (114)](https://user-images.githubusercontent.com/66901757/124786967-c7b2b200-df65-11eb-958d-b2c9a2416042.png)
#### Output-2
![Screenshot (116)](https://user-images.githubusercontent.com/66901757/124787087-df8a3600-df65-11eb-9c44-5d87fadeaba7.png)
#### Output-3
![Screenshot (115)](https://user-images.githubusercontent.com/66901757/124787159-ee70e880-df65-11eb-9a65-9766b31357ab.png)
### Output-4
![Screenshot (117)](https://user-images.githubusercontent.com/66901757/124787290-0183b880-df66-11eb-8abc-38cfdec93623.png)

#### Time taken for training is 233.5496 seconds.
![Screenshot (118)](https://user-images.githubusercontent.com/66901757/124787369-12342e80-df66-11eb-9990-cea45bba6be7.png)

* ### InceptionV3 model 
#### NOTE- The set 'result images' shows the 5 most similar images to the 'query image' in descending order. 
#### Output-1
![Screenshot (120)](https://user-images.githubusercontent.com/66901757/124788157-bfa74200-df66-11eb-8dfa-5bf85ffe2890.png)
#### Output-2
![Screenshot (122)](https://user-images.githubusercontent.com/66901757/124788419-efeee080-df66-11eb-9140-d43f6ecc4379.png)

#### Output-3
![Screenshot (121)](https://user-images.githubusercontent.com/66901757/124788471-fda46600-df66-11eb-8b35-3ccab61258e5.png)

### Output-4
![Screenshot (123)](https://user-images.githubusercontent.com/66901757/124788514-0a28be80-df67-11eb-8a1c-ba51ff3df9df.png)

#### Time taken for training is 178.2110 seconds.
![Screenshot (119)](https://user-images.githubusercontent.com/66901757/124788585-19a80780-df67-11eb-822a-15548d645604.png)

### Tasks Accomplished:-
  * Training the dataset on various models.
  * Comparing the performance of each model.  
  * Selecting the best model.

## Week 3 
(23th June- 30th June 2021)
#### Abstract
A working prototype can be seen here-https://github.com/TrunnMosby/GSoC-2021/blob/gh-pages/Aztec_Glyph_Detection.ipynb
### Tasks to be accomplished:-
  * Developing a prototype.
  * Testing of the prototype on various examples



## Week 4 
(1st July- 8th July 2021)
Note- The dataset has been updated, and more images have been added.

### Tasks to be accomplished:-
  1. Implimenting different techniques to increase the accuracy of the model.
  2. Using the updated dataset to train the model.

  





         

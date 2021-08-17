
![image](https://user-images.githubusercontent.com/66901757/119221827-e3294100-bb0e-11eb-8595-749a1dd9c932.png) 
![image](https://user-images.githubusercontent.com/66901757/119222398-d528ef80-bb11-11eb-836a-30dd3ee3ec64.png)
## Welcome to the project- "Development of Visual Recognition Model for Aztec Hieroglyphs."
This project is developed by Tarun Subhash Nagdeve for Google Summer of Code 2021 with Red Hen Labs
### Project Description
This project aims to develop a recognition system that'll identify Aztec glyphs. Aztec is pictographic and ideographic photo-writing. It has no alphabets but different symbolic signs that have different meanings. The dataset currently consists of 1255 color images and growing. The dataset contains three types of images: Simplex, Compound, and Atomic images. As the name, suggests Simplex and Atomic contain simple and atomic images, respectively, and Compound images are the combination of simple and atomic ones. So the main task here would be creating a neural network that'll take in an image, compare it with the ones in our system, and finally give out the five most similar images matching with the input image. Here, we'll be using pre-trained Neural Networks for training our model, like MobileNet, InceptionV3, VGG16, etc. And finally, the trained model will be deployed online so that it's accessible easily. 

### Timeline
#### Coding Period Before the First Evaluation
* [ Week 1 (7th June- 14th June 2021)](#Week-1)
* [Week 2 (15th June- 22th June 2021)](#Week-2)
* [Week 3 (23th June- 30th June 2021)](#Week-3)
* [Week 4 (1st July- 8th July 2021)](#Week-4)
* [Week 5 (9th July- 16th July 2021)](#Week-5)
#### Coding Period After the First Evaluation
* [Week 6 (17th July- 23rd July 2021)](#Week-6)
* [Week 7 (24th July- 31st July 2021)](#Week-7)
* [Week 8 (1st August-  8th August 2021)](#Week-8)
* [Week 9 (9th August- 16th August 2021)](#Week-9)
* [Week 10 (17th August- 23rd August 2021)](#Week-10) 



## Week-1
(7th June- 14th June 2021)
  
#### Abstract
The dataset currently consists of 1255 color images and growing. We first need to rename the photos, as some of them have identical names that can create problems while giving the output. Also, we need some preprocessing on the images, like resizing each image to the same size, turning each image to a similar color scale, etc.
### Tasks Accomplished:-
 * Renaming the images in the dataset. <br />
 * Preprocessing the images. <br />

## Week-2 
(15th June- 22th June 2021)
   
#### Abstract
The dataset has 1255 images, out of which only a few have more than one copy; this makes it very difficult for us to compare the results as we cannot split the data into train and test. But we can visually compare the output given by each model and the time taken by them to train. Four pre-trained models have been considered here- The VGG16 model, MobileNet model, ResNet101, and Inception V3.
* ### VGG16 model 
VGG16 is a convolution neural net (CNN ) architecture which was used to win ILSVR(Imagenet) competition in 2014.Most unique thing about VGG16 is that instead of having a large number of hyper-parameter they focused on having convolution layers of 3x3 filter with a stride 1 and always used same padding and maxpool layer of 2x2 filter of stride 2. It follows this arrangement of convolution and max pool layers consistently throughout the whole architecture. In the end it has 2 FC(fully connected layers) followed by a softmax for output. The 16 in VGG16 refers to it has 16 layers that have weights. This network is a pretty large network and it has about 138 million (approx) parameters. Here, we'll be using the FC2 layer for training our model.
#### Architecture of VGG-16 model
![VGG16](https://user-images.githubusercontent.com/66901757/124808538-b032f380-df7c-11eb-9b06-0d90043cc498.png)
#### NOTE- The set 'result images' shows the 5 most similar images to the 'query image' in descending order. 
#### Output-1 for VGG-16 model
![Screenshot (90)](https://user-images.githubusercontent.com/66901757/124781568-2295da80-df61-11eb-8096-a87258a91765.png)
#### Output-2 for VGG-16 model
![Screenshot (93)](https://user-images.githubusercontent.com/66901757/124782083-8fa97000-df61-11eb-9f0e-d89102c85afd.png)
#### Output-3 for VGG-16 model
![Screenshot (94)](https://user-images.githubusercontent.com/66901757/124782177-a51e9a00-df61-11eb-8aa8-db68ff9b88ba.png)
#### Output 4 for VGG-16 model
![Screenshot (109)](https://user-images.githubusercontent.com/66901757/124785024-1eb78780-df64-11eb-98cc-40d3dfd905d3.png)


#### Time taken for training by VGG-16 is 1,080.1289 seconds.
![Screenshot (125)](https://user-images.githubusercontent.com/66901757/124888953-36d6e780-dff4-11eb-8143-a22a91f0cffa.png)


* ### MobileNet model 
MobileNet is a class of CNN that was open-sourced by Google, and therefore, this gives us an excellent starting point for training our classifiers that are insanely small and insanely fast. MobileNet uses depthwise separable convolutions. It significantly reduces the number of parameters when compared to the network with regular convolutions with the same depth in the nets. This results in lightweight deep neural networks. Here, we'll be using the last layer for training our model.
#### Architecture of MobileNet model
![Mobile](https://user-images.githubusercontent.com/66901757/124808935-2e8f9580-df7d-11eb-88c8-53c8e8666a1d.png)
#### NOTE- The set 'result images' shows the 5 most similar images to the 'query image' in descending order. 
#### Output-1 for MobileNet model
![Screenshot (101)](https://user-images.githubusercontent.com/66901757/124784045-2e829c00-df63-11eb-9ee1-79988e6bd526.png)
#### Output-2 for MobileNet model
![Screenshot (103)](https://user-images.githubusercontent.com/66901757/124784379-802b2680-df63-11eb-9353-67a242dd1a0f.png)

#### Output-3 for MobileNet model
![Screenshot (102)](https://user-images.githubusercontent.com/66901757/124784185-51ad4b80-df63-11eb-923f-496abff161ec.png)
### Output-4 for MobileNet model
![Screenshot (105)](https://user-images.githubusercontent.com/66901757/124784447-91743300-df63-11eb-8bd6-90c69520d29c.png)

#### Time taken for training by MobileNet model is 115.8361 seconds.
![Screenshot (127)](https://user-images.githubusercontent.com/66901757/124892436-81a62e80-dff7-11eb-9692-1a6ddb40573b.png)



* ### ResNet101 model 
ResNet is one of the most powerful deep neural networks which has achieved fantabulous performance results in the ILSVRC 2015 classification challenge. ResNet has achieved excellent generalization performance on other recognition tasks and won the first place on ImageNet detection, ImageNet localization, COCO detection and COCO segmentation in ILSVRC and COCO 2015 competitions.There are many variants of ResNet architecture i.e. same concept but with a different number of layers. We have ResNet-18, ResNet-34, ResNet-50, ResNet-101, ResNet-110, ResNet-152, ResNet-164, ResNet-1202 etc. The name ResNet followed by a two or more digit number simply implies the ResNet architecture with a certain number of neural network layers. 
#### Architecture of ResNet101 model
![Resnet101](https://user-images.githubusercontent.com/66901757/124809352-a8c01a00-df7d-11eb-9acf-18aa020f41ab.png)

#### NOTE- The set 'result images' shows the 5 most similar images to the 'query image' in descending order. 
#### Output-1 for ResNet101 model
![Screenshot (114)](https://user-images.githubusercontent.com/66901757/124786967-c7b2b200-df65-11eb-958d-b2c9a2416042.png)
#### Output-2 for ResNet101 model
![Screenshot (116)](https://user-images.githubusercontent.com/66901757/124787087-df8a3600-df65-11eb-9c44-5d87fadeaba7.png)
#### Output-3 for ResNet101 model
![Screenshot (115)](https://user-images.githubusercontent.com/66901757/124787159-ee70e880-df65-11eb-9a65-9766b31357ab.png)
### Output-4 for ResNet101 model
![Screenshot (117)](https://user-images.githubusercontent.com/66901757/124787290-0183b880-df66-11eb-8abc-38cfdec93623.png)

#### Time taken for training by ResNet101 model is 488.8327 seconds.
![Screenshot (130)](https://user-images.githubusercontent.com/66901757/124897638-1e6acb00-dffc-11eb-9b34-2d43269eaaa0.png)



* ### InceptionV3 model 
Inception-v3 is a convolutional neural network architecture from the Inception family that makes several improvements including using Label Smoothing, Factorized 7 x 7 convolutions, and the use of an auxiliary classifer to propagate label information lower down the network (along with the use of batch normalization for layers in the sidehead).




#### Architecture of InceptionV3 model
![Inception](https://user-images.githubusercontent.com/66901757/124809517-d311d780-df7d-11eb-8f75-b992e3b33cae.png)
#### NOTE- The set 'result images' shows the 5 most similar images to the 'query image' in descending order. 
#### Output-1 for InceptionV3 model
![Screenshot (120)](https://user-images.githubusercontent.com/66901757/124788157-bfa74200-df66-11eb-8dfa-5bf85ffe2890.png)
#### Output-2 for InceptionV3 model
![Screenshot (122)](https://user-images.githubusercontent.com/66901757/124788419-efeee080-df66-11eb-9140-d43f6ecc4379.png)

#### Output-3 for InceptionV3 model
![Screenshot (121)](https://user-images.githubusercontent.com/66901757/124788471-fda46600-df66-11eb-8b35-3ccab61258e5.png)

### Output-4 for InceptionV3 model
![Screenshot (123)](https://user-images.githubusercontent.com/66901757/124788514-0a28be80-df67-11eb-8a1c-ba51ff3df9df.png)

#### Time taken for training by InceptionV3 model is 419.4781 seconds.
![Screenshot (132)](https://user-images.githubusercontent.com/66901757/124899592-e9f80e80-dffd-11eb-9a23-8b3cc7f00526.png)


### Tasks Accomplished:-
  * Training the dataset on various models.
  * Comparing the performance of each model.  
  * Selecting the best model.


### Conclusion
It can be noted from the examples above that the MobileNet model seems to be the most efficient model concerning both accuracy and time.
Hence we'll be using this model to train our data.


## Week-3 
(23th June- 30th June 2021)
#### Abstract
After testing various models, we've concluded that the MobileNet model seems to be the most efficient model. Next, we'll be creating a prototype using the MobileNet model and test it on various examples.
#### Test Output-1
![Screenshot (136)](https://user-images.githubusercontent.com/66901757/124948029-f7c58800-e02d-11eb-89f4-a8c79899fb2d.png)
#### Test Output-2
![Screenshot (137)](https://user-images.githubusercontent.com/66901757/124948107-090e9480-e02e-11eb-98a7-55e603dd993e.png)
#### Test Output-3
![Screenshot (138)](https://user-images.githubusercontent.com/66901757/124948183-17f54700-e02e-11eb-93dd-a3bb4b1cc352.png)
#### Test Output-4
![Screenshot (144)](https://user-images.githubusercontent.com/66901757/124949433-30b22c80-e02f-11eb-8ca4-5809eb24c3c4.png)
#### Test Output-5
![Screenshot (145)](https://user-images.githubusercontent.com/66901757/124949499-3e67b200-e02f-11eb-9f5d-9b7acdc96868.png)
#### Test Output-6
![Screenshot (146)](https://user-images.githubusercontent.com/66901757/124949557-4cb5ce00-e02f-11eb-8d2c-16edfb39bcb4.png)
#### Test Output-7
![Screenshot (147)](https://user-images.githubusercontent.com/66901757/124949615-5808f980-e02f-11eb-85cd-4762ae0e4a18.png)
#### Test Output-8
![Screenshot (148)](https://user-images.githubusercontent.com/66901757/124949659-635c2500-e02f-11eb-8838-751d2c9e0592.png)

You can visit the prototype here- https://github.com/TrunnMosby/GSoC-RedHenLabs-Aztec-Glyph-Detection/blob/main/MobileNet.ipynb

### Tasks Accomplished:-
  * Developing a prototype.
  * Testing of the prototype on various examples



## Week-4 
(1st July- 8th July 2021) <br />
Note- The dataset has been updated, and more images have been added.
#### Abstract
The updated dataset contains 1291 images. Now the new dataset has to be trained again. We'll again be using the MobileNet model to do so, and check the impact of increasing the size of the dataset on training time and accuracy. 
#### Time taken for training the updated dataset by MobileNet model is 117.6357 seconds.
![Screenshot (154)](https://user-images.githubusercontent.com/66901757/125607858-0e53913f-9d8f-4010-879c-e37ce31539fc.png)
#### Test Output-1
![Screenshot (101)](https://user-images.githubusercontent.com/66901757/124784045-2e829c00-df63-11eb-9ee1-79988e6bd526.png)
#### Test Output-2
![Screenshot (103)](https://user-images.githubusercontent.com/66901757/124784379-802b2680-df63-11eb-9353-67a242dd1a0f.png)
#### Test Output-3
![Screenshot (155)](https://user-images.githubusercontent.com/66901757/125608107-28d15876-2489-4c77-9c0e-7ba40788b8e6.png)
#### Test Output-4
![Screenshot (157)](https://user-images.githubusercontent.com/66901757/125608298-3c5efe81-ba67-41d6-b64e-d2b60ad05c50.png)

### Conclusion
It can be noted that the training time has increased by 1.7996 seconds and with almost no change in accuracy.   

### Tasks Accomplished:-
  1. Using the updated dataset to train the model.
  2. Checking the impact of increasing the size of the dataset on training time and accuracy. 

## Week-5 
(9th July- 16th July 2021) <br />
#### Abstract
The existing dataset still doesn't contain more than one image per label, so to overcome this problem, we'll be using the technique of data augmentation to generate similar images. Data augmentation is a strategy that enables practitioners to significantly increase the diversity of data available for training models without actually collecting new data. Data augmentation techniques such as cropping, padding, and horizontal flipping are commonly used to train large neural networks.
#### Example of Data Augmentation
![da](https://user-images.githubusercontent.com/66901757/126774282-1a18bef9-23da-44f6-87b6-f889214cd8e3.png)<br />
Using Data Augmentation, we've created five copies of each image using different orientations. Now the size of the dataset has increased to 6473 images. Again we'll be using the MobileNet model to train the model on the new dataset and check its accuracy. The data augmentation is done using ImageDataGenerator and all the parameters are mentioned below-
ImageDataGenerator(rotation_range=40,width_shift_range=0.2,height_shift_range=0.2,
                           shear_range=0.2,zoom_range=0.2,horizontal_flip=True)
#### Test Output-1
![Screenshot (168)](https://user-images.githubusercontent.com/66901757/126773631-f7c4ee7d-4b15-4fa9-8156-1521fc3c96b8.png)
#### Test Output-2
![Screenshot (169)](https://user-images.githubusercontent.com/66901757/126773667-0eee9568-8a34-41b9-b2f4-74fa976f3451.png)

#### Test Output-3
![Screenshot (170)](https://user-images.githubusercontent.com/66901757/126773702-ea06c53b-d9a0-4979-ae3d-9eddf75c187d.png)

#### Test Output-4
![Screenshot (171)](https://user-images.githubusercontent.com/66901757/126773730-cc305229-7645-411f-97a5-140a0be798c4.png)

#### Test Output-5
![Screenshot (172)](https://user-images.githubusercontent.com/66901757/126773766-1b337b5f-7223-45f6-8555-cc5f1e0c1020.png)

#### Test Output-6
![Screenshot (173)](https://user-images.githubusercontent.com/66901757/126773796-43a8f86e-91b9-4a44-8c19-a37372e9598a.png)

#### Time taken for training the Augmented dataset by MobileNet model is 717.2585 seconds or 11.9543 minutes.
![Screenshot (174)](https://user-images.githubusercontent.com/66901757/126774750-e062cdc6-9c9a-4a45-9061-a0d9d363b350.png)

### Tasks Accomplished:-
  1. Generating more images using Data Augmentation techniques. 
  2. Training the MobileNet model on the Augmented dataset and checking it's accuracy.


## Week-6
(17th July- 23rd July 2021) <br />
#### Abstract
We'll now train the augmented images dataset using VGG16 model.
#### Test Output-1
![Screenshot (182)](https://user-images.githubusercontent.com/66901757/129734303-844cba18-d7f0-4264-b84b-fc5a1b0f8518.png)
#### Test Output-2
![Screenshot (183)](https://user-images.githubusercontent.com/66901757/129734393-e40425e2-3fbc-4a3d-94e7-7c0779335d0b.png)
#### Test Output-3
![Screenshot (184)](https://user-images.githubusercontent.com/66901757/129734438-eda25df6-8309-48de-ae63-1e3263737da1.png)
#### Test Output-4
![Screenshot (185)](https://user-images.githubusercontent.com/66901757/129734476-1c16691f-0e5a-4764-846e-961d1714f95f.png)
#### Test Output-5
![Screenshot (186)](https://user-images.githubusercontent.com/66901757/129734552-2b8e6829-dc37-4dbb-a03b-39fa4d2a1f35.png)
#### Time taken for training the Augmented dataset by VGG16 model is 6697.024 seconds or 111.61 minutes.
![Screenshot (187)](https://user-images.githubusercontent.com/66901757/129734619-d5103eec-70e7-4b6d-b50a-634739785fdb.png)


## Week-7
(24th July- 31st July 2021) <br />
#### Abstract
We'll now train the augmented images dataset using InceptionV3 model.
#### Test Output-1
![Screenshot (189)](https://user-images.githubusercontent.com/66901757/129736726-89386e2b-e2f1-49ea-bacb-6c780800d6be.png)

#### Test Output-2
![Screenshot (190)](https://user-images.githubusercontent.com/66901757/129736817-b5c5a07d-e6bc-4754-b1f0-c475eedb38b7.png)

#### Test Output-3
![Screenshot (191)](https://user-images.githubusercontent.com/66901757/129736901-349739e0-8e1c-4c9b-a3bf-344c44d0237f.png)

#### Test Output-4
![Screenshot (192)](https://user-images.githubusercontent.com/66901757/129737135-dffae598-2961-4f03-b5fc-e5024384bc9f.png)

#### Test Output-5
![Screenshot (193)](https://user-images.githubusercontent.com/66901757/129737262-051886dc-c4c5-4392-aaef-742621509c34.png)

#### Time taken for training the Augmented dataset by InceptionV3 model is 2348.7055 seconds or 39.145 minutes.
![Screenshot (188)](https://user-images.githubusercontent.com/66901757/129737332-441793ea-d613-4b95-b5bb-6ff2b8cfd919.png)

## Week-8
(1st August-  8th August 2021) <br />
#### Abstract
We'll now train the augmented images dataset using ResNet101 model.
#### Test Output-1
![Screenshot (201)](https://user-images.githubusercontent.com/66901757/129738793-3527c94b-5126-42f3-98e3-7ea14903bad1.png)
#### Test Output-2
![Screenshot (202)](https://user-images.githubusercontent.com/66901757/129738885-74451401-90d2-4d9f-a43e-10ba3c6318a7.png)
#### Test Output-3
![Screenshot (203)](https://user-images.githubusercontent.com/66901757/129739014-24234b38-6927-42ee-83f8-6cd274cb8045.png)
#### Test Output-4
![Screenshot (204)](https://user-images.githubusercontent.com/66901757/129739079-ddff0f5f-e09c-44a8-a21f-9a4166c600ec.png)
#### Test Output-5
![Screenshot (205)](https://user-images.githubusercontent.com/66901757/129739136-27e62f73-45cd-45a2-9d3b-b667959a1586.png)
#### Time taken for training the Augmented dataset by ResNet101 model is 3825.0867 seconds or 63.751445 minutes.
![Screenshot (200)](https://user-images.githubusercontent.com/66901757/129739206-c024f387-ce8b-45bb-9b63-138861a2b96b.png)

## Week-9
(9th August-  16th August 2021) <br />
#### Abstract
After testing all the models we come to the conclusion that apart from InceptionV3 all other models are performing well. Though the time taken by each model is very high when compared to MobileNet model. We can still compare the performance of all the models by computing the error from the original values, here we'll take the augmented images as the closest image and calculate the distance from them, then we'll train the models on dataset without augmented images and calculate the deviation between them.
Ranking of the models based on both performance and time taken:-
1. MobileNet
2. ResNet101
3. VGG16
4. InceptionV3





         

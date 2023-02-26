# Denoising-Autoencoder
# 1. Data and Preprocessing: 
We have used a subset of the landscape dataset that contains 4319 RGB images
provided by kaggle from this link :
https://www.kaggle.com/datasets/arnaud58/landscape-pictures/code
It contains images with 7 different backgrounds.
To work with the data we created a subset of the data with size 100 instances , split it 80 images for
training and 20 images for testing.
Then we fed those images into a list , resized those images to (400,400) , then normalized those sets ;
As images in the data had larger sizes that were over(1024,1024) which required a
very high computational power.
for testing after the training process we have created another test set which contained 3 different images from the ones in the training set , and also preprocessed them. 
#---------------------------------------------------------------------------------------------------------------------------------
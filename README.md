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
# 2. Methodology : 
At the beginning I have created gaussian noise with mean = 0 , and standard deviation = 1 over images , and here is an example of how they looked :

    ![image](https://user-images.githubusercontent.com/60916510/221427402-f4f4e7ab-bc84-4388-9887-5af3be1de4d0.png)

I have tried two different approaches : 
1. In the Fisrst approach I trained the autoencoder on the normalized training set , then I have tested it on noised images (external test set ) , I have tested this  approach on two different convolutional autoencoders; the first one went from 16 to 8 and the second one went from 80 to 32 . 
2. In the Second approach I have separated the autoencoders into two parts (encoder and decoder) , added the noise to the encodeed images then passed it to the decoder , tested this approach on two different convolutional autoencoders one went from 16 to 8 and the other one went from 80 to 32. 

# Introduction
Tracking a thing is revolutionary field as high-speed computers and high-resolution cameras has been developed the interest in computer vision algorithms for applications such as security, sports, and military. Within these applications, one of the most frequently performed task is determining the number, position, and movement of various objects. The techniques that performed over such sports can help us to give better replay and positive response towards the gameplay. The motion analysis and tracking information provided by the computer vision techniques can be used for the tactical analysis in different sports. 

Since the “ball” is the maximum crucial item in tennis, detecting and monitoring the ball turns into vital in tennis video analysis. Unfortunately, so a long way, no set of rules is capable of attain excellent consequences in finding the ball in broadcast tennis video BTV) because of the subsequent demanding situations:
- The corridor has severe deformation because of the reflection.
- The corridor may be very small, specifically on a long way facet of the camera. For a few frames, balls are so small that human eyes are not able to see.
-	The ball is frequently occluded through the gamers and the net. It can also additionally blend with the target market and complex background. The look of the ball vac- irregularly over frames. Its size, shape, and speed alternate irregularly over frames.

The above-indexed demanding situations make it tough to construct a ball illustration to identification the corridor in a frame.
In different words, just like the corridor detection and monitoring trouble in broadcast football video (BSV), this trouble is item-indistinguishable


# Dataset
Dataset that I’ve used is taken from the third-party website <a href='https://drive.google.com/file/d/1Dq2ag6a7ESHJm3ZHSJrYcu9_hWNyNkx1/view' >Dataset</a>. 
This dataset is provided the images of a game that has recorded. The sample of this dataset has given as follows.

![alt text](https://github.com/Utsav4852/Tennis-Ball-Tracking/blob/main/images/tennis_dataset.png)

Like this there are total 95 games of data are given and each game containes approximately 200+ images. So in total there are 20k images are taken for the training purpose. Along with the images each file also contains one label.csv file which has the the exact ball cordinates and the ball is visible or not in the frame. File name contains the name of the image, Visibility of the ball as some times ball get blurry because of the high speed that’s why it has 2 types of visibility 1 means it is clearly visible and 2 means it is partially visible, x-coordinate and y-coordinate contains the coordinate of the ball in the frame and status contains 2 different values like 0 means the frame contains the ball and 1 means the ball is not in the frame.



# Methodology
Methodology follows total 4 stages of process. Ball detection, Court Detection, Player Detection and Live tracking prediction.
-	Ball Detection: In this project we have given the images and coordinates. So, as a preprocessing task first I transformed the original image to ground truth that shows only ball in the entire frame as shown below.

![alt text](https://github.com/Utsav4852/Tennis-Ball-Tracking/blob/main/images/preprocessing.png)

- Court and player Detection: In our case we have steady camera setup for the entire video. So, the line of the court will be steady. It can be detected with certain pixel as shown below. 

![alt text](https://github.com/Utsav4852/Tennis-Ball-Tracking/blob/main/images/court_and_player.png)

- Ball Tracking: Once we get the ball position, we must pass that position to tracknet model to train the model. It will understand the ball tracking and we will get predicted output in the video.

# Output
![output_Final_2_AdobeCreativeCloudExpress](https://user-images.githubusercontent.com/40597501/163780923-4fddf01c-cae6-47d2-b84b-320c610fd528.gif)

Code is available <a href='https://github.com/Utsav4852/Tennis-Ball-Tracking/blob/main/Tennisball_tracking_final.ipynb'>Here</a>.

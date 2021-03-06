# Raspberry-Pi-Facial-Recognition
This is a lifesize humanoid based on the Inmoov 3D printed design. The link to the STL files will be linked below. The orginal design utiizes a custom pcb to interact with an arduino mega so that there are enough pins available for all the motors. I decided to go with an arduino mega and a shield that can supply the nesscary voltage and power to all the large servo motors. However for the head there is no sort of camera design for the eyes. I decided adjust 2 pieces in the eyes so that there is mobility in the eyes (can look up and down) then embedded a small raspberry pi camera with a ribbon wire in which the raspberry pi 3b can be mounted on the back of the humanoid. The facial recognition runs on tensorflow lite and requires the full 4 cores on the raspberry pi to be enabled otherwise you will get an error. Then you will need to run the face_dataset python file and point the camera at yourself in order to take 100 pictures that are converted to grayscale so that it can be inputted into the model. Since there would be many people who would like to use this feature I incorpatered scalability where you can add your name to the id list of photos that were taken when you ran the face_dataset file.

<img width="230" alt="Humanoid" src="https://user-images.githubusercontent.com/81518926/134824864-ed5c97a5-01f9-4b19-9bd2-da1c47918686.png">

# Materials
* Raspberry Pi 3B
* 3D printer
* Arduino Mega
* 4 large RC continous servos
* 20 micro servos
* Power supply

# Software Setup
First we begin by setting up the lastest version of raspbian buster which can be downloaded by visitng https://www.raspberrypi.org/ and downloading the zip file then unzipping it with either Winrar or 7zip then grab the disk image file and upload it to an SD card thats at least 16GB. Then configure wifi and enable ssh, VNC viewer, Camera and I2C. After that run a git clone on my repository to get the facial recognotion training and dataset files. Then we will need to download opencv and once that is configured run the train file and there should be no library issues. Then run the dataset prepaeration file where it takes 100 pictures of your face. The facial algorithms that this uses are 

# Project Insight and future developments
Inside of the body there are over 15 servos, 5 for each hand 2 large rc servos for the shoulders, 2 for the forearms, 4 for the eyes. Currently the A.I model has been uploaded to a google pai where the image processing is done on a server which is much faster than the raspberry pi running opencv. Then In terms of advanced features there is a simulation software where the motors can be mapped and you can use gesture control with the robot. I intend to add voice control to the robot where a small circular microphone will be placed inside of the ears which will be connected to the pi and with the same google api we can interact recieve and make voice commands.


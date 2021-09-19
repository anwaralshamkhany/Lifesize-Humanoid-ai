# Raspberry-Pi-Facial-Recognition
This is a lifesize humanoid based on the Inmoov 3D printed design. The link to the STL files will be linked below. The orginal design utiizes a custom pcb to interact with an arduino mega so that there are enough pins available for all the motors. I decided to go with an arduino mega and a shield that can supply the nesscary voltage and power to all the large servo motors. However for the head there is no sort of camera design for the eyes. I decided adjust 2 pieces in the eyes so that there is mobility in the eyes (can look up and down) then embedded a small raspberry pi camera with a ribbon wire in which the raspberry pi 3b can be mounted on the back of the humanoid. The facial recognition runs on tensorflow lite and requires the full 4 cores on the raspberry pi to be enabled otherwise you will get an error. Then you will need to run the face_dataset python file and point the camera at yourself in order to take 100 pictures that are converted to grayscale so that it can be inputted into the model. Since there would be many people who would like to use this feature I incorpatered scalability where you can add your name to the id list of photos that were taken when you ran the face_dataset file.

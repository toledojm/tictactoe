# Tic Tac Toe Game

Hi community! I want to share a Tic Tac Toe game that I play against my CPU. I use Python language for cross marks (x) detection on a handwriting board using a cell phone like webcam with IP Webcam app and CNC Gcode for serial communication with the router motion card.

Detail:
- I used Ultralitycs library for object detection training Yolov8 (nano modelo) with Roboflow cross marks dataset (about 1000 images + labels with augmentation included). 
- For cross detection in a particular zone I used a board image to split each polygon (9) with Roboflow PlygonZone. 
- For detection I used the Yolov8 trained model and Roboflow supervision library.
- For CNC communication I used my USB serial port with pyserial library.
- For CNC circles I used Autodesk Fusion360. I Design the board points and in the manufacture workspace I post-process the Gcode for GRBL type.

Steps:
1. Starting the game, all board positions are null.
2. CPU takes the first random move, using a circle mark.
3. I used the cross mark after.
4. CPU detects the cross mark and evaluates the board game, if no one wins the game continue.


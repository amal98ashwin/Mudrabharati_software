# MUDRABHARATI
Mudrabharati is a novel and unified fingerspelling system for Indic scripts in general. It can be used by the hearing impaired in India for their educational activities in Indian language media. In the fingerspelling system used in American Sign Language (ASL), a signing system used the world over, gestures are used to emulate the shapes of the English alphabet. A fingerspelling system based on the shape of the characters is not suitable for Indic scripts. For this reason, Mudrabharati is designed based on the underlying phonetics of the Indic scripts. Therefore, Mudrabharati emerges as a universal fingerspelling system for Indian languages.
<br/>

![image](https://github.com/user-attachments/assets/6a0de3d1-367e-4410-ac06-be2e95b7751b) <br/>

# WINDOWS DESKTOP APPLICATION

## Steps for installation

1) Download the zip file using the drive link and extract the files to a folder.
2) Please ensure that the dependent files are in the same directory as the .exe file.
3) Open the mudrabharati_desktop.exe file to run the application and explore MUDRABHARATI!

## Application
### **Selecting camera**<br/>
The application will take few seconds to open. Once open, the application window will look as below,<br/>

![image](https://github.com/user-attachments/assets/4ee7dc44-cd5d-46ea-a077-8d41b0fb1eb4) <br/><br/>
In the above window, select the camera index. By default, in-built webcam of the device will have index **0**. Additional cameras will have subsequent indices.


### **Opening application**<br/>
After pressing **Start**, the application will open as below, <br/>

![image](https://github.com/user-attachments/assets/488a229f-b1e6-4bb9-acbf-6285cfbfa696)


## Features
### **Temporal sensitivity**<br/>
In the top left, the sliding bar under "Normal time" controls for the temporal sensitivity of the detection. The value is in seconds. Experienced signers can increase the sensitivity by **lowering** the value.

### **Calibration buttons**<br/>
Place your right hand at position 1 and press **Calibrate Position 1** button. Wait for 5 seconds (count-down visible) to calibrate position 1 with respect to the face. Do the same for position 9 if needed.

### **Flip buttons**<br/>
To adjust the flip of the camera feed, these buttons are provided. Ensure that the video is mirror image of the user.

### **Language selection buttons**<br/>
The desired language for visual feedback of the script can be chosen by clicking on the buttons. **ta** stands for Tamil, **te** stands for Telugu and **hi** stands for Hindi (Devanagiri).

### **Talk**<br/>
**Talk** button is used to convert the entered text into sound. It is compatible with all languages.

# AI ALGORITHM FOR DETECTION
![image](https://github.com/user-attachments/assets/f6469b2f-b452-4937-9be6-b861fa8b1eb0)


**Input:** The input from the webcam is obtained. <br/> <br/>
**Keypoints detection:** The facial and hand keypoints are located using Google's mediapipe model. <br/> <br/>
**Position estimation:** With respect to the nose keypoint, the screen is divided into left and right field. <br/> <br/>
**Gesture prediction:** The hand keypoints corresponding to the right hand are fed as input to the consonant_gesture_recognizer model and that of the left hand are fed to either vowel_gesture_recognizer or the punctuation_recognizer models based on the estimated location. <br/> <br/>
**Character prediction:** By combining the estimated location and gesture of both the hands, the character is retrieved from the dictionary. <br/> <br/>


### **Eye Blink Detector**  

The **Eye Blink Detector** is a real-time application that uses **OpenCV** to detect eye blinks using a webcam. This project is useful for applications like **driver drowsiness detection** or monitoring alertness levels. It employs **Haar Cascade Classifiers** to detect faces and eyes, and it tracks consecutive frames where eyes are closed to determine if a person is blinking.  

#### **Technologies Used**  
- **Python**  
- **OpenCV** (Computer Vision)  
- **NumPy** (Numerical Computations)  

#### **Project Workflow**  

1. **Initialize Face & Eye Detection**  
   - Load Haar Cascade classifiers for **face detection** and **eye detection** (`haarcascade_frontalface_default.xml` & `haarcascade_eye_tree_eyeglasses.xml`).  

2. **Capture Real-Time Video Feed**  
   - Open the webcam using `cv2.VideoCapture(0)`.  

3. **Detect Eyes & Track Blinks**  
   - For each frame:  
     - Detect faces in the frame.  
     - Detect eyes within the detected face region.  
     - If no eyes are detected for **consecutive frames**, a blink is registered.  

4. **Trigger Alert on Blink Detection**  
   - If eyes remain closed beyond a defined **blink threshold**, an alert is displayed on the screen for **a set duration**.  

5. **Continuous Monitoring**  
   - The system continuously analyzes frames and updates blink detection in real-time.  
   - The loop runs until the user exits (`q` key press).  

#### **How to Run the Project**  
1. Install dependencies:  
   ```bash
   pip install opencv-python numpy
   ```  
2. Run the script:  
   ```bash
   python eye_blink_detector.py
   ```  
3. Make sure your webcam is working as the program captures live video.  


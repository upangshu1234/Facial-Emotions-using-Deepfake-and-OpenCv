# Facial Emotion Recognition using OpenCV and DeepFace

This project implements real-time facial emotion detection using the **DeepFace** library and **OpenCV**. It captures video from the webcam, detects faces, and predicts the emotions associated with each face. The emotion labels are displayed on the frames in real time. This is one of the simplest implementations of real-time emotion monitoring.

## ⭐ Give this repository a star if you find it useful!
This project took time and effort to understand and implement. Your support is appreciated! 😊

---

## 🛠 Dependencies

This project requires the following libraries:

- **DeepFace**: A deep learning facial analysis library that provides pre-trained models for facial emotion detection. It relies on TensorFlow for the underlying deep learning operations.
- **OpenCV**: An open-source computer vision library used for image and video processing.

## 📌 Installation & Setup

Follow these steps to get started:

### 1️⃣ Clone this repository
```sh
 git clone https://github.com/upangshu-basak/Facial-Emotion-Recognition-using-OpenCV-and-DeepFace.git
 cd Facial-Emotion-Recognition-using-OpenCV-and-DeepFace
```

### 2️⃣ Install dependencies

Using `requirements.txt`:
```sh
pip install -r requirements.txt
```

Or install them individually:
```sh
pip install deepface
pip install tf_keras
pip install opencv-python
```

### 3️⃣ Download Haar cascade XML file

The project requires a pre-trained Haar cascade classifier for face detection. Download the **haarcascade_frontalface_default.xml** file from the OpenCV GitHub repository and place it in the project directory.

### 4️⃣ Run the script
Execute the Python script to start real-time facial emotion detection:
```sh
python emotion.py
```
The webcam will open, and real-time facial emotion detection will start. Detected faces will be labeled with their corresponding emotions.

---

## ⚙️ Approach

1. **Import libraries**: OpenCV (`cv2`) for video capture and image processing, and DeepFace for emotion detection.
2. **Load the Haar cascade classifier**: The XML file is used to detect faces in the video feed.
3. **Start capturing video**: The webcam feed is captured using `cv2.VideoCapture()`.
4. **Process frames continuously**:
   - Convert frames to grayscale using `cv2.cvtColor()`.
   - Detect faces using `face_cascade.detectMultiScale()`.
   - Extract the face **Region of Interest (ROI)**.
   - Preprocess the face image using DeepFace’s built-in functions.
   - Predict emotions using a pre-trained model.
   - Retrieve the predicted emotion label and display it.
5. **Display results**:
   - Draw rectangles around detected faces.
   - Label them with predicted emotions using `cv2.putText()`.
   - Show the processed frames in real time using `cv2.imshow()`.
6. **Exit condition**: Press **'q'** to stop the script.
7. **Release resources**: The video capture is released, and all windows are closed using `cv2.destroyAllWindows()`.

---

## 📷 Output Preview
The program labels detected faces with emotions such as **Happy, Sad, Angry, Neutral**, etc., directly on the video feed.

---

## 👨‍💻 Author

Made with ❤️ by **Upangshu Basak**

Feel free to fork this repository, contribute, and improve it! If you encounter any issues, open an **Issue** or reach out. 🚀


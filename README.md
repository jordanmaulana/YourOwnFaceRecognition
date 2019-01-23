# YourOwnFaceRecognition
Probably the clearest example of face recognition using your very own dataset. This project is using Python, open-cv and TensorFlow. Yes! Say DEEP LEARNING!

## **THE GOAL** 
The goal is to recognize only you and consider other people (not you) as strangers.

## SOURCE & PROGRAMMING INSPIRATION :v:

https://www.geeksforgeeks.org/image-classifier-using-cnn/

https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/

This project is a combination of both sources.

## **REQUIREMENTS**

1. **Python**
   
   I am using python 3.6.4 because the latest version of python is not supported by TensorFlow yet.
   You can download it here https://www.python.org/downloads/

2. **TensorFlow**
   
   You can read how to install it here https://www.tensorflow.org/install/pip
   I am not using virtual environment and just run `pip install --upgrade tensorflow` did it with no issue for me.

3. **tflearn**
   
   Deep learning library featuring a higher-level API for TensorFlow used to create layers of our CNN
   run `pip install tflearn` from your cmd 

4. **open-cv**
   
   To process the image like converting them to grayscale and etc.
   run `pip install opencv-python` 

5. **numpy**
   
   To process the image matrices
   run `pip install numpy`

6. **tqdm**
   
   Instantly make your loops show a smart progress meter, just for simple designing sake
   run `pip install tqdm`

7. **imutils**
   
   run `pip install imutils`

   
## HOW TO DO IT

1. **Run buildData.py** to build your dataset
   - your camera will detect your face using **cv2.CascadeClassifier haarcascade_frontalface_default.xml** and saves it as .png images
   - You can **change your file name on line 39**. (it is "jordan" in my project)
   - In this step, you have to direct the camera to capture only your face.
   - You can be as expressive as possible
   - Capture it from different angles
2. Now, run the first step again, but change your file name into "unknown". This time, capture other people faces to be detected as unknown or strangers, which means not you.
3. Create 2 new folders, name them as **training** and **testing**
4. Move 70% of your images into training folder and the rest 30% into testing folder. Do the same for strangers images.
5. **Run training.py** to generate training files
   - change your training and testing directory on line 9, 10
   - change your label on line 22, 23 according to your file names
6. **Run modelling.py** to generate model files
7. **Run deploy2.py** and enjoy how it works!

If you provide variative dataset of your face (different angle, brightness, contrast), it will mostly produce higher accuracy of your image recognition. So, train as many variative photos of yours.

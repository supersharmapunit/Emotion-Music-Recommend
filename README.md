Music for the Mind: Identify a user's emotional state from a picture or video, and recommend suitable music to fit and/or improve their mood.

# Emotion-Music-Recommendation
Recommending music based on your facial expressions using FER 2013 dataset 

# Project Description:
The project employs an emotion recognition model trained on the FER 2013 dataset, capable of identifying seven different emotions in real-time video feed captured from a webcam. Based on the identified emotion, the app recommends a playlist of songs that match the user's emotional state. The recommended songs are displayed on the screen using a Neumorphism UI design for the website. This allows the user to choose and listen to music that fits their emotional state, enhancing their mood and overall well-being.

# Features:
- Real time expression detection and song recommendations.
- Modern UI for website.

# Running the app:
Flask: 
- Run <code>pip install -r requirements.txt</code> to install all dependencies.
- Run <code>python app.py</code> and give camera permission if asked.

# Tech Stack:
- Keras
- Tensorflow
- Flask

# Dataset:
The dataset used for this project is the famous FER2013 dataset. Models trained on this dataset can classify 7 emotions. The dataset can be found <a href = "https://www.kaggle.com/msambare/fer2013">here</a>.

Note that the dataset is highly imbalanced with happy class having maxiumum representation. This might be a factor resulting in okaysish accuracy after training.

# Model Architecture:
- The model architecture is a sequential model consisting of Conv2d, Maxpool2d, Dropout and Dense layers:
1. Conv2D layers throughout the model have different filter size from 32 to 128, all with activation 'relu'
2. Pooling layers have pool size (2,2)
3. Dropout is set to 0.25 as anything above results in poor performance
4. Final Dense layer has 'softmax' activation for classifying 7 emotions
- Used 'categorical_crossentropy' for loss with 'Adam' optimizer with 'accuracy' metric


# Image Processing and Training:
- The images were normalised, resized to (48,48) and converted to grayscale in batches of 64 with help of 'ImageDataGenerator' in Keras API.
- Training took around 13 hours locally for 75 epochs with an accuracy of ~66 %

# Current condition:
The entire project works perfectly fine. Live detection gives good frame rates due to multithreading.

# Project Components:
- haarcascade is for face detection.
- camera.py is the module for video streaming, frame capturing, prediction and recommendation which are passed to main.py.
- main.py is the main flask application file.
- index.html in 'templates' directory is the web page for the application. Basic HTML and CSS.
- utils.py is an utility module for video streaming of web camera with threads to enable real time detection.
- train.py is the script for image processing and training the model.


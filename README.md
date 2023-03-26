Music for the Mind: Identify a user's emotional state from a picture or video, and recommend suitable music to fit and/or improve their mood.

# Emotion-Music-Recommendation
Recommending music based on your facial expressions using FER 2013 dataset 

# Project Description:
The project employs an emotion recognition model trained on the FER 2013 dataset, capable of identifying seven different emotions in real-time video feed captured from a webcam. Based on the identified emotion, the app recommends a playlist of songs that match the user's emotional state. The recommended songs are displayed on the screen using a Modern UI design for the website. This allows the user to choose and listen to music that fits their emotional state, enhancing their mood and overall well-being.

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


# Project Components:
- haarcascade is for face detection.
- camera.py is the module for video streaming, frame capturing, prediction and recommendation which are passed to main.py.
- main.py is the main flask application file.
- index.html in 'templates' directory is the web page for the application. Basic HTML and CSS.
- utils.py is an utility module for video streaming of web camera with threads to enable real time detection.
- train.py is the script for image processing and pre-trained model.


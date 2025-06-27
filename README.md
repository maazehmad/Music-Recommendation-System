# Music Recommendation System

This is an AI-powered music recommendation system that suggests similar songs based on audio features and provides song lyrics using speech recognition. The system is built using Python, PyTorch, MongoDB, and Flask.

---

## Features

* Find similar songs based on MFCC audio features
* Extract and display lyrics using speech recognition
* Play songs directly from the web interface

---

## Tech Stack

Languages and Libraries: Python, PyTorch, TensorFlow, NumPy, Scikit-learn, Flask, MongoDB
Tools: ffmpeg, SpeechRecognition, eyed3, Pymongo

---

## Requirements

* Python 3.x
* MongoDB
* ffmpeg
* Python Libraries listed in requirements.txt

---

## Installation

1. Clone the repository:

   ```
   git clone https://github.com/your-username/music-recommendation-system.git
   cd music-recommendation-system
   ```

2. Create a virtual environment:

   ```
   python -m venv venv
   source venv/bin/activate   # On Windows use venv\Scripts\activate
   ```

3. Install the required libraries:

   ```
   pip install -r requirements.txt
   ```

4. Install ffmpeg
   Download and install ffmpeg from the official website and ensure it is added to your system's path.

5. Set up MongoDB
   Ensure MongoDB is installed and running locally.
   Create a database named `Audio1` and a collection named `Features1`.

6. Download the FMA Dataset
   Download the `fma_large` dataset and metadata from the FMA website: [https://github.com/mdeff/fma](https://github.com/mdeff/fma)

---

## Model Training

The system uses a Multi-Layer Perceptron (MLP) model to learn audio features and compare similarity between songs.

Steps:

1. Extract MFCC features from audio files:

   ```
   python features.py
   ```

   This will store the extracted features in the MongoDB collection `Audio1.Features1`.

2. Train the model:

   ```
   python train_model.py
   ```

   This script will preprocess the data, train the MLP model using PyTorch, and save the model as `trained_model.pkl`.

---

## Running the Application

Start the Flask application:

```
python app.py
```

This will launch a web interface that allows you to search for songs, view similar recommendations, extract lyrics, and play songs.

## Future Enhancements

* Add genre or mood-based filtering
* Integrate external APIs like Spotify or YouTube
* Improve lyrics accuracy using advanced NLP models

---

## Skills Demonstrated

Audio Processing, Neural Networks, Web Development with Flask, Database Management with MongoDB, Natural Language Processing, Speech Recognition, Data Engineering


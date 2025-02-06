#Emotion Detection in Audio Using Psychoacoustic Models
#Project Overview
This project implements an AI-based emotion detection system for speech audio. It integrates psychoacoustic principles (e.g., loudness perception, pitch sensitivity) with machine learning models to classify emotions from speech data. The model is trained on the RAVDESS dataset and can predict emotions from new audio inputs.
#Features
•	Extracts psychoacoustic features (e.g., loudness, pitch) alongside standard features (MFCC, spectral contrast, etc.).
•	Classifies emotions like happy, sad, angry, neutral, etc. using deep learning.
•	User-friendly prediction function to analyze any speech file.
•	Visualizes model performance with accuracy/loss graphs.
•	Google Colab-based implementation – no local setup required.
#Dataset
The project uses the RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song) dataset. Ensure you upload your dataset to /content/data in Google Colab before running the notebook.
#Download RAVDESS Dataset:
 https://zenodo.org/record/1188976 
Tech Stack
Programming Language: Python
Libraries:
librosa – Audio feature extraction
numpy, pandas – Data processing
scikit-learn – Machine learning utilities
keras, tensorflow – Deep learning framework
matplotlib – Data visualization
#Installation
Open Google Colab and create a new notebook.
Model Architecture
The deep learning model consists of:
Input Layer: 40 MFCC + psychoacoustic features
Hidden Layers:
Fully connected layers (256, 128 neurons)
ReLU activation
Dropout layers for regularization
Output Layer: Softmax activation for emotion classification

#Steps to Run
  #Data Pre-processing
      Extract MFCCs, chroma, mel spectrogram, spectral contrast, tonnetz, RMS (loudness), and zero-crossing rate (pitch sensitivity).
      Encode emotion labels.
Split into training and test sets.
  #Model Training
      Train a dense neural network using keras.
      Run for 50 epochs with batch size 32.
 #Evaluate model accuracy.
    Prediction
      Use predict_emotion() to classify a new speech file.
#Model Performance
    Training accuracy: ~85%
    Test accuracy: ~80%
    Loss and accuracy graphs are plotted for evaluation.


#Future Improvements
    •	Enhance feature extraction using wavelet transforms.
    •	Implement attention-based deep learning models for better accuracy.
    •	Train on multilingual datasets to improve robustness.
    •	Develop a real-time emotion detection web app using Flask or FastAPI.


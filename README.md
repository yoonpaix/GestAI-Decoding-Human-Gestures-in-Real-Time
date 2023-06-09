# GestAI-Decoding-Human-Gestures-in-Real-Time

This repository contains Python code that implements a real-time action recognition system using deep learning and OpenCV. The system captures video from a webcam, detects human body landmarks using MediaPipe's Holistic model, extracts sequences of keypoints from these landmarks, and uses a trained LSTM (Long Short-Term Memory) deep learning model to classify the actions depicted in the sequences.

## Project Structure
The code is organized into several sections:

Import and initialisations: Contains imports of required libraries and initializations of MediaPipe variables.<br>

Function definitions for Landmark Detection and Keypoint Extraction: Contains definitions of landmarks_detection(), draw_styled_landmarks(), get_landmarks(), and extract_keypoints() functions.<br>

Data collection for action recognition: Captures video frames and associated landmark data for a defined set of actions.<br>

Collect keypoint Values for Training and Testing: Extracts sequences of keypoints from the landmarks and stores them for model training and testing.<br>

Preprocessing and Data Organization: Preprocesses the collected data into a suitable format for deep learning and organizes the data into training and testing sets.<br>

Build and Train LSTM Neural Network: Defines and trains an LSTM deep learning model on the preprocessed data.<br>

Making Predictions: Uses the trained model to make predictions on the test data.<br>

Evaluation using Confusion Matrix and Accuracy: Evaluates the model's performance using a confusion matrix and accuracy score.<br>

Using the Model for Real-Time Action Recognition: Uses the trained model to perform real-time action recognition from a webcam feed.<br>

## Usage
Ensure that you have all required dependencies installed. You can install them using pip:
```python
pip install opencv-python mediapipe sklearn tensorflow numpy pandas
```

During the real-time action recognition phase, press 'q' to quit the program.


## Model

The model used in this project is an LSTM network, chosen for its effectiveness in processing sequential data. The model was trained on keypoint data collected and preprocessed by the aforementioned functions.

## Note

The model's performance can be improved by collecting more data, adjusting the confidence parameters in the holistic model, fine-tuning the LSTM model architecture, or adjusting the threshold for prediction probability.

## Dependencies

OpenCV
MediaPipe
Scikit-learn
TensorFlow
NumPy
Pandas

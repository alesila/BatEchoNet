# BatEchoNet🦇
This project explores the use of deep learning techniques to identify bat species from the ultrasonic echolocation recordings, supporting scalable bioacoustic monitoring and biodiversity research. 

--- 

## Objectives:
The main objective of this project is to develop a classification model capable of identifying bat species from ultrasonic audio recordings.

The specific objectives are:

- To process acoustic recordings and transform them into visual representations using spectrograms.

- To train a deep learning model for multiclass species classification.

- To evaluate the model’s performance using metrics appropriate to the problem.

- To analyze the model’s errors from both an acoustic and biological perspective.

---

## Data: 
The audio files were obtained through the XenoCanto.org API. To download files, a profile must be created to obtain a personalized key. More information can be found here: https://xeno-canto.org/explore/api

- 1785 .WAV files were collected and labeled by species
  
- All audios sampled at 192 kHz to preserve ultrasonic information

- Each recording was converted into a mel-spectrogram representation

---

## Methodology:
The project follows an end-to-end machine learning pipeline:

1. Audio preprocessing and standardization

2. Conversion of raw audio to mel-spectrograms

3. Image-based classification using ResNet50 with transfer learning

4. Model evaluation using accuracy, top-3 accuracy, and confusion matrix

Spectrograms are treated as images, allowing the CNN to learn frequency–time patterns characteristic of different bat species.

--- 

## Results: 
The model achieves good validation performance despite limited data. Top-3 accuracy is particularly high, indicating that the correct species is often among the most probable predictions. Furthermore, misclassifications mainly occur between acoustically similar species, which is consistent with biological 
expectations.

---

## Technology used:
- Python
- TensorFlow/Keras
- Librosa
- scikit-learn
- Pandas/NumPy
- Matplotlib
- Streamlit (for prototype deployment)

---

## Project structure: 
1. audio/ (Raw audio files .wav)
   
2. spectrograms/ (Generated spectrogram images)
   
3. Data_collection_and_analysis.ipynb
   
4. Model_training.ipynb
   
5. df_fixed.csv (Audio file labels)
  
6. README.md

# MOSAIC
ML-based project on detection of crackles and wheezes

## Problem Statement
Stethoscope-based respiratory auscultation has long been an important first-line physical exam. The development of stethoscope technology has made it possible to record patient sounds with high quality. This project aims to solve the detection of lung conditions—specifically, crackles and wheezes—through the use of machine learning algorithms.

For a given digital dataset, in the form of text and audio files, we can form spectrogram images, which are then used for model training. Once the model is trained, it can make predictions on the **presence/absence of crackles** and the **presence/absence of wheezes**. This helps in detecting unhealthy symptoms in patients.

**Wheezing**:
A high-pitched hissing sound that's similar to a deflating balloon. It's often caused by air passing through a narrowed airway at high speed, and is commonly associated with asthma and emphysema. 

**Crackles**:
An interrupted or explosive sound that can sound like rattling, bubbling, or clicking. It's usually caused by the opening of airways in areas of the lung that are deflated, and is a sign of too much fluid in the lung. Crackles are often only heard with a stethoscope. 

## Solution
1. **Audio to Image Conversion**: We converted the audio files (.wav) to images using the `librosa` library to better visualize and analyze the audio.
  
2. **Data Preprocessing**: We paired the audio files with their corresponding text files. After reading the text file, we split the audio file based on timestamps. The separated audio segments are then passed through the `features_extractor` function.

3. **Feature Extraction**: Inside the `features_extractor` function, we converted the audio to images and extracted features using **MFCC (Mel-frequency cepstral coefficients)**.

4. **Model Prediction**: The model predicts four possible outcomes based on the input:
   - **Presence of crackles**
   - **Absence of crackles**
   - **Presence of wheezes**
   - **Absence of wheezes**

The model helps in detecting unhealthy symptoms in patients by analyzing these features.

## Diagnosis of Lung Abnormalities (Feb 2023 - June 2023)

- **Audio Analysis**: Processed 2,000 lung sound files into spectrograms using **Librosa**.
- **Model Accuracy**: Achieved 96% accuracy with a CNN model.
- **Tech Stack**: Python, Librosa, CNN

### Why Librosa?
Librosa was chosen for this project due to its powerful and efficient capabilities for audio processing and feature extraction. It offers several tools specifically designed for working with audio signals, making it ideal for tasks like converting audio to spectrograms and extracting features such as **MFCCs** (Mel-frequency cepstral coefficients), which are essential for analyzing sound patterns in the lungs. Its simple and intuitive API allowed for quick development and integration into the machine learning pipeline, ensuring high-quality audio data preprocessing for accurate model predictions.

More About **MFCCs** [https://en.wikipedia.org/wiki/Mel-frequency_cepstrum#:~:text=In%20sound%20processing%2C%20the%20mel,collectively%20make%20up%20an%20MFC.]

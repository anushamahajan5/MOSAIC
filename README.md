# MOSAIC
ML-based project on detection of crackles and wheezes
# PROBLEM-STATEMENT : 
Stethoscope-based respiratory auscultation has long been an important
first-line physical exam.The development of stethoscope technology has made it possible to
record patient sounds with high quality.The project here aims to solve one such lung condition—wheezes and
crackles—through the use of machine learning algorithm.For a given digital data, in the form of text and audio files we can form
spectrophotogram figures and further model training can beaccomplished.
Once, we train the model ,it makes predictions on Presence/absence of
crackles and Presence/absence of wheezes.
In this we can detect any unhealthy symptom of patients

# SOLUTION: 
* We converted the audio file to theimage using the librosa library to get an idea of the audio .
* we started the preprocessing of thedata, for this we paired the audio file (.wav) and corresponding text file.Then we read the text file and split the audio file on the basis of timestamps along with this we pass the separated images in the function "features_extractor"
* Inside that function we converted the audio to image and extracted the feature using MFCC(Mel-frequency cepstral coefficients)
* The four possible outputs will be predicted as follows: The presence of crackles and wheezes both are determined


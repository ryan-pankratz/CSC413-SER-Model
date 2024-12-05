A repository for our CSC413 final project. A Speech Emotion Recognition model.

For our dataset, we make use of the RAVDESS dataset found here: https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio

For our features, we use the MFCCs, Zero Crossing Rate, Melspectrogram, chroma STFT, and Root mean square energy. Our data was stored in 16Khz and we used Google's WebRTCVad to remove unnecessary noise. 
As we are not audio experts, we used the features that others have found success with in the past (and due to many long hours of trying to work with openSMILE). Specifically, we used the features that were successful 
when used in this model: https://www.kaggle.com/code/shivamburnwal/speech-emotion-recognition. But unlike their model, we used a Bi-directional LSTM and kept the variable size dimensions instead of averaging them out.

Our data splitting was done in the CSC-413_Data_Split.ipynb, here, we also used WebRTCVad to clean the extra noise, and data augment the training data in order to avoid overfitting as best we could. It was then saved back 
into a .wav file and in 16 KHz.

Our Modelling was done in CSC-413_Project.ipynb, here we also did the feature extraction from the .wav files, and also modelled both our model with and without dropout layers to test if the layer helped.

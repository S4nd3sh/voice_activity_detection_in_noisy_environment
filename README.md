# Voice activity detection in noisy environment

The project was developed in Google Colab GPU environment and the training of the model generally takes about 6-8 hours on CPU for about 500 sample audio files where as the model training takes about 10-15 mins on GPU for the same amount of the utterances.

Dataset can be downloaded and extracted from : https://ai.googleblog.com/2017/08/launching-speech-commands-dataset.html

The audio files were manually sampled from each utterance and saved in a single file for my project rather than how it is present in the extracted compressed files in multiple folders.

The audio data was converted to spectrograms via framing using hamming window.

The spectrograms generated was used to train CNN to develop a model to predict the mask that was initially generated using the thresholding technique on the signal without the presence of noise.

The trained model is available in h5 file format at : https://drive.google.com/open?id=1nY3fAWb6SHOy0FvzlaBGUf6C-JTEFrMH

The required code to reload the model is provided at the end to load and make predictions.

Speech validation signal with noise and after multiplying with the mask genreated from CNN is available in the same location as model.

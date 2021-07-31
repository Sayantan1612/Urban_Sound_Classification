# Urban_Sound_Classification

Project created during training cum internship in iSmriti IIT KANPUR

It’s a Classification Problem. Data-set taken from TUT DCASE 2017.
Classify 1800-odd Audio Samples into 4 categories:
1. Baby cry
2. Glass Break
3. Gun shot
4. Others

-> Done in python in Google Co lab Notebooks.

->Uploaded the data in Git-Hub after cleaning. 1800->1500 odd samples.

-> Libraries used are:
Numpy: Python Library to work with fast Fourier transforms and arrays and do other linear algebra problems.
Keras: It’s an open source neural network library to import models.
Sklearn: Software that provides free algorithms and techniques for classification, regression etc. Type of Problems.
Librosa: It’s a python library for audio files. To extract the feature of an audio file.

->After Loading the audio files, we used Librosa to extract the features from the audio files like wavelength,Zero crossing rate (Sign change +ve to -ve) , Spectrum centre (centre of mass) and mainly the MFCC (consists of 10-20 features in itself)

->MFCC Mel-Frequency Cepstral Coefficients:
Audio signal is divided into time frames.
Cepstrum is the information rate of change in spectral bands.
Then there is a filter bank which is responsible for frequency scaling.
Then Fourier transform takes place which make the feature vectors.
->So the audio file had been converted and had 20 features for each audio file.
->Now we needed to Label the 4 categories and for the machine to understand and distinguish easily, we converted them to binary using the One-hot encoding technique.
->Then we split the data-set into Training (80%) and Testing (20%).
->We are asked to try out Sequential Model from Keras:

Sequential Model:
Deep Learning/Neural Network Model
This model is Appropriate for a plain stack of layers where each    		layer has exactly one input and one output tensor.	
Activation layer is like a mathematical gate for input feeding to a 			current neutron to go to its output.
We had used “relu” as activation layer. Rectified Linear Units.
F(x)=max(0,x);

The performance measure of the model was done by the Cross 			Entropy Loss gives a value between 0 and 1.
->Accuracy was 79%.(Bad on training data)
->Accuracy on testing data was around 70%.
->Metrics used: F1 Score, Evaluation Matrix/Confusion Matrix.

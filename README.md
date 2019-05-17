# DeepLearning_CNN_LanguageIdentification

Language Identification from Audio File using the Deep Learning CNN Model

YouTube Video Tutorial URLs: <br>
   2 minutes video: https://youtu.be/8jNt1EIKpxc <br>
   15 minutes video: https://youtu.be/FFq7wMZ5fnY <br>


READ ME
---------------

This is brief notes explaining the contents of the ModelAndData.zip folder and the steps you need to follow if you want to use the real data set from the specified website. 

(1) Extract the contents of ModelAndData.zip folder to your desired location.

(2) When you extract it you will the following directory structure

ModelAndData/
	.
	./images		(this folder has image files embedded in jupyter notebook)
	./dataDir 		(this is a CRITICAL base working directory for data with in the jupyter notebook.)
	./dataDir/Training data 	(this folder has tiny dataset of around 248 audio MP3 files)
	./datadir/trainingData.csv  (this csv file has output labels for each audio input file)
	./readme.txt				(this is the readme.txt)
	./LanguageIdentificationModel_FakruddinMohammed_V4.ipynb 	(this is jupyter notebook to run the model)

(3) To run the model, you must start the "jupyter notebook" from the directory where the model.zip has been extracted. Otherwise, the jupyter notebook wont be able to find the 'dataDir' folder. 

(4) For whatever reasons if you cannot start from the extracted zip folder, you will have to edit the following line in the "LanguageIdentificationModel_FakruddinMohammed_V4.ipynb" jupyter notebook. 

Edit the following line to the suitable location where the zip files are extracted.

base = './dataDir'


(5) Open the supplied jupyter notebook "LanguageIdentificationModel_FakruddinMohammed_V4.ipynb", then click on run-> all cells.

(6) The model will take the data and output labels from the following directories and will start running the model

./dataDir/Training data
./dataDir/trainingData.csv

(7) Since the model is giving the best performance for spectrogram image size of 32x32 and for MFCC vector size od 11, the model is set to run using these feature vector sizes and using the tiny sample data of (248 files)

(8) The model produces the loss & accuracy results, for the following:
	(a) Spectrogram 32x32 (without data augmentation)
	(b) Spectrogram 32x32 (with data augmentation)
	(c) MFCC vector size 11 (without data augmentation)
	(d) MFCC vector size 11 (with data augmentation)

(9) If you would like to run the model for different feature vector sizes, then edit the following lines

For spectrogram size, edit the following two lines

height=32
width=32

For MFCC feature vector size, edit the following line

feature_dim_2 = 11


(10) If you would like to run the model on full data set downloaded from the website, then extract the contents of audio MP3 files to the following location:

./dataDir/Training data
./dataDir/trainingData.csv


Requirements
--------------

Python system libraries
----------------------
os <br>
shutil <br>
glob <br>
pathlib <br>

Python audio speech processing library
------------------------------------
librosa <br>
Python data processing and plotting libraries
------------------------------------
pandas <br>
numpy <br>
scipy <br>
matplotlib <br>
imageio <br>
skimage <br>
seaborn <br>
IPython <br>
plotly <br>
tqdm <br>

Python machine learning libraries
------------------------------------
sklearn <br>
keras <br>
tensotflow <br>

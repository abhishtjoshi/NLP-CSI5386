			---------------NLP Assignment 2---------------------


Assignment 2 is performed using Google Colab platform and Kaggle platform.  

Part 1:
_________________ 

Pre-trained Model:

Download the model zip file.
Unzip the model. In the folder where CUAD main data is present.
Run the ipynb file.

Fine Tuning Model:
Upload the CUAD data to Kaggle along with the ipynb file.
Import notebook to kaggle and Run the notebook.

 
Part 2: 
_________________ 

Upload all the Merge input txt files on google drive [Training Dataset, Testing Dataset]

Mount the Google drive to Google Colab, to access the Data present in Google Drive. 

Open the txt file for which you want to run the models and read lines from the files using read(). 

Perform data preprocessing on the file and run the file for different models 

For each model import Libraries and install the models and libraries (Sentence Transformer, Torch) as mentioned in IPYNB file. 

Run the model and compare the cosine similarity after fitting the tuning parameters. 

----SBert---- 

Install sentence transformer using “!pip install -U sentence-transformers” 

Using model 'all-MiniLM-L6-v2' and 'all-mpnet-base-v2'

	“from sentence_transformers import SentenceTransformer, util” 

Tuning parameters:
	
	epochs=4,3 and Batch Size=64


----SimCSE---- 

Install the SimCSE  

“!pip install simcse” 

Evaluate the Pearson Correlation(PC) value and reevaluate after applying hyper-parameter tuning.

Parameters decided based on combination and significant improvement in the PC value: combination of epochs [1 to 10] and batch size [16, 32, 64]. 
--------------------------------------------------------------------------


Performed the Pearson Correlation between the output/result file with the GS files by using the correlation-noconfidence.pl script and command mentioned below:

“   ./correlation-noconfidence.pl STS2016.gs.<dataset>.txt \ 

                                 SYSTEM_OUT.<dataset>.txt” 


 
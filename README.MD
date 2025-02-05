Bengali Lexical Simplification

# Overview

- This  file provides instructions for running the Bengali lexical simplification code on Google Colab. The process involves uploading multiple datasets, running the code for different models, and evaluating the results using various metrics.

- Running the BERT models(XLM-Roberta and sagorsarkar) with or without helper function for all three datasets as described below. 


# Requirements
- Google Colab: This code is designed to run on Google Colab, which provides the necessary environment, including GPU support for deep learning models.
- Python Libraries: Ensure the following libraries are installed in your Colab environment:

	* transformers
	* torch
	* datasets
	* wordfreq
	* tensorflow
	* pandas
	* sacrebleu
	* nltk
	* genism

- The code installs these libraries as needed, so no prior installation is required.

# Input Files
- Before running the code, prepare the following files to be uploaded to the Colab session:
- Datasets

	* Evaluationdataset1.txt
	* Evaluationdataset2.txt
	* Evaluationdataset3.txt
        * GroundTruth1.xlsx
	* GroundTruth2.xlsx
	* GroundTruth3.xlsx

  

- Ground Truth File: This file contains sentences with complex words and their simplified alternatives in an Excel format.
  Ground Truth1.xlsx (You can rename or use different ground truth files, but ensure they are in the expected format with columns: 'sentence', 'complex_words', and 'simplified_words').      

- BERT Model Result Files: These are the output files from the BERT models' predictions.
- For example, sagordataset1withhelp.txt or Robertadataset1nohelp.xlsx.

# Steps to Run the Code on Google Colab for BERT models

- Upload Files: The code will prompt you to upload specific files at each stage. Please ensure you upload the correct file as requested. You can manually upload the files by clicking on  the "Choose Files" button in the Colab file upload dialog.

- Evaluation Datasets: Upload Evaluationdataset1.txt, Evaluationdataset2.txt, and Evaluationdataset3.txt when prompted.


# Steps to run the Evaluation script on google colab:

- Ground Truth File: Upload GroundTruth1.xlsx, GroundTruth2.xlsx, GroundTruth3.xlsx in the upload section on top left side on colab for the ground truth data.

- BERT Model Result Files: The result datasets will be downloaded automatically in the current working directory(e.g., sagordataset1withhelp.xlsx) when evaluating the model's performance.

# Run the Code: Follow these steps to execute the code:

- Open the Colab notebook.
- Run the first code block to install necessary libraries.
- The script includes complex word identification, BERT model predictions(after running files will be directly downloaded from colab environment), and evaluation scripts using various metrics (Precision, Recall, F1-score, Accuracy, BLEU, SARI).
- Execute each code block sequentially as prompted, ensuring you upload the correct file when the script requests it.
- The code will process the files, generate predictions, and evaluate the results using the provided metrics.


# Evaluate Results:
- The code uses  BERT model’s output, the ground truth file and the Evaluation file to compare with each other and identify complex word and understand which complex words replaced correctly with its valid synonyms as per the GrounfTruth Files. After comparing, Precision, Recall, F1-score, Accuracy of the model is calculated. For the evaluation script result will show in the google colab itself.

- The final output includes confusion matrices, evaluation scores, and predicted sentences.


# Notes
- Manual File Uploads: During the execution of the code, you'll be prompted to upload specific files. Ensure that you upload the correct files as mentioned above at each step.
- File Formats: The ground truth and evaluation files are expected to be in Excel or text format. The ground truth file must have columns labeled 'sentence', 'complex_words', and 'simplified_words'.
- Customising Input: You can modify the input filenames as long as they match the expected structure in the code.

# Example Usage for BERT Models
- Run the codes separately for the three evaluation datasets for the BERT models XLM-Roberta and Sagorsarkar(with or without helper function)
- For example, For running XLM-Roberta with or without helper function.
 	* Upload Evaluationdataset1.txt when prompted.
	* Then after evaluation the resultant file will be obtained. 
 	* Same process will be followed for Evaluationdataset2 and Evaluationdataset3.
- Same above process will be repeated for Sagorsarkar BERT model as well for all three Evaluation dataset.



# Example usage for Evaluation script
- For running the Evaluation script, we have to upload GroudTruthfile, XLM-Roberta's output file(with or without helper function) and main Evaluation file for the comparison and obtain the metrices.
- Same evaluate the all datasets produced by BERT models for Evaluationdataset1, Evaluationdataset1,Evaluationdataset1.


# conclusion
- This guide has explained how to run the Bengali lexical simplification code on Google Colab, including how to upload the necessary files, run the models, and evaluate their performance. 
-Make sure to have your datasets ready and upload them when the code asks for them.

- This project is flexible, so you can try using different datasets and models to see what works best. For more details or changes, check the comments in the code for guidance.




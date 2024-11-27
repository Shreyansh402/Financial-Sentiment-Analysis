# Financial-Sentiment-Analysis
Analyzing text data in the financial domain to extract meaningful insights. Specifically, the goal is twofold: Aspect Detection: Identify the relevant aspects or target topics mentioned in the text from a pre-defined list of aspect classes. Sentiment Analysis: Predict the sentiment score for each identified aspect. 

Project Overview
The objective of this project is to predict:
	1	Aspects: The primary financial category discussed in the text, such as "Corporate," "Market," etc.
	2	Sentiment Score and Label: A numerical sentiment score ranging from -1 to 1 and a corresponding label (Negative, Neutral, or Positive).
This project employs a pipeline-based model architecture, which consists of two separate stages:
	1	Aspect Classification Model:
		Predicts the main financial category of the text.
		Uses a fine-tuned transformer-based model (FinBERT) for classification.
	2	Sentiment Regression Model:
		Predicts the sentiment score for the text.
		Converts the sentiment score into a label: Negative (0), Neutral (1), or Positive (2).
This pipeline approach ensures that each task is optimized individually, resulting in better overall performance and interpretability compared to combined multitask architectures.

Files Included
	1	Code File (code.txt):
		This file contains all the Python code required for the project, including:
		Data preprocessing and exploratory data analysis (EDA).
		Implementation of the pipeline model for aspect classification and sentiment analysis.
		Training, evaluation, and prediction scripts.
		Instructions to execute the code are provided in the next section.
	2	Output File (output.pdf):
		Converted from the Jupyter Notebook, this file includes:
		EDA plots and insights about the dataset.
		Results from the pipeline model's training and evaluation phases.
		Metrics for both aspect classification and sentiment regression tasks.
		Sample predictions from the trained model.

How to Run the Code
Execution Steps:
	1	Load the dataset:
		The code is designed to use the FIQA 2018 dataset, containing three splits: train, validation, and test.
		Ensure these files are loaded correctly, and modify the paths in the code to point to your dataset files if needed.
		The dataset must contain the following columns: sentence, aspects, and sentiment_score. Ensure that these columns are preprocessed as demonstrated in the code (e.g., splitting aspects into main categories, creating sentiment labels from scores).
	2	Training the models:
		Execute the training scripts for the aspect classification and sentiment regression models.
		Pre-trained FinBERT weights are used for initialization, ensuring robust baseline performance.
	3	Testing the models:
		To test the models on new data:
		Replace the test dataset with your custom data in the format:
		sentence: The financial text.
		aspects: Placeholder values if aspect predictions are required (they will be ignored during inference).
		sentiment_score: Placeholder values, as predictions will be generated by the sentiment regression model.
		Modify the input paths in the code to point to your custom test file.
		The models will output both predicted aspects and sentiment scores/labels for the test data.
	4	Making predictions:
		Use the provided prediction function to input any custom text and retrieve its predicted aspect and sentiment score/label.

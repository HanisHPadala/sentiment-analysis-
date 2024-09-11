# sentiment-analysis-
YouTube Comment Sentiment Analysis
Overview
This project uses a fine-tuned BERT model to classify the sentiment of YouTube comments into three categories: positive, neutral, and negative. The project includes fetching comments from YouTube, preprocessing them, fine-tuning a BERT model, and analyzing sentiment distribution.

Requirements
Python 3.x
PyTorch
Transformers
scikit-learn
Matplotlib
Google API Client
You can install the necessary packages using pip:

bash
pip install torch transformers scikit-learn matplotlib google-api-python-client
Setup
Obtain a YouTube API Key: You need a YouTube Data API key to fetch comments. You can get it from the Google Developer Console.

Prepare the Video ID: Find the ID of the YouTube video you want to analyze.

Usage
Replace Placeholders:

Update the api_key variable in the main() function with your YouTube API key.
Update the video_id variable with the ID of the YouTube video you want to analyze.
Run the Script: Execute the script by running:

bash
python script.py
This will:

Fetch comments from the specified YouTube video.
Fine-tune a BERT model on a subset of comments.
Predict sentiment labels for comments.
Print accuracy of the model on the validation set.
Display a bar chart showing the distribution of sentiments.
Code Structure
SentimentDataset: Custom dataset class for loading and tokenizing text data.
preprocess_for_finetuning: Prepares the dataset for fine-tuning.
fine_tune_model: Fine-tunes the BERT model on the training data.
fetch_youtube_comments: Fetches comments from YouTube using the API.
preprocess_comments_batch: Prepares comments for model evaluation.
evaluate_comments: Predicts sentiment labels using the fine-tuned model.
analyze_and_visualize_sentiments: Analyzes and visualizes the sentiment distribution.
Troubleshooting
API Key Issues: Ensure your YouTube API key is valid and has the necessary permissions.
Insufficient Comments: If there are fewer than 60 comments, the model may not train effectively. Try using a different video or collecting more comments.

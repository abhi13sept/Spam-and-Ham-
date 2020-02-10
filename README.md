# Spam-and-Ham
Spam and Ham Classifier using Python 

# Dataset: 
The dataset used for this project is UCI SMS spam collection dataset. Link: https://www.kaggle.com/uciml/sms-spam-collection-dataset/

It's a spam classifier program in python which can tell whether a given message is spam or ham.It is done using theorem from probability theory called Baye’s Theorem.

# 1.Loading Libraries

I am using NLTK for processing the messages, WordCloud and matplotlib for visualization and pandas for loading data, NumPy for generating random probabilities for train-test split.

# 2.Load Data

We load the data and the dataframe is created accordingly for train and test split.

# 3.Test and Train Split

To test the model the data is split into train dataset and test dataset. The train dataset is used to train the model and then it will be tested on the test dataset. I used 75% of the dataset as train dataset and the rest as test dataset. Selection of this 75% of the data is uniformly random.

# 4.Visualizing the data

The matplotlib and WordCloud dependencies are used in the visualization of data.

# Spam Data
![]()

# Ham Data
![]()

# 5.Training Model

I have used two techniques for it:
1.Bag of Words
2.TF-IDF

Data PreProcessing :
Before starting the trainig data is preprocessed.First the all the words are converted to lowercase.
Then we tokenize the words doing this we remove the punctuations in it and splitting the message in peices.
The words like ‘go’, ‘goes’, ‘going’ indicate the same activity. We can replace all these words by a single word ‘go’. This is called stemming. We are going to use Porter Stemmer.
The we remove the stop words like 'a','the','is' and so on. As these words do not provide any information about the context of the text.

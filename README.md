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
There are simple text cleaning techniques that can be used as a first step, such as:

 1. Ignoring case
 2. Ignoring punctuation
 3. Ignoring frequent words that don’t contain much information, called stop words, like “a,” “of,” etc.
 4. Reducing words to their stem (e.g. “play” from “playing”) using stemming algorithms(ProterStemmer).

Bag of Words:

A popular and simple method of feature extraction with text data is called the bag-of-words model of text.

A bag-of-words is a representation of text that describes the occurrence of words within a document. It involves two things:

  1. A vocabulary of known words.
  2. A measure of the presence of known words.
It is called a “bag” of words, because any information about the order or structure of words in the document is discarded. The model is only concerned with whether known words occur in the document, not where in the document.

TF-IDF:

TF: Term Frequency, which measures how frequently a term occurs in a document. Since every document is different in length, it is possible that a term would appear much more times in long documents than shorter ones. Thus, the term frequency is often divided by the document length (aka. the total number of terms in the document) as a way of normalization:

TF(t) = (Number of times term t appears in a document) / (Total number of terms in the document).

IDF: Inverse Document Frequency, which measures how important a term is. While computing TF, all terms are considered equally important. However it is known that certain terms, such as "is", "of", and "that", may appear a lot of times but have little importance. Thus we need to weigh down the frequent terms while scale up the rare ones, by computing the following:

IDF(t) = log_e(Total number of documents / Number of documents with term t in it).

# 6.Classification

For classifying a given message, first we preprocess it. For each word w in the processed messaged we find a product of P(w|spam). If w does not exist in the train dataset we take TF(w) as 0 and find P(w|spam).We multiply this product with P(spam) The resultant product is the P(spam|message). Similarly, we find P(ham|message). Whichever probability among these two is greater, the corresponding tag (spam or ham) is assigned to the input message.

# 7.Result
![]()

# For Further Reading 

Navie Bayes Theorem:https://en.wikipedia.org/wiki/Naive_Bayes_classifier
Techniques used: Bag of words - https://en.wikipedia.org/wiki/Bag-of-words_model
                 TF-IDF - https://en.wikipedia.org/wiki/Tf%E2%80%93idf
Pre-Processing Techniques: Tokenization - https://nlp.stanford.edu/IR-book/html/htmledition/tokenization-1.html
                           Stop words - https://www.geeksforgeeks.org/removing-stop-words-nltk-python/
                           Stemming - https://nlp.stanford.edu/IR-book/html/htmledition/stemming-and-lemmatization-1.html


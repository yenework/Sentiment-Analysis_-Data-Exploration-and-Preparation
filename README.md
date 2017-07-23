# Sentiment-Analysis_-Data-Exploration-and-Preparation
The dataset I chose to work on it is the “A Large Movie Review Dataset” which is found at http://ai.stanford.edu/~amaas/data/sentiment/.  In this section the data preparation process is  discussed. 

In any data science project, it is very import to explore the data and prepare it to employ machine learning algorithm for analytics. Accordingly, the data set was imported and explored and then necessary preparations such as cleaning the dataset, transforming words into feature vectors, tokenizing and stemming documents and stop words into individual words have been performed as follows.

CLEANING DATA

After the data was imported and explored, one of the steps of preparing the dataset was cleaning it.  The purpose of cleaning the data is to remove non-letter characters that are not related to emotion. To do so, regex library from python was used.  As can be seen below the non-letter character such as <, > and / are removed after cleaning the data.

REPRESENTING TEXT AS NUMERICAL FEATURE VECTORS 

To employ machine learning algorithm, categorical data should be converted to numerical form. To convert the text data to numerical form, the bag- of -words model was employed.

CountVectorize class from scikit-learn was implemented to build bag of words model and fit_transform on the coutVectrorize transformed the given corpus to feature vectors as can be seen below. In addition, the TfidTransformer, from Scikit-learn was used to transform frequently occurring words that do not contain useful information into tf-idf.

TOKENIZATION AND STEMMING

Before moving to developing a machine learning model on the cleaned data, the text corpa was split into individual words of the root form. To do so, tokenization and a technique called Word stemming were employed. While the tokenizer splits text corpa into individual words the word stemming technique stems the words to their root form.  For this process, Lancater stemmer algorithm and Porter stemmer algorithm from the NLTK package were used.     

STOP WORDS
 
To remove extremely common words such as is, and has etc., the English 127 stop word set, which is available from NLTK library was used .

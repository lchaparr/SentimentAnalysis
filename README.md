# SentimentAnalysis
Sentiment Analysis over tweets with Security topics.
The code explores the performance of different kinds of sentiment analysis

## Lexicon Method
Lexicon-based: count number of positive and negative words in given text and the larger count will be the sentiment of text.

## Traditional ML
Machine learning based approach: Develop a classification model, which is trained using the pre-labeled dataset of positive, negative, and neutral.

### Bag of Words (BOW):
The bag-of-words model is one of the simplest language models used in NLP. It makes an unigram model of the text by keeping track of the number of occurences of each word. This can later be used as a features for Text Classifiers. BOW model is a common way of representing text data as input feature vector to an ML model. 

To vectorized the features the code uses:
	CountVectorizer()

### TF-IDF.
In Term Frequency(TF), you just count the number of words occurred in each document. The main issue with this Term Frequency is that it will give more weight to longer documents. Term frequency is basically the output of the BoW model.

IDF(Inverse Document Frequency) measures the amount of information a given word provides across the document. IDF is the logarithmically scaled inverse ratio of the number of documents that contain the word and the total number of documents.

TF-IDF(Term Frequency-Inverse Document Frequency) normalizes the document term matrix. It is the product of TF and IDF. Word with high tf-idf in a document, it is most of the times occurred in given documents and must be absent in the other documents. So the words must be a signature word.

To vectorized the features the code uses:
	TfidfVectorizer()


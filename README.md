# SentimentAnalysis
Sentiment analysis is the interpretation and classification of emotions (positive, negative and neutral) within text data using text analysis techniques.

The code explores the performance of different kinds of sentiment analysis over tweets with Security topics.

## Lexicon Method
Rule based sentiment analysis refers to the study conducted by the language experts. The outcome of this study is a set of rules (also known as lexicon or sentiment lexicon) according to which the words classified are either positive or negative along with their corresponding intensity measure.

In Rule-base approach, we take into account to measures: polarity and subjetivity.

*Polarity:* it is a measurement of how positive or negative the given problem instance is. In other words, it is related to the emotion of the given text.

*Subjectivity:* It refers to opinions or views (can be allegations, expressions or speculations) that need to be analyzed in the given context of the problem statement. The more subjective the instance is, the less objective it becomes and vice versa.

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

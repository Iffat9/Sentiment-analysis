# Sentiment-analysis
Sentiment analysis is one of the most popular applications of natural language processing and text analytics.
The idea is to analyze and understand the reactions of people toward a specific entity and take insightful actions 
based on their sentiment.

IMDB movie reviews dataset is been used for the sentiment aalysis.
The dataset contains 50000 reviews, labeled as positive or negative.
predicting the sentiment of 15000 labeled movie reviews and use the remaining 35000 reviews for training our supervised models

text_normalizer file is used for cleaning, pre-processing, and normalizing text to bring text components like phrases and words
to some standard format.

cleaning text: Our text often contains unnecessary content like HTML tags, which do not
add much value when analyzing sentiment. Hence we need to make sure we remove them
before extracting features. The BeautifulSoup library does an excellent job in providing
necessary functions for this.

Removing accented characters: In our dataset, we are dealing with reviews in the
English language so we need to make sure that characters with any other format, especially
accented characters are converted and standardized into ASCII characters. A simple example
would be converting é to e.

Expanding contractions: In the English language, contractions are basically shortened
versions of words or syllables. These shortened versions of existing words or phrases are created
by removing specific letters and sounds. Examples would be, expand "don’t" to "do not" and "I’d" to 
"I would". Contractions pose a problem in text normalization because we have to deal with special
characters like the apostrophe and we also have to convert each contraction to its expanded,
original form.

Removing special characters: Another important task in text cleaning and
normalization is to remove special characters and symbols that often add to the extra
noise in unstructured text. Simple regular expression can be used to achieve this. Its your choice to retain
numbers or remove them, if you do not want them in your normalized corpus.

Removing stop words: Words which have little or no significance especially when
constructing meaningful features from text are also known as stop words. Words like a, an, the,
and so on are considered to be stopwords. There is no universal stopword list but we use a
standard English language stopwords list from nltk. You can also add your own domain specific
stopwords if needed.

Stemming and Lemmatization: Word stems are usually the base form of possible
words that can be created by attaching affixes like prefixes and suffixes to the stem to create
new words. This is known as inflection. The reverse process of obtaining the base form of a
word is known as stemming. A simple example are the words WATCHES, WATCHING, and
WATCHED. They have the word root stem WATCH as the base form.

Lemmatization is very similar to stemming, where we remove word affixes to
get to the base form of a word. However the base form in this case is known as the root word
but not the root stem. The difference being that the root word is always a lexicographically
correct word (present in the dictionary) but the root stem may not be so. We will be using
Lemmatization only in our normalization pipeline to retain lexicographically correct words.

supervised sentiment analysis:

The major steps to achieve this are mentioned as follows :
1. Prepare train and test datasets (optionally a validation dataset)
2. Pre-process and normalize text documents
3. Feature engineering
4. Model training
5. Model prediction and evaluation



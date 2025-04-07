
## **Prerequisites**

- Python 
- Pandas 
- NLTK
- Spacy


## **Resources :**

- NLTK : https://www.nltk.org/api/nltk.tokenize.html 
- PANDAS : https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html
- SPACY : https://spacy.io/usage/spacy-101 
- Regex cheasheet : see python's re module documentation https://docs.python.org/3/library/re.html  


## **Database**

We will use the PLOS narrativity database

This database is used in a scientific article about the **importance of narrativity** in the citation frequency of climate change scientific articles.  https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0167983  


## **Tasks**

### 1. Basic preprocessing
- 1.1 Open the database. Generate simple statistics about the abstracts. How many unique articles are there (Tips: check pmid)? What is the mean length of abstracts in characters (Tips: Check ab)? 

### 2. Word-level preprocessing
- 2.1 Split the abstracts into list of words. How many different words are there in the vocabulary? 
- 2.2 Split the abstracts into list of words using three different tokenizers from nltk. e.g : tokenizers = [TreebankWordTokenizer(), ToktokTokenizer(), TweetTokenizer()]  What is the difference in terms of number of words? What do you think has changed?


### 3. Domain specificity and regex
- 3.1 Use regex to retrieve numbers (ints, floats, %, years, ...) using a regex. 
- 3.2 How many percent of characters are numbers (as defined above) in a given abstract? 


### 4. Classic NLP Pipeline to Represent Data
- 4.0 Re-tokenize using spacy
- 4.1 Lemmatize using spacy
- 4.2 POS tagging using spacy, plot the trees
- 4.3 NER using spacy, give the amount of each entity type for a given abstract

### 5. Topic Modelling
- 5.1 Use Gensim's LDA to compute a topic model. 
- 5.2 Use PyLDAvis to visualise the topic model. What are the different topic clusters?
- 5.3 Use a tf-idf representation for each abstract, and use your favorite clustering algorithm.
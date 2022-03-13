# word2vec, open the blackBox
In this repository, you can see what is in Gensim word2vec pre-trained model

Word2vec is a technique for natural language processing published in 2013. The word2vec algorithm uses a neural network model to learn word associations from a large corpus of text. Once trained, such a model can detect synonymous words or suggest additional words for a partial sentence. As the name implies, word2vec represents each distinct word with a particular list of numbers called a vector. The vectors are chosen carefully such that a simple mathematical function (the cosine similarity between the vectors) indicates the level of semantic similarity between the words represented by those vectors (wikiPedia).

Gensim is an open source python library for natural language processing and it was developed and is maintained by the Czech natural language processing researcher Radim Řehůřek. Gensim library will enable us to develop word embeddings by training our own word2vec models on a custom corpus.

The Word2Vec model (300) trained on part of the Google News dataset, covering approximately 3.2 million words and phrases and about 900 millions connections. Such a model can take hours to train, but since it’s already available, downloading and loading it with Gensim takes minutes.

Download link : https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit?resourcekey=0-wjGZdNAUop6WykTtMip30g
After obtaining 3GB package, a following code used to extract words and phrases from Word2vec pretrained model:
```from gensim import models
import gensim.downloader as api
import numpy as np # linear algebra
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)
import os
import nltk
import gensim

url="C:/gensim-data/word2vec-google-news-300/word2vec-google-news-300.gz"

from gensim.models.keyedvectors import KeyedVectors
model = KeyedVectors.load_word2vec_format(url, binary=True)
model.save_word2vec_format('GoogleNews-vectors-negative300', binary=False)
```


The result is this text file (actual size is about 43 MB): word2vec_content.zip


The motivation of this project is to show words and phrases in word2vec. Normally it is a blackbox. It would be helpful to follow up projects like clustering.

References:
https://radimrehurek.com

https://github.com/mmihaltz/word2vec-GoogleNews-vectors

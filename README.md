# MAPD-mod-B-project
### MAPD-B distributed processing exam default projects

Analysis of Covid-19 papers

1. We implement a distributed algorithm to count the occurrences of all the words inside a list of documents using Bag data-structure of DASK. Here, we explain the algorithm step by step and in the end we wrap all the steps inside a single function in order to test the computational time required by the algorithm as a function of the number of cluster workers and the number of data partitions.

The algorithm is divided into two parts:

+ **Map phase** : For each document $D_i$, produce the set of intermediate pairs $(w, c_p(w))$, one for each word $w \in D_i$, where $c_p(w)$ is the number of occurrences of $w$ in $D_i$.
E.g.: (*hello*, 3)
+ **Reduce phase** : For each word $w$, gather all the previous pairs $(w, c_p(w))$ and return the final pair $(w, c(w))$ where $c(w)$ is the number of occurrences of $w$ for all the Documents. In other words, $c(w)$ is equal to $\sum_{k=1}^n c_{p_k}(w)$

2. In this section we convert the documents into a usable DataFrame in order to figure out the countries that are most and less active in the research.

3. In NLP a common technique to perform analysis over a set of texts is to transform the
text to a set of vectors each one representing a word inside a document. At the end of
the pre-processing the document will be transformed into a list of vectors or a matrix of
$n \times m$ where $n$ is the number of words in the document and $m$ is the size of the vector
that represents the word $n$.

More information about word-embedding: https://towardsdatascience.com/introduction-to-word-embedding-and-word2vec-652d0c2060fa
What you can do is to transform the title of the paper into its embedding version by using
the pre-trained model available on FastText page: https://fasttext.cc/docs/en/pretrained-vectors.html.
The pre-trained model that you have to download is the https://dl.fbaipublicfiles.com/fasttext/vectors-wiki/wiki.en.vec
Basically the pre-trained model is more or less a huge dictionary in the following format
$key : vector$.

To load the model follow this snippet of code which is slightly different from what you
can find at this page https://fasttext.cc/docs/en/english-vectors.html

In this task, we will: 


 - Load the data plucking only the metadata field of each paper, since it contains the title
 
 
 - load the english fasttext model
 
 
 - create one dictionary per paper, each one with its title and the embedding for it
 
 
 - save each dictionary in a .json file
 

### MAPD-B data management 

This assignment covers the following topics:

1. Redundancy
2. Cryptography
3. Object Storage Technology
4. REST APIs and Block Chain Technology

# Search Engine
This project is to build a search engine based on the crawled data. We remove stop words and stem the words to eliminate variations. We calculate tf-idf for each unique word. JSON is used to store the inverted index. We also optimze the database using prefix tree to reduce the search time. When a query is given, we get the top 10 results based on cosine similariy using tf-idf. Upon these results, we sort it again using Jaccard coefficient to get the best result.

![GUI](https://github.com/kalmanlukelin/CS-221-project3-search-engine/master/Figure/searchengine.png)

## Running the project
Use index.py to build database
```
python2 index.py path_of_database
```

Use run.py to show the result
```
python2 run.py path_of_database
```

## Result
Processed document numbers: 37485
Number of unique words: 506388
Toal size of index: 376 MB
Time for building inverted index: 2964.35 secs
Time for saving inverted index: 27.95 secs
Time for saving inverted index using prefix tree: 216.14 secs

The following is the search time for each query. The optimzed one is to search the database made by prefix tree.
| Input                   | Searching time                                         |
| ----------------------  | ------------------------------------------------------ |
| Informatics             | Non optimzied: 33 seconds. Optimized: less than 1 sec. |
| Mondego                 | Non optimzied: 32 seconds. Optimized: less than 1 sec. |
| Irvine                  | Non optimzied: 31 seconds. Optimized: less than 1 sec. |
| artificial intelligence | Non optimzied: 32 seconds. Optimized: less than 1 sec. |
| computer science        | Non optimzied: 32 seconds. Optimized: 1 sec.           |

## Built with
* bs4
* nltk
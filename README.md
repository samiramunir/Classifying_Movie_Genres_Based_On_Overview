# Multioutput Classifer for Movie Genre

![](/Media/pic.jpeg)


Objective: 

This project aims to build a  multi-target classifer that can predict a movie's multiple genres  based on it's overview text that was collected from the IMDB Moviedb database. The challenge was to  have a model that classifies a movie to be in multple genres. For example, the movie Avatar falls into the following categories according to IMDB.  Action, Adventure, Fantasy, Sci-Fi. Not only is it a multiclassication problem, the classes are not mutually exclusive. 

Process: 

- Performed  TFIDF word vectorization of 5000 synopsis using NLTK from IMDB movie dataset  
- Tuned hyperparameters using gridsearchcv from scikit learn. Final model performed 105% better than random guessing, at  predicting multiple overlapping genres for each movie.




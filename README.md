# Multioutput Classifer for Movie Genre

![](/Media/pic.jpeg)


Objective:

Our overall objective was to classify text into multiple labels. To do this we searched for a dataset that would require this type of application. 

This project aims to build a  multi-target classifer that can predict a movie's multiple genres based on it's overview text that was collected from the The Moviedb database. The challenge was to have a model that classifies a movie to be in multple genres. 

![](/Media/Avatar.png)

As you can see according to IMDB, Avatar is not only Fantasy but its classified by Action, Adventure, and Fantasy. Not only is it a multiclassication problem, the classes are not mutually exclusive. S For our project we decided to train movies that fell in one or more of the following 11 genres:  

Action,  Adventure, Comedy, Crime, Drama, Fantasy, Horror, Mystery, Science Fiction, Thriller

We used a multioutput classifer that trains one classifier for each of the target genres. So the classifer actually trained on our train set 11 times with each time having one genre as the target. The output prediction for one movie would inclue a True or False prediction for each of the genres for each of the genres. 


Process: 

- Performed  TFIDF word vectorization of 5000 synopsis using NLTK from IMDB movie dataset  
- Tuned hyperparameters using gridsearchcv from scikit learn. 
- The fina model was SVC using multioutput classifer from skLearn. 


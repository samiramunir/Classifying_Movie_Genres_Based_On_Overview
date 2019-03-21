# Multi-Label Classifer for Movie Genre

![](/Media/pic.jpeg)


## Motivation:
As businesses continue to amass data and documents, new avenues of exploring those data/documents keep arising. Text classification is very useful machine learning tool that allows for analyzing large volumes of documents and group them into different categories. One of the challenges associated with text classification is to attach multiple labels to the same document. For example, take movie generes into consideration. A movie can fall into multiple genres. Take Avatar for instance. 

![](/Media/Avatar.png)

The above picture shows that according to IMDB, Avatar is not only Fantasy but its classified by Action, Adventure, and Fantasy. Moreover, the classes are not mutually exclusive. So there is no hard drawn line between each classification. This project aims to build a multi-label classifer that can predict a movie's multiple genre labels based on it's overview text that was collected from the The Moviedb database. 

The model is trained on movies that fall in one or more of the following 11 genres:  

Action,  Adventure, Comedy, Crime, Drama, Fantasy, Horror, Mystery, Science Fiction, Thriller

We used a multioutput classifer that trains one classifier for each of the target genres. So the classifer actually trained on our train set 11 times with each time having one genre as the target. The output prediction for one movie would inclue a True or False prediction for each of the genres for each of the genres. 


## Data Set EDA:
  
The initial exploration revealed that there were certain words like Life, Fine that are common in all genres. 

Word Cloud for All Movies Classified as Action
![](/Media/WCAction.png)

Word Cloud for all Movies Classified as Comedies
![](/Media/wcComedy.png.png)
 

![](/Media/pie1.png)

The following heatmap shows how correlated one genre is to another. As you can see comedy and thriller are the least correlated. Which is intuitive.  

![](/Media/heatmap.png)









## Best Model:
- Performed  TFIDF word vectorization of 5000 synopsis using NLTK from The MovieDb dataset  
- Tuned hyperparameters using gridsearchcv with multioutputclassifer running SVC model which gave us our best score on our test data at 0.19 which is better than the base case of .09. 

![](/Media/Gridsearch.png) 

Testing Results:

![](/Media/predictions.png)



## Going Forward: 

The model could be trained on more data. There are rooms for tryin other sklearn multiclass algorithms like multilabel classifer. The challenge with achieving a higher score lies in the fact that the model has to make 11 different predictions for each movie. As a result the probabilities of getting each 11 predictions right for each movie is low and acts against the over all test score. 
 

*****************************************************************
Project Partner [Mubarak Bajwa](https://github.com/Mubarakb)
*****************************************************************

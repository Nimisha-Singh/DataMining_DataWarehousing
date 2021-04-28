# Movie-Recommender-System

# INTRODUCTION 

1: A recommender system or a recommendation system, is a subclass of information filtering system that seeks to predict the “rating” or “preference”, a user would give  to an item. They are primarily used in commercial applications. \
2: Recommender systems are utilized in a variety of areas and are most commonly recognized as playlist generators for video and music services like Netflix, Youtube and Spotify, product recommenders for services such as Amazon, or content recommender for social media platforms as Facebook and Twitter.  These systems can operate using a single input, like music, or multiple inputs within and across platforms like news, books, and search queries. \
3: There are also popular recommender systems for specific topics like restaurants and online dating. 

# APPROACH USED

We used Content Based approach, our recommendation system will recommend other movies which are going to use are similar to the selected movie. \
f(movie) -> movie \
Advantages: \
The model doesn’t need any data about other users, since the recommendations are specific to this user. This makes it easier to scale to a large number of users. \
The model can capture the specific interests of a user, and can recommend niche items that very few other users are interested in. 

# SIMILARITY MEASURES
Cosine similarity is a metric used to determine how similar the documents are irrespective of the size.\
Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space.  In the context of recommendation system, the two vectors are the arrays containing the word counts of two documents. \
The Cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance because of the size, they could still have a smaller angle between them. \
“Smaller the angle, higher the similarity”. 



# IMPLEMENTATION

1 Preprocessing 

We started our project with the preprocessing of the dataset. Initially our dataset file (movie _metadata.csv) contains columns color,  director_name,  num_critics_for_review, duration and many more, there were a total 28 columns. 
We extracted the features which are required for our recommendation system. The features which we extracted were director_name, actor1_name, actor2_name, actor3_name, genres, movie_title and a combined attribute which we made by ourselves, it is a combination of all the previous attributes. 
The final data is stored in the final_dataset.csv file.

2  Model Making:
We designed the model for our recommendation system, we started with tokenizing the column  “combined” and made a collection of text documents and built a vocabulary of known words using the CountVectorizer function.
After that we learn the dictionary and store the document-term matrix in the final_cv variable.
Next, we calculate the cosine similarity among the text documents and store their value in the variable similarity. Lastly we made a function named rcmd in which we passed our input movie as the argument. Function returns the list of 12 movies which are most similar with our input movie. 
              
3 Hosting our system over a Local Server : 
We used flask, micro web framework written in python, to host our system over a local server.

3.1 What is Flask? 
Flask is a lightweight WSGI  Web application framework. This means flask provides you with tools, libraries and technologies that allow you to build a web application. This web application can be some web pages, a blog, a wiki or go as big as a web-based calendar application or a commercial website.
Flask is part of the categories of the micro-framework. Micro-framework are normally frameworks with little to no dependencies to external libraries. This has pros and cons. Pros would be that the framework is light, there is little dependency to update and watch for security bugs, cons is that some time you will have to do more work by yourself or increase yourself the list of dependencies by adding plugins.



https://nimisha-singh.github.io/Movie-Recommender-System/

https://github.com/souravarya07/Movie-Recommender-System

https://docs.google.com/document/d/1-Pw8RHJbcy6H4HQDcug7oojq_WZe_0f7AXxRA48n160/edit

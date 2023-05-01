![image](https://user-images.githubusercontent.com/111785493/229134087-8dffa779-894f-4431-a67a-fe90b27d4d4a.png)

# Goodreads User Recommendation System

*This repository holds an attempt to make a recommendation system using the user feedback dataset from the popular book review website GoodReads

Goodreads Kaggle link:
https://www.kaggle.com/datasets/b2dde9353c9d10c36e4d6b593a74c109dbaca6393a1ca0f2c7abafeba7633641/code?select=book1-100k.csv



## Overview
Goodreads is a popular website where many readers go to leave reviews and ratings on books they have read, users can search the database for books to view other users' ratings and reviews. The Goodreads dataset including the User ID, book name, and user feedback review, using a collaborative filtering system, a recommendation system can be made, recommending a user’s next read based off of other user’s reviews and books that they have read.


## Summary of Workdone

I started off with some data processing. The dataset contained some null values, there was a rating of 'This user doesn't have any rating'. Each of the rows that had this rating also had a Name of 'Rating'. I removed these datapoints since they would be of no use.

After Data processing, I did some visualization, and then cleaned the book titles to help with the effiency of the search engine created later.

The search engine was created by using a term frequency matrix, then using cosine similarity I found the other users that liked the same book that was searched for and based off of the most similar user's reads I recommended other books.

* Data:
    * Input: multiple CSV files with user data, 51945 rows x 3 columns
    * there are 362,596 User IDs

  * Size: 19.9 MB
  * Instances: UserID, Book Name, Review

#### Preprocessing / Clean up

* For the book names, some data processing was done to make a book title search engine. Special characters such as '/' and dashes was removed, extra spaces were removed and all the letters were made to be lowercase. 

#### Data Visualization

I made 2 bar graphs, 1 to see the distribution in the ratings and 1 to see which books had the highest ratings

### Problem Formulation

* Define:
  * In the files Draft1.ipynb and Draft2.ipynb, I tried different ways to create a collaborative filtering system.
  * Models
    *I attempted to use the Book datasets that comes with the goodreads dataset file to match the book titles in the User dataset to the book titles in the Book dataset to create a better and more expanded dataset. 

### Training
* I used cosine similarity to create a search engine
* To create a collaborative filtering recommendation system

### Conclusions

* Created a search engine to find the books in the datafile, since the titles can vary so much, this was necessary for the search engine and created unique IDs for each book title. Then finding other users who also read that book and finding books that those users read and comparing it to the whole population to give more efficient book recommendations. 

### Future Work

* To try making a search engine where, input book and quick output of book recommendations
* Utilizing the Book dataset that is included with the GoodReads data file, where I would connect the User dataset and Book dataset to give recommendation and then provide more information about the books recommended.

## How to reproduce results

* In this section, provide instructions at least one of the following:
   * Reproduce your results fully, including training.
   * Apply this package to other data. For example, how to use the model you trained.
   * Use this package to perform their own study.
* Also describe what resources to use for this package, if appropirate. For example, point them to Collab and TPUs.

### Overview of files in repository

*The Final.draft.ipynb is the final code for the recommendation system
* Draft 1.ipynb: this was my first attempt at doing something with this dataset
* Draft 2.ipynb: this is my current attempt at making a recommendation system
*visualization draft.ipynb is my first attempt on the visualization
* How I Combined The Separate Datasets.ipynb: This is how I combined the multiple separate datasets into one dataset



### Software Setup
* pandas
* numpyu
* matplotlib
* glob

### Data

* Goodreads dataset contains two types of datasets, 1 is the book dataset that contains information about approcimately 10,000,000 books, there is detailed information about the books such as publication year, author, ISBN, etc. and there is a Users dataset that contains information about the Users book reads and their ratings. To access the Goodreads dataset, it can be downloaded from the Kaggle link listed above, the dataset is said to be updated every 2 days. 
* Since the dataset is so large, both the Users datset and Book dataset is split into smaller datasets, I combined them into one file in the 'How I Combined The Separate Datasets.ipynb'.

### Training

* cosine similarity for the search engine

#### Performance Evaluation

* Entering the book title into the search engine, gives you the bookid, I used this to find any similar users that read the book, this is the 'similar_users' data. From that I found other books that they also liked that was rated a 4 or higher. Now I compared those books that were rated highly and divided it by everyone who read it and rated it highly as well. That is what the score value is in the last table. It is the ratio between how similar users liked the recommended books vs. how much the average user liked the book.This is because the higher the score the better the recommendation.

One of my favorite books is 'It Ends With Us', I used this to test my recommendation system. The output recommended books, really intrigued me. 


## Citations

* I used the youtube channel: Dataquest. This channel provided alot of videos that helped with understanding cosine similarity
* the kaggle link: https://www.kaggle.com/datasets/b2dde9353c9d10c36e4d6b593a74c109dbaca6393a1ca0f2c7abafeba7633641/code?select=book1-100k.csv








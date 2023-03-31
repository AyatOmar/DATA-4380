![image](https://user-images.githubusercontent.com/111785493/229134087-8dffa779-894f-4431-a67a-fe90b27d4d4a.png)

# Goodreads User Recommendation System

* **One Sentence Summary** Ex: This repository holds an attempt to make a recommendation system using the user feedback dataset from the popular book review website GoodReads

GoodReads Kaggle link:
https://www.kaggle.com/datasets/b2dde9353c9d10c36e4d6b593a74c109dbaca6393a1ca0f2c7abafeba7633641/code?select=book1-100k.csv



## Overview
Goodreads dataset including the User ID, book name, and user feedback review, using a collaborative filtering system, a recommendation system can be made. Recommending a user’s next read based off of other User’s reviews and book reads.


## Summary of Workdone

Starting off with some data processing, making a better and more efficient search engine. 

* Data:
  * Type: For example
    * Input: multiple CSV files with user data, 51945 rows x 3 columns
    * there are 362,596 User IDs

  * Size: 19.9 MB?
  * Instances (Train, Test, Validation Split): UserID, Book Name, Review

#### Preprocessing / Clean up

* For the book names, some data processing was done to make a book title search engine. Special characters such as / and dashes was removed, extra spaces were removed and all the letters were made to be lowercase. 

#### Data Visualization

Show a few visualization of the data and say a few words about what you see.

### Problem Formulation

* Define:
  * Input / Output
  * Models
    * Describe the different models you tried and why.
  * Loss, Optimizer, other Hyperparameters.

### Training
* I used cosine similarity to create a search engine
* I am trying to create a collaborative filtering recommendation system

### Performance Comparison

* Clearly define the key performance metric(s).
* Show/compare results in one table.
* Show one (or few) visualization(s) of results, for example ROC curves.

### Conclusions

* State any conclusions you can infer from your work. Example: LSTM work better than GRU.

### Future Work

* What would be the next thing that you would try.
* What are some other studies that can be done starting from here.

## How to reproduce results

* In this section, provide instructions at least one of the following:
   * Reproduce your results fully, including training.
   * Apply this package to other data. For example, how to use the model you trained.
   * Use this package to perform their own study.
* Also describe what resources to use for this package, if appropirate. For example, point them to Collab and TPUs.

### Overview of files in repository

* Draft 1.ipynb: this was my first attempt at doing something with this dataset
* Draft 2.ipynb: this is my current attempt at making a recommendation system
* How I Combined The Separate Datasets.ipynb: This is how I combined the multiple separate datasets into one dataset 

* Note that all of these notebooks should contain enough text for someone to understand what is happening.

### Software Setup
* pandas
* numpyu
* matplotlib
* glob

### Data

* Point to where they can download the data.
* Lead them through preprocessing steps, if necessary.

### Training

* Describe how to train the model

#### Performance Evaluation

* Describe how to run the performance evaluation.


## Citations

* Provide any references.








# Authors of This Project
This is a group project with 4 authors equally contributed.

-Yirong Bian (yb970@nyu.edu)

-Cindy Lin (cyl4981@nyu.edu)

-Hanyuan Zhang (hz1832@nyu.edu)

-Wanyi Yang (wy815@nyu.edu)

# Background
When mentioning anime, the first that comes to people’s mind is probably <em>Your Name</em> which became a hot topic in 2016, or <em>Spirited Away</em> which was directed by renowned Japanese director Hayao Miyazaki and won the Academy Award. Nonetheless, the history of anime can be traced back decades ago, and it has since been an important part of the entertainment industry. In this report, we aim to explore users' feedback on anime based on the features of the anime. As we explore the dataset with approaches ranging from hypothesis testing to machine learning, we bear the overarching question of what makes a good anime in mind. We try to analyze factors that could affect the quality of the anime and the users’ reactions. Moreover, we intend to build a prediction model that could potentially help businesses to project users’ feedback for the anime they produce. 


# 1 Data Preprocessing
This raw data set was obtained from [Kaggle] (https://www.kaggle.com/datasets/hernan4444/anime-recommendation-database-2020). We are using the anime.csv file, consisting of 35 columns and 17,562 rows. Each row represents information about an anime, meaning there are a total of 17,562 anime being counted, whereas each column represents a feature of the anime. We notice that NaN values are marked as “Unknown” in this data set and we apply a row-wise removal of the missing value and drop the unnecessary columns for each of the following tasks. We deal with the categorical variables, including genre, producer, rating, type, source, and studio by using one-hot encoding to convert them into dummy variables. It is worth noting that one anime may have more than one genre and producer. We transform the string type numeric data to numeric and extract the year of the feature Premiered as integers. In addition, we divide the anime into five groups and create a new categorical column: extra short anime (0 - 10), short anime (11 - 26), medium anime (27 - 50), long anime (> 50) based on the episodes feature, which will be useful in one of the questions in the inference chapter. In terms of extreme values, we decide not to remove any outliers because they are valid and consistent with reality.

# 2 Inference 
We aim to explore whether anime’ premiered year will have an impact on their scores and whether is there a different preference in anime genres. and whether viewers are more likely to complete anime with fewer episodes in length. The code is in '2 Inference (Cindy Lin and Wanyi Yang).ipynb'.

# 3 Prediction
We are trying to use different features to predict the score of different animes. We want to find out the most relevant features that can reveal the quality of animes. Also, we want to investigate how well they can predict the score as we increase the number of features taken as input. The code is in '3 Prediction (Hanyuan Zhang).ipynb'.

# 4 Classcification
We want to answer: Is it possible to know whether the anime is good or not based on reviewers' actions data such as the number of 'Watching', 'Dropped', etc? The code is in '4 Classification (Hanyuan Zhang).ipynb'.


# Conclusion
In this capstone project, we explore inference, prediction, and classification approaches to analyze the anime data set. We conclude that there are features that are highly correlated with the score and popularity of an anime. In the inference section, it is interesting to see that the quality of the anime does not improve significantly, as the anime industry and relevant technology develop while genre plays a major role in popularity. We suggest anime producers and investors take the different target audience populations segmented by genre into consideration. In the prediction section, we show that genre and episode length are two major factors that may influence the viewer’s enjoyment of anime, while producers and studios are the most important features of the anime quality. By implementing various machine learning models, we find ridge linear regression is the most suitable in this situation. And we are able to predict the quality of anime based on its production background. In the classification section, we find that the random forest has the largest accuracy score in differentiating good and bad quality anime based on the reactions. We also find that the most indicative metric of the anime's quality from the perspective of the users is the number of 'Members' and 'Favorites'.

# Environment Configuration
The environment configuration is in environment.yml file


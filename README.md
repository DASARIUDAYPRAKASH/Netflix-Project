# Capstone Project
## NETFLIX MOVIE RECOMNDATION SYSTEM

## Table Of Contents

1.	Problem Statement
2.	Project Objective
3.	Data Description
4.	Data Pre-processing steps and inspiration
5.	Choosing the algorithm for the project
6.	Motivation and reasons for choosing the algorithm
7.	Conclusion
 
## Problem Statement
Recommendation Engines are the much-needed manifestations of the desired Predictability of User Activity. Recommendation Engines move one step further and not only give information but put forth strategies to further increase users’ interaction with the platform.
In today’s world OTT platform and Streaming Services have taken up a big chunk in the Retail and Entertainment industry. Organizations like Netflix, Amazon etc. analyses User Activity Pattern’s and suggest products that better suit the user needs and choices.
For the purpose of this Project, we will be creating one such Recommendation Engine from the ground-up, where every single user, based on their area of interest and ratings, would be recommended a list of movies that are best suited for them.


## Project Objective

1. Find out the list of most popular and liked genre
2. Create Model that finds the best suited Movie for one user in every genre.
3. Find what Genre Movies have received the best and worst ratings based on User Rating. 

## Data Description

Feature Name	Description
ID	          Contains the separate keys for customer and movies.
Rating	      A section contains the user ratings for all the movies.
Genre	        Highlights the category of the movie.
Movie Name	  Name of the movie with respect to the movie id.

 
## Data Pre-processing steps and inspiration

**1. Loading the Dataset:** The initial step involves loading the dataset into the analysis environment, typically using libraries like Pandas in Python, ensuring accessibility for further examination.

**2. Checking for Data Types:** It is imperative to inspect the data types of each column to ensure consistency and appropriateness for subsequent analyses and operations.

**3. Creating Columns:** As the data available in Notepad .txt format and it is not having any header or column names we are providing them during the loading of the data. 

**4. Preprocessing Data:** Now after providing the column names such as Cust Id and Rating.  We have Nan values in the Rating Columns. And here we are considering those Nan Columns as Movie Id So based on this we can create another column named Movie Id.   

**5. Handling Outliers:** Since it is Contain Nominal Data and in the time of collecting the opinions or ratings of the movie there should be mandatory fields only. And the Rating Order also 1,2,3,4,5 and the Cust id is also type of distinct or categorical in nature because it is describing each individual customer behavior so there is no scope for Outliers.

## 6. Exploring and finding the Inferences from the Data: 
•	In order to exploring the Data, we are aggregating the Ratings and counting all the Rating’s.  which will show the distribution of the Rating count towards to the Ratings.

•	After that in order to count the movie number we consider the Nan values which are present in Rating Column. And summing up them and we got Number of Movies = 4499

•	And for finding the count of customer we subtract the movie Number from the Unique Customer Id’s. and we got Customers count as 470758

•	And for finding the count of Rating’s also we subtract the Number of movies from Unique Rating’s. and we got Rating count as 24053764

•	So, after all those steps we can plot the values on Bar Chart

Inferences from it 

**1.	The Rating 4 is Got Highest share of 34%**

**2.	The Rating 3 is Got Second Highest share of 29%**

**3.	After that The Rating 5 is Got 23%**


**4.	After that The Rating 2 is Got 10%**

**5.	After that The Rating 1 is Got 5%**
   !![image](https://github.com/DASARIUDAYPRAKASH/Netflix-Project/assets/130547847/edd2497c-4c4a-4ec3-ad46-941dc06c8b5c)


•	The dataset of movie ratings. When it finds missing ratings (represented by Nan values), it assigns each sequence of consecutive ratings a unique movie ID. The purpose is to organize the data for analysis, ensuring that each movie has a distinct identifier even if there are missing ratings in between. Finally, it prepares the data for further analysis or modeling by creating a new Data Frame with movie IDs Column assigned to each rating.

•	After creating the movie id column to the dataset. Now we found that the Movies has been rated minimum Times is 2538

•	we did for the same to customers that are minimum times of review is 64.

•	After last two steps we dropped those movies which is less often Rated. And we dropped the customers also who are Inactive or less often giving the ratings to the movies. 

•	And we got the Trimmed data set with shape of 15622656 X 3

•	After that we created Pivot Table which Has Movie Id as Column and Cust id as rows and the Rows Contains the ratings which are given to the movies.

•	we imported the Movie titles data which contains the name of the movies.

•	After that we join the movie title dataset with Movie Ratings Dataset.







•	And we took one customer id that is 712664 and found that to which movies he had given a rating of 5. And we can see them below
 ![image](https://github.com/DASARIUDAYPRAKASH/Netflix-Project/assets/130547847/5bc67859-9557-4a6d-9c9c-2de4db933cf1)












## Choosing the algorithm for the project
Using Singular Value Decomposition (SVD) for a movie recommendation system involves breaking down the user-movie rating matrix into simpler components, which helps in identifying hidden patterns or latent factors in the data. These latent factors can represent things like genre preferences or viewer tastes. SVD is particularly effective for recommendation systems because it allows us to make predictions about how users might rate unseen movies based on their past ratings and the ratings of similar users. Overall, SVD is a powerful technique for creating accurate and personalized movie recommendations by leveraging the underlying structure of the rating data.


 
## Motivation and reasons for choosing SVD
Efficient Dimensionality Reduction: SVD reduces the size of the user-item matrix, aiding scalability and computational efficiency.
Robust to Sparsity: SVD performs well even with sparse data, common in movie rating datasets where users rate only a fraction of available movies.
Interpretable Factors: SVD uncovers underlying patterns like user preferences or movie genres, making recommendations more intuitive.
Personalization: SVD offers personalized recommendations by identifying similar users or items based on latent factors, enhancing user engagement.
Scalability: SVD algorithms are computationally efficient, making them suitable for large-scale recommendation tasks.
Proven Effectiveness: Widely adopted by industry leaders like Netflix, SVD has demonstrated its effectiveness in generating high-quality recommendations across various domains, including movies.
 
## Conclusion
•	Based on the analysis conducted on the dataset, it can be concluded that the SVD model is the most suitable for Recommendation System.  And we included on top 30% Top Rated Movies only.
•	After applying the SVD algorithm we got our Evaluations like below
 
![image](https://github.com/DASARIUDAYPRAKASH/Netflix-Project/assets/130547847/b0798e9f-8253-46e5-952d-08508c4e859d)

•	Now We Predicted Top 10 Movies for the Customer having id of 712664.
 ![image](https://github.com/DASARIUDAYPRAKASH/Netflix-Project/assets/130547847/ede60b2b-7bb0-441d-bb67-685048e107e8)


# Thank You!

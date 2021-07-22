# Predicting-Astrological-Signs

## Project Description
Astrology is a pseudoscience that claims to divine information about human affairs and terrestrial events by studying the movements and relative positions of celestial objects. -Wikipedia

## Data Description
The dataset contains almost 60,000 user profiles from a popular dating website. Any personal information about the users has been removed.
59946 Rows, 31 features

## Data Cleaning
I read the csv data into a pandas dataframe to begin cleaning and exploring the data.

My plan for cleaning was to preserve as much original data as possible.

Continous variables - filled nulls and outliers with mean

Categorical variables - filled nulls with 'no answer' string

Contextuals features - removed nulls and combined text answers due to the orignal dataset having unstorted text answers

Special cases: the 'sign' and 'religion' features contained the user's sign/religion, but also how important their sign/religion is to them. I separted these variables into two separate features - one for the actual sign/religion, and another for the user's feelings about their sign/religion.
 
## EDA

![dist_of_age](https://user-images.githubusercontent.com/83669741/126005860-e404a94c-edca-436b-96eb-669d00c6993e.png)
![dist_of_sex](https://user-images.githubusercontent.com/83669741/126005862-615d1f89-9ec7-4f7b-a4a6-2db65e46379a.png)
![dist_of_sign_seriousness](https://user-images.githubusercontent.com/83669741/126005864-781457af-a07d-4a66-bd3d-f0c90ba22ec7.png)
![dist_of_signs](https://user-images.githubusercontent.com/83669741/126005866-4f49c019-7fdb-4c9c-a636-8ef98d834600.png)

 ## First Model
To start, I separated my categorical and contextual features and built the following models with only the categorical features:

Model, Accuracy:

Baseline (random) 8.33%

Logistic Regression 8.12%

Random Forest Classifier 8.35%

Gradient Boosting Classifier 8.50%

Gradient Boosting Classifier (With GridSearch Best Params) 8.92%


## NLP Model
Then I wanted to do the same approach of modeling only the contextual free-text questions to predict astrological signs.

Model, Accuracy:

Baseline (random) 8.33% 

Logistic Regression 8.63%

Random Forest Classifier 8.70%

Gradient Boosting Classifier 8.71%


## Comprehensive Model
Next, I wanted to combine my categorical and contextual features into one model.

Model, Accuracy:

Baseline (random) 8.33%

Random Forest Classifier 8.28%

Gradient Boosting Classifier 9.26%

## Further Studies
More parameter tweaking

More text pre-processing

Examine feature importances 

Use Topic Modeling to determine the topic of each essay question

Vector similarity analysis

Recommendation matching 

Analyze if people with the same sign or traditionally “compatible” signs match together


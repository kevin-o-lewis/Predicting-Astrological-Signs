# Predicting-Astrological-Signs

## Project Description
Astrology is a pseudoscience that claims to divine information about human affairs and terrestrial events by studying the movements and relative positions of celestial objects. -Wikipedia

## Data Description
The dataset contains almost 60,000 user profiles from a popular dating website. Any personal information about the users has been removed.
59946 Rows, 31 features

## Data Cleaning
Methodology: preserve as much original data as possible, including outliers and nulls values.

Continous variables - filled nulls and outliers with mean
Categorical variables - filled nulls with 'no answer' string
Contextuals features - removed nulls and combined text answers due to the orignal dataset having unstorted text answers
Special cases: the 'sign' and 'religion' features contained the user's sign/religion, but also how important their sign/religion is to them. I separted these variables into two separate features - one for the actual sign/religion, and another for the user's feelings about their sign/religion.
 
## EDA


 
 ## First Model
 simple logistic regression using the following columns:
'age', 'status', 'sex', 'orientation', 'body_type', 'diet', 'drinks',
       'drugs', 'education', 'height', 'job', 'offspring', 'pets', 'smokes', 'religion_actual', 'religion_seriousness'
 8.2 % of predictions were correct on the test set
 this is slightly worse than randomly choosing one of the 12 classes, which would give you 8.3 % correct predictions


when I changed my target variable to sign_seriousness (how seriously a user takes their sign), I reached 51.1% correct predictions, with four classes ('and it matters a lot', 'and its fun to think about', 'but it doesnt matter', 'no_answer')

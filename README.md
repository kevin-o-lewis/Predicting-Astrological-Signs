# Predicting-Astrological-Signs

## Project Description
What is astrology
Why I chose this topic

## Data Description
59946 Rows, 31 features

## Data Cleaning
Methodology: preserve as much original data as possible, including outliers and nulls values.

 0   age          59946 non-null  int64 \  
 1   status       59946 non-null  object \
 2   sex          59946 non-null  object \
 3   orientation  59946 non-null  object \
 4   body_type    54650 non-null  object \
 - filled nulls with "no answer"
 
 5   diet         35551 non-null  object
 - filled nulls with "no answer"
 
 6   drinks       56961 non-null  object
 - filled nulls with "no answer"
 
 7   drugs        45866 non-null  object
 - filled nulls with "no answer"
 
 8   education    53318 non-null  object
 - filled nulls with "no answer"
 
 9   ethnicity    54266 non-null  object 
 
 
 10  height       59943 non-null  float64
 - filled nulls with mean (68)
 - replaced outliers (defined as singular occurances) with mean (68)
 
 11  income       59946 non-null  int64
 - 48442 nulls entered as -1
 - nulls account for ~80% of column data
 - Removed column
 
 12  job          51748 non-null  object
 - filled nulls with "no answer"
 
 13  last_online  59946 non-null  object
 - skip for now
 
 14  location     59946 non-null  object
 - skip for now
 
 15  offspring    24385 non-null  object
 - filled nulls with "no answer"
 
 16  pets         40025 non-null  object
 - filled nulls with "no answer"
 
 17  religion     39720 non-null  object
 - filled nulls with "no answer"
 - split into two columns, one for religion, one for how serious they take it. 
 - example: {religion:'catholicism but not too serious about it'} becomes {religion_actual: 'catholicism', religion_seriousness: 'but not too serious about it'}
 
 18  sign         48890 non-null  object
 - removed entire row if sign == null (due to sign beinmg target)
 - handled same as religion, split into two columns. 'sign_actual' will be target
 
 19  smokes       54434 non-null  object
 - filled nulls with "no answer"
 
 20  speaks       59896 non-null  object 
 21  essay0       54458 non-null  object 
 22  essay1       52374 non-null  object 
 23  essay2       50308 non-null  object 
 24  essay3       48470 non-null  object 
 25  essay4       49409 non-null  object 
 26  essay5       49096 non-null  object 
 27  essay6       46175 non-null  object 
 28  essay7       47495 non-null  object 
 29  essay8       40721 non-null  object 
 30  essay9       47343 non-null  object 
 
 ## First Model
 simple logistic regression using the following columns:
 'age', 'status', 'sex', 'orientation', 'body_type', 'diet', 'drinks',
       'drugs', 'education', 'job', 'offspring', 'pets', 'smokes',
       'religion_actual', 'religion_seriousness'
 8.2 % of predictions were correct on the test set
 this is slightly worse than randomly choosing one of the 12 classes, which would give you 8.3 % correct predictions

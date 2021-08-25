# Contents

This folder contains: 
1. Monthly Twitter-based indicators of unemployment in `./indicator/`
2. Programs necessary to produce them in `./code/`

# Monthly twitter-based indicators

Indicators are available for three countries: Brazil (`BR`), Mexico (`MX`), and United States (`US`):
- `./indicator/twitter_country.csv` contains Twitter indicators at the country-level. 
- `./indicator/twitter_city.csv` contains Twitter indicators at the top five cities for each country sorted by the total number of Twitter users. 

Each file contains the following variables: 
- `n_users_total` is the total number of twitter users observed each month.
- Various types of Twitter indices named `(1)_(2)_(3)`
- `(1)` stands for the five different labels related to the user's unemployment status.
- `(2)` stands for the classification model used to count the Twitter labels. We consider three approaches: 
  - `keywords` uses a keyword-based model
  - `bert05` uses a BERT-based model with a threshold probability of 0.5
  - `bert09` uses a BERT-based model with a threshold probability of 0.9
- `(3)` stands for different sample splits of the Twitter users.
  - `total` uses the total sample of all Twitter users
  - `gender_male` uses Twitter users whose gender is classified as male
  - `gender_female` uses Twitter users whose gender is classified as female

# Capstone: Formation Finder

#### By Ryan Scribner

## Problem Statement

I want to build a multiclass classification model (Decision Tree, KNN) that will input a geologic type log and be able to pick the desired geologic formation tops and return the values to the user.

## Data

The Formation Finder data used in this project was obtained from TD Geosteering. The data is maintained as LAS files and names of clients and formations were not provided to protect their privacy/investments. It includes scientific data collected for drilling purposes such as gamma ray, density porosity, resistivity.  See data dictionary below!

| Feature       | Type    | Dataset   | Description        |
|---------------|---------|-----------|--------------------|
| DEPT          | float64 | Log_1_TC  | Depth in feet (')  |
| DPHI          | float64 | Log_1_TC  | Density Porosity   |
| GR            | float64 | Log_1_TC  | Gamma Ray          | 
| ILD           | float64 | Log_1_TC  | Resistivity        | 
| FORMATION     | int64   | Log_1_TC  | Formation number   | 


## Modeling

The dataset was analyzed with two different purposes:
1. Identifying formation tops on an uploaded type log through supervised learning.
2. Accurately separate or highlight potential areas of interest using density porosity and resistivity readings!

I tried to use k-means to build an unsupervised model, but it was unable to cluster and classify the geologic data effectively. So, I used my domain knowledge to turn it into a supervised learning model instead. I went through and picked each geologic top and gave them a numeric value so the model could train itself effectively.

### Model 1

#### KNN

- Training accuracy score: 0.98
- Testing accuracy score: 0.98

### Model 2

#### Random Forest Classifier

- Training accuracy score: 1.0
- Testing accuracy score: 1.0

## Findings and Conclusion

The purpose of this project is to predict geologic formations through modeling. Data was cleaned and null values removed.  Three variables were selected based on their importance to the potential clientele, Gamma Ray, Density Porosity and Resistivity.  I tried to use k-means to build an unsupervised model, but it was unable to cluster and classify the geologic data effectively.  So, I used my domain knowledge to turn it into a supervised learning model instead.  I went through and picked each geologic top and gave them a numeric value so the model could train itself effectively.  Modeling commenced with KNN and Random Forest Classifier. Random Forest Classifier was chosen as the production model because of its near perfect results on the test data.

All models performed with a high level of accuracy and minimized false positives and negatives. Random Forest Classifier was chosen as the production model due to its near perfect classification of the data set.

## Next Steps
 
- Add more areas of interest (different oil/fields around the country)
- Better technical analysis (able to graph cross over between density porosity and neutron porosity)

## Works Cited

https://en.wikipedia.org/wiki/Gamma_ray_logging
https://en.wikipedia.org/wiki/Porosity
https://en.wikipedia.org/wiki/Resistivity_logging

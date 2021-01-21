I want to build a multiclass classification model (Decision Tree, KNN) that will input a geologic type log and be able to pick the desired geologic formation tops and return the values to the user.

The purpose of this project is to predict geologic formations through modeling. Data was cleaned and null values removed.  Three variables were selected based on their importance to the potential clientele, Gamma Ray, Density Porosity and Resistivity.  I tried to use k-means to build an unsupervised model, but it was unable to cluster and classify the geologic data effectively.  So, I used my domain knowledge to turn it into a supervised learning model instead.  I went through and picked each geologic top and gave them a numeric value so the model could train itself effectively.  Modeling commenced with KNN and Random Forest Classifier. Random Forest Classifier was chosen as the production model because of its near perfect results on the test data.

All models performed with a high level of accuracy and minimized false positives and negatives. Random Forest Classifier was chosen as the production model due to its near perfect classification of the data set.

| Feature       | Type    | Dataset   | Description        |
|---------------|---------|-----------|--------------------|
| DEPT          | float64 | Log_1_TC  | Depth in feet (')  |
| DPHI          | float64 | Log_1_TC  | Density Porosity   |
| GR            | float64 | Log_1_TC  | Gamma Ray          | 
| ILD           | float64 | Log_1_TC  | Resistivity        | 
| FORMATION     | int64   | Log_1_TC  | Formation number   | 
# KNN Algorithm for Glass Type Classification
## Context
This is a Glass Identification Data Set from UCI. It contains 10 attributes including id. The
response is glass type(discrete 7 values)
## Content
### Attribute İnformation:
1. Id number: 1 to 214 (removed from CSV file)
2. RI: refractive index
3. Na: Sodium (unit measurement: weight percent in corresponding oxide, as are attributes 4-10)
4. Mg: Magnesium
5. Al: Aluminum
6. Si: Silicon
7. K: Potassium
8. Ca: Calcium
9. Ba: Barium
 10. Fe: Iron
 11. Type of glass: (class attribute):
  - 1 buildingwindowsfloatprocessed
  - 2 buildingwindowsnonfloatprocessed
  - 3 vehiclewindowsfloatprocessed
  - 4 vehiclewindowsnonfloatprocessed (none in this database)
  - 5 containers
  - 6 tableware
  - 7 headlamps

There is no missing value in this dataset. These situation were checked in the code file.
Dataset Source : https://www.kaggle.com/uciml/glass
## Using KNN Algorithm
Firstly, the dataset is loaded and its target feature is assigned to variable y. Then the dataset is splitted at the rate we set as a train and test set. Dataset
is scaled with feature scaling before training the data. There are 7 different types of glass, so the Knn algorithm is run based on 7 neighbors. The data are classified according to their proximity to these centers that are determined automatically. After getting the accuracy result, the best parameter selection is made. The reason for this is to increase the accuracy value. In the last step, the system is restarted with the parameters selected for the most accurate result.

## Interpretation of the Result
For the KNN algorithm; Although we have 7 glass types, the selection of 6 neighbors has increased success. I think the reason of this situation is glass type 4 is not exist in dataset.

## References
- https://www.kaggle.com/juxwzera/decision-tree-and-knn
- https://seaborn.pydata.org/generated/seaborn.distplot.html (seaborn library is used for visualising data)
- Some lecture codes from Introduction to Machine Learning course by Berna KIRAZ

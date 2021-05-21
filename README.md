# 10-fold cross-validation accuracy using NB Classifier

Libraries used:

| Library | Function | Usage |
|---------|----------|-------|
|Pandas|	read_csv|	to read the dataset|
|NumPy|	Mean|	to calculate mean|
|sklearn.preprocessing|	Imputer|	to handle missing values|
|sklearn.preprocessing|	LabelEncoder, OneHotEncoder|	For encoding ordinal variables|
|sklearn.naive_bayes|	GaussianNB|	to fit Naïve Bayes model|
|sklearn.model_selection|	train_test_split|	to partition the dataset| 
|sklearn.model_selection|	cross_val_score|	for cross validation|
|Sklearn|	Metrics|	to find accuracy|

## Dataset 1- Dermatology

This dataset contains 34 attributes, 33 of which are linear valued and one of them is nominal. 12 attributes are Clinical whereas the rest are Histopathological. The class has 6 possibilities.
Number of Instances: 366
Number of Attributes: 34

Result
-
|Iterations|	Accuracy|
|----------|----------|
|1|	0.8275862068965517|
|2| 0.8148148148148148|
|3|	0.8888888888888888|
|4|	0.8461538461538461|
|5|	0.88|
|6|	0.875|
|7|	0.9130434782608695|
|8|	0.9565217391304348|
|9|	0.8695652173913043|
|10|	0.9130434782608695|

Mean Accuracy- 0.878461766979758
-
Interpretation
-
Looking at the above Mean accuracy, we can say that Naïve bayes model is well suited for the taken dataset. 

## Dataset 2- Car Evaluation

The dataset contains 6 ordinal variables: Buying, Maintenance, Doors, Persons, Luggageboot and Safety. The class contains 4 possible values.
Number of Instances: 1728 (instances completely cover the attribute space)
Number of Attributes: 6


Class Distribution (number of instances per class)
  
 |class|N|N[%]|
 |--------|--------|---------|
 |unacc |   	1210 |   70.023 % |
 |acc   |     	384 |  22.222 % |
 |good  |     	69 |  3.993 % |
 |v-good|     	65  | 3.762 %|

Pre-processing Task-

As the door attribute of the taken dataset has no correlation with the class label that’s why we are not taking the door attribute and similar reason for excluding the safety attribute. 

Result-
-
Confusion Matrix-
|  |  |  | |
|--|--|--|--|
|37|26|30|23|
|0|21|	0|	3|
|42|107|184|29|
|0	|0	|0	|17|

10-fold cross validation using NB

|Iteration|	Accuracy|
|---------|---------|
|1	|0.45901639344262296|
|2	|0.48360655737704916|
|3	|0.4426229508196721|
|4	|0.5573770491803278|
|5	|0.5|
|6	|0.512396694214876|
|7	|0.6033057851239669|
|8	|0.5454545454545454|
|9	|0.4576271186440678|
|10|	0.4830508474576271|

Mean Accuracy-	 0.5044457941714755
-
Interpretation-
-
Considering the above 10-fold cross validation results Naïve Bayes is not the appropriate model for the given dataset.

## Dataset 3: Tic Tac Toe
The dataset contains 9 nominal variables, each variable indicating the value at one of the 9 locations. The values are O, X or blank. The class has two possible values namely Positive and Negative.
Number of Instances: 958
Number of Attributes: 9

Class Distribution (number of instances per class)

|class|N|N[%]|
|------|-----|-----|
|positive|	626|	65.3445|
|negative|	332|	34.6555|

Results-
-
Confusion Matrix:
|  |  |
|--|--|
|23|77|
|3|185|

10-fold cross validation using NB

|Iteration|	Accuracy|
|--------|---------|
|1	|0.6911764705882353|
|2	|0.7205882352941176|
|3	|0.7313432835820896|
|4	|0.6567164179104478|
|5	|0.746268656716418|
|6	|0.7014925373134329|
|7	|0.7014925373134329|
|8	|0.7611940298507462|
|9	|0.7424242424242424|
|10|	0.6212121212121212|

Mean Accuracy-	 0.7073908532205284
-
Interpretation-
-
Considering the above 10-fold cross validation results, Naïve Bayes is moderately suited for the  given dataset. One possible explanation for the low accuracy could be uneven class distribution as the percentage of positive class is much more than the negative class.

## Dataset 4: Breast Cancer

The dataset contains 10 features namely Code_Number,Clump_Thickness, Uniformity_of_cell_size, Uniformity_of_cell_shape, Marginal_Adhesion, Single_Epithelial_Cell_Size, Bare_Nuclei, Bland_Chromatin, Normal_Nucleoli and Mitoses. Each feature has 10 possible values, from 1 to 10.
Number of Instances: 682
Number of Attributes: 10

Class Distribution (number of instances per class)

|class      	|N|          	N[%]|
|-|-|-|
|2 (benign)|	444	|65.0073|
|4 (malignant)|	239	|34.9927|

Results-
-
Confusion Matrix:
| | |
|-|-|
|129|	2|
|24|	50|

10-fold cross validation using NB

|Iteration|	Accuracy|
|--------|----------|
|1	|0.8367346938775511|
|2	||0.7959183673469388|
|3	|0.8775510204081632|
|4	|0.8333333333333334|
|5	|0.875|
|6	|0.9148936170212766|
|7	|0.851063829787234|
|8|	0.7021276595744681|
|9|	0.8085106382978723|
|10|	0.851063829787234|

Mean Accuracy-	 0.8346196989434072
-
Interpretation
-
Considering the above 10-fold cross validation results Naïve Bayes is well suited for the dataset taken for evaluation.

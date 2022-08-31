# Company-Bankruptcy-Prediction
## Description:

Prediction of bankruptcy is a phenomenon of increasing interest to firms who stand to lose money because on unpaid debts. Since computers can store huge dataset pertaining to bankruptcy making accurate predictions from them before hand is becoming important.
The data were collected from the Taiwan Economic Journal for the years 1999 to 2009. Company bankruptcy was defined based on the business regulations of the Taiwan Stock Exchange.
In this project, we have used various classification algorithms like Logistic Regression, KNN and Naive Bayes (Gaussian) Classifier and their accuracy metrics have been plotted simultaneously.

## Execution:


### Data cleaning:

For the First step, the data is imported from a csv file and converted to a panda’s DataFrame. Pandas is inbuilt library in python that is used in handling and manipulating Dataframes. Dataframe is basically collection of Rows and Columns. 
Once the data is clean, we check for the statistics of the cleaned data. The statistics of the data tells us the mean, median and the distribution of the data and some more info. Also, we checked for any null values and duplicate values in the whole dataset and for our surprise, we didn’t find neither any null nor duplicate values.
After the data is cleaned, Visualizations can be done on the data and inferences can be noted. 

### Visualizations:

One such visualization is to find the correlation between the variables. Plotting the correlation between variables is not visually appealing as there are 65 different variables. But we see some red squared in between that says they are highly correlated. 
As the target variable is categorical i.e., Bankrupt or not, plotting this variable we find out that around 97% of the data present is of financially stable and the rest is financially unstable.
Similarly, we can plot the Boxplot of Correlations between the variables and also feature distributions for close to bankruptcy companies.
After all this, we remove the outliers. Outlier is a data point that is present very far away from the mean of the distribution of the data. There is a set procedure to remove the outliers. And once the outliers are scaped of, The Boxplot distribution is plotted once again to find out that most of the outliers are removed.
Then, we perform a Log (Logarithmic) transformation on the data, the log transformation is performed in the data to remove any skewness present in the data and produce an approximate log-normal distribution. After the log transformation has been performed, we see a approximation of normal distributions in our dataset.

### Data modelling:

Coming to the second part, which is Data Modelling in which we try out different Supervised Machine Learning Classification algorithms fits the best to our dataset and gives us the best accuracy scores like precision, Recall, AOC-ROC curve, Accuracy and so on
Starting with a primitive Logistic Regression, Logistic regression is a statistical model that in its basic form uses a logistic Function to model a binary dependent variable, although many more complex extensions exist. After we apply Logistic regression to our model, the AOC-ROC score of 0.84
K nearest neighbors classifier is a non-parametric supervised learning algorithm first developed by Evelyn Fix and Joseph Hodges in 1951.  
It works by finding the distance between a query and all the examples in the data. For classification problems, a class label is assigned on the basis of a majority vote—i.e. the label that is most frequently represented around a given data point is used.
To which example the query is closest to is calculated using different metrics such as Euclidean distance, Manhattan distance, Minkowski distance and other metrics.
Providing an overall accuracy of 0.897, f1-score of 0.40 and finally AOC-ROC score of 0.625

Naive Bayes classification is an algorithm that is based on the Bayes’ Theorem. It is not a single algorithm but a family of algorithms where all of them share a common principle.
Naïve Bayes Classifier is one of the simple and most effective Classification algorithms which helps in building the fast machine learning models that can make quick predictions.
It is a probabilistic classifier, which means it predicts on the basis of the probability of an object. Naive Bayes classifier is also used for text classification algorithm.Naive Bayes classifier is also used for text classification algorithms. Coming to its accuracy scores, overall accuracy score of 0.66, and a f1-score of 0.16 and AOC score of 0.76

### Conclusion: 

Concluding, according to the f1-scores and the Accuracy metrics, KNN is the best metric to choose for further predictions. According to AOC-ROC, Logistic Regression stands first with a score of 0.84 Nevertheless, in this case, the best decision is to use Logistic regression because it can better recognize the minority class even misclassifying some not close to bankruptcy companies as close to bankruptcy.Also, the parameters that contribute to bankruptcy of a company are also external such as decisions taken by the CEO of the company and dwindling workforce and so on, which can neither be calculated nor predicted.

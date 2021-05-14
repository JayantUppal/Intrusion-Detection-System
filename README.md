# Intrusion Detection System

Due to the advancement in technology and digitization of information, there has been an increase in network data traffic. This also brings in the scope of increased network attacks and poses a threat to computer systems and data. The vulnerabilities in network security seem to increase in direct proportion with the use of the internet. Intrusion Detection Systems prove to be an effective method to detect unauthorized access and attacks in a network and safeguard it from intruders. In this project, we use the [KDD dataset](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html) to develop an intrusion detection system using machine learning algorithms and ensemble techniques. The dataset is first preprocessed to obtain clean and non-redundant data which is then tested against an ensemble model involving three classifiers namely Gaussian Naive Bayes, Decision Tree, and XGBoost.

The goal is to build an IDS to classify attacks as malicious or normal connections. Here is the entire implementation in four steps:- 
- Load the dataset and apply pre-processing.
- Perform Exploratory Data Analysis on the dataset.
- Train and test following classifiers - Decision Tree, Gaussian Naive Bayes, XGBoost.
- Make predictions using ensemble techniques.

![Methodology](https://user-images.githubusercontent.com/47852407/118237126-901f1080-b4b4-11eb-8ddd-a00945caa5e8.png)

# Steps Involved

### Preprocessing
This step includes data integration, data reduction through feature and instance selections, data transformation by converting symbolic features to numeric and class to nominal), data cleaning to remove outlier and extreme values. Also, the dataset had all types of forms: continuous, discrete, and symbolic with varied
ranges and resolutions, most of which cannot be processed by a pattern classification method, hence preprocessing of data was necessary before we could build a classification model.

### Exploratory data analysis (EDA)
EDA involves visualizing a dataset to summarize the main characteristics using statistical graphics and other data visualization methods. This provides a deeper understanding of the dataset to extract impartial experiments.

### Building Classifiers
  #### Decision Tree
  A decision tree is very much popular as a single classifier because   of its simplicity and easier implementation. It is a classification model that uses a  tree-like structure to perform a decision and is commonly used in operation research and intrusion detection because it gives better performance compared to   other algorithms.

  #### Gaussian Naive Bayes
  Gaussian Naive Bayes is a variant of Naive Bayes that follows Gaussian normal distribution and supports continuous data. Naive Bayes is a group of supervised machine learning classification algorithms based on the Bayes theorem. It produces good results in the classification where there exist simpler relations.

  #### XGBoost
  eXtreme gradient boosting (XGBoost) is a boosting technique that is a part of the ensemble-based approach. A sequential decision tree is constructed, which is also called a sequential ensemble technique. This method provides a result that contains bias that is low and high invariance because the model has a better ability to fit the training data.

### Classification using ensemble techniques
Classification of the network traffic data as normal or malicious using Ensemble Learning is a method that combines multiple learners to solve the specific problems to improve the accuracy of classifiers. We will use the max voting method that is generally used for classification problems. In this technique, multiple models are used to make predictions for each data point. The predictions by each model are considered as a ‘vote’. The predictions which we get from the majority of the models are used as the final prediction.

# Results
The results show that an ensemble of Gaussian Naive Bayes + Decision Tree + XGBoost with proper preprocessing activities on KDD 1999 Cup Dataset will
produce enhanced and more efficient IDS performance with low false positives. Also, the results show that it is possible to have a single and powerful classifier as the XGBoost classifier gives almost equally efficient results as the ensemble model.

![Results](https://user-images.githubusercontent.com/47852407/118238271-ed679180-b4b5-11eb-893c-f818fdd33655.png)

# How to use

- Create a virtual environment
```
$ pip install virtualenv
$ virtualenv ids-env
$ source ids-env/bin/activate
```
- Clone this repository
```
$ git clone https://github.com/JayantUppal/Intrusion-Detection-System.git
$ cd Intrusion-Detection-System/
```
- Install necessary imports
```
$ pip install -r requirements.txt
```
- Download dataset from [here](http://kdd.ics.uci.edu/databases/kddcup99/kddcup.data_10_percent.gz). Keep it in the same folder
- Now, start jupyter notebook using:
```
$ jupyter notebook
```
- Select 'IDS.ipynb' and you're good to go!

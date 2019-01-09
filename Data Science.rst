Data Pipeline  
   * Load  
   * Clean (if needed) 
   * Basic Stats/EDA 
   * Normalize 
   * Query/ML task 
   * Optimize Parmeters (if relavant) 
   * Evalute 


types of Data:  
   * Time Series
   * Tablular Data
   * Map Data
   * Text Data
   * Image Data 

Tasks:  
    * Aggregate Statistics
    * Regression (least squares)
    * Classification (KNN, logistic regression)
    * Clustering (KMeans)
    * Dimension reduction (PCA)
        - rojection scatterplot for top two
        - color dots by class (if there are) or target value (of there is)
        - explained variance on ALL components
        -  bar graphs of weights of each of the top two components
    * Bayes rule (show probabilities) 
        - two or more Classes
        - you want probability of class (classification problem)
        - you build histogram of measured value for each class
        - use Bayes rule to go from P(X|Y) to P(Y|X)


Data Sources: 
    sklearn.datesets(iris, MNIST digits, Boston housing data)

    UCI ML Archive https://archive.ics.uci.edu/ml/datasets.html 
  
    Kaggle https://www.kaggle.com 
  
    Project Guttenberg https://www.gutenberg.org/
  
    NYC Open Data http://www.nyc.gov/html/data/about.html 

    Word Bank Data https://data.worldbank.org/

    Awesome-public-datasets https://github.com/awesomedata/awesome-public-datasets


Regression
   1.Load data
   2.Plot scatter and Linear
        ax.scatter()
        ax.plot()
   3.Find the Linear regression
        * Using numpy libarary linalg
        * Using the spcipy libarary
        * Using scikit learn(machine learning libarary)
            - import LinearRegression and 
            - Load data and create dataframe for it
            - set target and features
            - EVD
            - create LinearRegression object lm
            - train_test_split 
            - lm.fit()
            - lm.predict()
            - plt.scatter(actual, predict)
            - evaluate  metrics
                RMSE  np.sqrt(metrics.mean_squared_error())
                R squares
        

Classification:
    1.Load data
    2.set target and features
    3.split into train, test set
    4.select Classification Model (KNeighborsClassifier)
    5.fit and predict
    6.evaluate
        knn.score()
        metrics.accuracy_score()
        metrics.classification_report()


Cluster:
    1.Load data
    2.split into train, test set
    3.select Classification Model
    4. fit and predict
    5.evaluate
        knn.score()
        metrics.accuracy_score()
        metrics.f1_score()



Machine Learning

Algorithms Grouped by Learning Style
    1.Supervised Learning
        Example problems：
            classification 
            regression
        Example algorithms：
            Logistic Regression
            Back Propagation 
            Neural Network.
    2.Unsupervised Learning
        Example problems：
            clustering
            dimensionality reduction
            association rule learning
        Example algorithms: 
            Apriori algorithm 
            k-Means
    3.Semi-Supervised Learning
        Example problems :
            classification 
            regression

Algorithms Grouped By Similarity
    Regression
        Linear Regression
        Logistic Regression
        Support Vector Regression (SVR)
        Ordinary Least Squares Regression (OLSR)
    Instance-based Algorithms
        KnerghborsClassifier
    Cluster
        K-Means
        K-Medians
    Artificial Neural Network Algorithms
        Perceptron
        Back-Propagation
    Deep learning
        Convolutional Neural Network (CNN)
    Dimensionality Reduction Algorithms
        Principal Component Analysis (PCA)
    Decision Tree Algorithms
        Classification and Regression Tree (CART)
    Bayesian Algorithms
        Bayesian Network (BN)
        Naive Bayes



Subset Select
    

Model evaluation
    Regression
        - RMSE
        - MSE
        - R squares
        - Adjusted R squares
    Classification
        - Accuracy_score
        - classification_report
    Cluster
        -    
    Cross Validation




Linear Regression is used to establish a relationship between Dependent and Independent variables, 
which is useful in estimating the resultant dependent variable in case independent variable change.

Logistic Regression on the other hand is used to ascertain the probability of an event. 
And this event is captured in binary format, i.e. 0 or 1.


F1 Score: It is a harmonic mean of precision and recall given by-
F1 = 2*Precision*Recall/(Precision + Recall)

Accuracy: Percentage of total items classified correctly- (TP+TN)/(N+P)


Recall: Number of items correctly identified as positive out of total true positives- TP/(TP+FN)

Specificity: Number of items correctly identified as negative out of total negatives- TN/(TN+FP)

Precision: Number of items correctly identified as positive out of total items identified as positive- TP/(TP+FP)

Type I Error: Number of items wrongly identified as positive out of total true negatives- FP/(FP+TN)
Type II Error: Number of items wrongly identified as negative out of total true positives- FN/(FN+TP)



===============================
Dask
===============================

What is Dask?
Dask, a flexible parallel computing library for analytic computing. 
With Dask, you will be able to take the Python workflows you currently have and 
easily scale them up to large datasets on your workstation without the need to 
migrate to a distributed computing environment.

Why do we need Dask?
1) Python is now well established as a major platform for data analysis and data science. 
2) For many data scientists, the largest limitation of Python is that all data must 
    fit into the resident memory of the available workstation. 
3) Further, traditionally, Python has only been able to utilize one CPU.

When do we need Dask?
If you love Pandas and Numpy but were sometimes struggling with data that would not
 fit into RAM then Dask is definitely what you need. 


=========
PySpark
=========
Spark is a tool for doing parallel computation with large datasets and it integrates well with Python.

Spark lets you spread data and computations over clusters with multiple nodes (think of each node as a separate computer). 

Splitting up your data makes it easier to work with very large datasets because each node only works with a small amount of data.

It is a fact that parallel computation can make certain types of programming tasks much faster.

However, with greater computing power comes greater complexity.

Deciding whether or not Spark is the best solution for your problem takes some experience, but you can consider questions like:
    * Is my data too big to work with on a single machine?
    * Can my calculations be easily parallelized?


============================
Map Reduce with Mr. Job
============================

====================
Support vector machine
====================
In machine learning, support vector machines are supervised learning models with associated learning 
algorithms that analyze data used for classification and regression analysis.

The advantages of support vector machines are:
    Effective in high dimensional spaces.
    Still effective in cases where number of dimensions is greater than the number of samples.
    Uses a subset of training points in the decision function (called support vectors), so it is also memory efficient.
    Versatile: different Kernel functions can be specified for the decision function. Common kernels are provided, but it is also possible to specify custom kernels.

The disadvantages of support vector machines include:
    If the number of features is much greater than the number of samples, avoid over-fitting in choosing Kernel functions and regularization term is crucial.
    SVMs do not directly provide probability estimates, these are calculated using an expensive five-fold cross-validation (see Scores and probabilities, below).

==============
Deep Learning
==============

======================
Neural Network(Keras)
======================

    Neural networks account for interactions really well
    Deep learning uses especially powerful neural networks

Activation functions
    Applied to node inputs to produce node output

    than
    ReLU(Rectified Linear Activation)
        relu(x)  =  0 if x < 0
                    x if x > 10
    sigmoid

Loss function
    Aggregates errors in predictions from many data points into single number
    
    Measure of model’s predictive performance
        Total Squared Error
        Mean Squared Error 
    
    Lower loss function value means a better model

    Goal: Find the weights that give the lowest value for the loss function

Gradient descent
    - Imagine you are in a pitch dark field
    - want to find the lowest point
    - Feel the ground to see how it slopes
    - Take a small step downhill
    - Repeat until it is uphill in every direction
    - steps:
        - Start at random point
        - Until you are somewhere flat:
            - Find the slope
            - Take a step downhill 
    - if the slope is positive:
        - Going opposite the slope means moving to lower numbers 
        - Subtract the slope from the current value
        - Too big a step might lead us astray
    - Solution: learning rate
        - Update each weight by subtracting learning rate * slope


forward propagation 
    - Multiply-add process
    - Dot product
    - Forward propagation for one data point at a time 
    - Output is the prediction for that data point


Backpropagation
    - Backpropagation is a method used in artificial neural networks to calculate a gradient 
      that is needed in the calculation of the weights to be used in the network.
    - Allows gradient descent to update all weights in neural network (by getting gradients for all weights)
    - Comes from chain rule of calculus
    - Trying to estimate the slope of the loss function w.r.t each weight
    - Do forward propagation to calculate predictions and errors

Backpropagation process
    - Go back one layer at a time
    - Gradients for weight is product of:
        1. Node value feeding into that weight
        2. Slope of loss function w.r.t node it feeds into
        3. Slope of activation function at the node it feeds into
    - Need to also keep track of the slopes of the loss function w.r.t node values
    - Slope of node values are the sum of the slopes for all weights that come out of them

Recap:
    - Start at some random set of weights
    - Use forward propagation to make a prediction
    - Use backward propagation to calculate the slope of the loss function w.r.t each weight
    - Multiply that slope by the learning rate, and subtract from the current weights
    - Stochastic Keep going with that cycle until we get to a flat part


Stochastic gradient descent
    - It is common to calculate slopes on only a subset of the data (‘batch’)
    - Use a different batch of data to calculate the next update
    - Start over from the beginning once all data is used
    - Each time through the training data is called an *epoch*
    - When slopes are calculated on one batch at a time: stochastic gradient descent    

Workflow for optimizing model capacity
    - Start with a small network
    - Gradually increase capacity
    - Keep increasing capacity until validation score is no longer improving

============================
Dimension reduction (PCA)
============================
If your learning algorithm is too slow because the input dimension is too high, then using PCA to speed it 
up can be a reasonable choice. 
This is probably the most common application of PCA. 
Another common application of PCA is for data visualization.



make English for ecah topic  ()
review Multiple Choices

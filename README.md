# Creating-Customer-Segments
Unsupervised Learning Project [Udacity Machine Learning Nanodegree]

## Project Overview
### Project Description
Implement unsupervised learning techniques on product spending data collected for customers of a wholesale distributor in Lisbon, Portugal to identify customer segments hidden in the data.

### Project Procedure
- Explore the data
  - Analyze feature relevance
  - Visualize feature distributions
- Preprocess the data
  - Implement feature scaling
    - Natural logarithm
    - Box-Cox transformation
  - Detect and remove outliers 
- Use principal component analysis(PCA) to do feature transformation
- Reduce the dimensionality of the data from six to two
- Use clustering algorithm to identify customer segments
  - Gaussian Mixture Model(GMM)
  - K-Means
- Compare prediction to actual distributions

### Project Results
  - Gradient Boosting algorithm performed best in f-score and accuracy on the testing dataset
  - Improve model performance after tuning model using grid search
  
    | Metric | Unoptimized Model | Optimized Model |
    | :---:   | :-: | :-: |
    | Accuracy | 0.8630 | 0.8705 |
    | F-score | 0.7395 | 0.7513 |
    
  - Both accuracy score and f-score are slightly declined on the reduced data(top 5 important features) than the scores on the full data.     However, it decreases substantial training time. 
  
    | Metric | Final Model trained on full data |  Final Model trained on reduced data  |
    | :---:   | :-: | :-: |
    | Accuracy | 0.8705 | 0.8590 |
    | F-score | 0.7513 | 0.7252 |
    | Train time | 5.7013 | 54.9721|

## Getting Started
### Prerequisites
This project requires **Python 2.7** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

You will also need to have software installed to run and execute an [iPython Notebook](http://ipython.org/notebook.html)

If you do not have Python installed yet, it is highly recommended that you install the [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included. Make sure that you select the Python 2.7 installer and not the Python 3.x installer. 

### Run

In a terminal or command window, run one of the following commands:

```bash
ipython notebook customer_segments.ipynb
```  
or
```bash
jupyter notebook customer_segments.ipynb
```

This will open the iPython Notebook software and project file in your browser.

### Data

The customer segments data is included as a selection of 440 data points collected on data found from clients of a wholesale distributor in Lisbon, Portugal. More information can be found on the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wholesale+customers).

Note (m.u.) is shorthand for *monetary units*.

**Features**
1) `Fresh`: annual spending (m.u.) on fresh products (Continuous); 
2) `Milk`: annual spending (m.u.) on milk products (Continuous); 
3) `Grocery`: annual spending (m.u.) on grocery products (Continuous); 
4) `Frozen`: annual spending (m.u.) on frozen products (Continuous);
5) `Detergents_Paper`: annual spending (m.u.) on detergents and paper products (Continuous);
6) `Delicatessen`: annual spending (m.u.) on and delicatessen products (Continuous); 
7) `Channel`: {Hotel/Restaurant/Cafe - 1, Retail - 2} (Nominal)
8) `Region`: {Lisbon - 1, Oporto - 2, or Other - 3} (Nominal) 

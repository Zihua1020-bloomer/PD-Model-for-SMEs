# PD-Model-for-SMEs
Use the SMEs data to create a 3_year_model and a 1_year_model and do the comparison. 

# Data 
Data is unbalanced (5% default and 95% non-default). For each company, there are different records of different time points. Each time points have the different records of customers.

# Unique point
## Deal with unbalanced data. 
Rather than oversampling, I created 2 new datasets which are for one year PD model and 3 year PD model. 

For the One Year PD Model, I divided the data according to default and non-default first, then for each year, I extracted the same number of non-default with default. For each account, as long as they once defaulted at the beginning year, the data will not be used later

For the 3-Year PD Model, The observation period will last for 3 years from the starting records. As long as they once defaulted at one point in the period, then they are seen as the default. I created a new variable default_3 yr for this model. And similar to the one-year model to deal with unbalanced situations. 

## Use hierarchical clustering method to do feature selection
Inspired by the index of datasets are mainly from financial statements, I used hierarchical clustering to do feature selection.

## Customer segmentation with clustering
At last, I used the clustering method to draw the pictures of the customers. I found that there are mainly 5 categories of customers . 

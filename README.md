# Cryptocurrencies
---
_Cryptos analysis using unsupervised machine learning and Python_

## Overview
---
The purpose of this project was to analyze a dataset from many alternative cryptocurrencies to spot trends that make a firm or person want to invest in them. The problem with cryptos is that the most common ones, like bitcoin or ethereum, are becoming unaffordable for the common public. That being said, I will be using unsupervised machine learning to see if we can spot any trends that result in opportunities of these altcoins.

## Resources
---
* Datasets:
* [Crypto](crypto_data.csv)

##Technologies used:

* Python
* Jupyter notebook
* Sklearn, pandas, and hvplot libraries
* Unsupervised Machine Learning

## Results
---
First, I had to preprocess and transform the data so that unsupervised machine learning could work. This included dropping null values, using only tradaeble and mined cryptocurrencies, numerically encoding categorical columns using the pandas.get_dummies method, and scaling the data using the StandardScaler() method as well.
Moreover, I proceeded with the Principal Component Analysis (PCA) to reduce the 98 scaled columns I had, to only 3 principal components.

![image_name](https://github.com/pady7/Cryptocurrencies/blob/main/plots/PrincipalComponents.png)

## Elbow Curve

![image_name](https://github.com/pady7/Cryptocurrencies/blob/main/plots/ElbowCurve.png)

As it can be seen, the optimal result was 4 clusters. So, I then proceeded with the KMeans analysis to fit the pca dataframe and predict the clustering. The product was this clustered_df with a 'Class' column that showed the predictions to which group it belonged to.

![image_name](https://github.com/pady7/Cryptocurrencies/blob/main/plots/ClusterDf.png)

And last but not least, I came up with some visualizations to better understand the results.

![image_name](https://github.com/pady7/Cryptocurrencies/blob/main/plots/3d-plot.png)

This first one was a 3D scatter plot which located each clustered crypto in relation to the 3 principal components created on the PCA. As it is seen, there are 3 major groups and one outlier.

![image_name](https://github.com/pady7/Cryptocurrencies/blob/main/plots/coinsMinedScatterPlot.png)

## Summary
---
The job of unsupervised machine learning is to discover patterns or groups of data when there is no known output. That being said, this analysis was successful at grouping cryptocurrencies into 4 groups. If we were to create a crypto investment portfolio we would need to further analyze the clusters. Nevertheless, we have a good start point where we can see that the most profitable and known cryptos are somewhat in the 2 groups that have less supply and mined coins in comparison to others. These cryptos are Bitcoin and Ethereum. Nevertheless, we should keep up with the innovations of technology where new altcoins are being created with very interesting value propositions.



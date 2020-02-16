# Cryptocurrency Prediction

## Overview
Cryptocurrency is a relatively complex and vast field with many different currencies and countless metrics that can be difficult to digest without proper analysis aided by visualizations. There is an opportunity to pitch an investment in cryptocurrencies to an accounting firm which could be quite lucrative. It will be necessary to analyze crypto data with the aim of discovering trends that can be used when pitching the investment.

## Resources
Software:
- Pandas 1.0.0
- Sklearn 0.22.1
- Plotly 4.5.0
- Hvplot 0.5.2

Data Sources:
- iris_data.csv
- shopping_data.csv
- https://min-api.cryptocompare.com/data/all/coinlist

## Summary
The trends being searched for in the data are unknown so any sort of supervised learning model will not be effective. There are no known outputs. Because of this, two unsupervised algorithms were tested. Before diving into crypto data, both of these models were tested on sample datasets with less features and data entries. Both algorithms are forms of clustering which simply group data points together. The first technique explored was the K-means Algorithm which groups the data into 'K' number of clusters determined by the means of all the points in each cluster. The other algorithm is Hierarchical Clustering which starts by declaring each point as a cluster then iteratively joins similar clusters until a predetermined stopping point. Both of these algorithms have their own pros and cons; K-means works best when there is a sense of the number of clusters before hand, Hierarchical does not necessarily need any assumptions regarding the number of clusters. 

## Challenge Overview
The accounting firm is interested in offering a new cryptocurrencies investment portfolio for its customers. The task is to present a report of tradable currencies and how they can be grouped for classification in developing an investment product. 

## Challenge Summary
The data first needed to be transformed and scaled in order to be used by an unsupervised clustering algorithm. Due to the high degreee of features, PCA (Principal Component Analysis) was performed to identify the primary influences in variance of the data. From there, the K-Means Algorithm was deployed with 4 clusters (determined by an elbow curve) which classified the data entries into 4 groups. When visualized, there is a clear outlier (Bittorrent) with the other three clusters having relatively clear boundaries between them. However, when viewing the original features 'TotalCoinsMined' vs. 'TotalCoinSupply', the clustering does not provide any insights into the cryptocurrencies' trends. Because of this, either more features could be added or more data points to try and extract meaningful groupings. 
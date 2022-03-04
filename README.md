# Cryptocurrencies

## Overview of Project

Using unsupervised machine learning, our goal was to analyze a large dataset of cryptocurrencies and classify them into multiple groups.  We visualized the data with both 2D and 3D scatter plots, and finally produced a report that classified the cryptocurrencies according to their features.

## Resources

Data Source: [crypto_data.csv](https://github.com/ZeroDarkHardy/Cryptocurrencies/blob/main/resources/crypto_data.csv)<br/>
Software/Code Language(s): Python 3.7.11, Conda 4.11.0, Jupyter Notebook, Visual Studio Code 1.65.0

## Results

### Elbow Curve<br/>
Using K-Means with the Inertia Method, we identify the number of useful clusters before we start seeing diminishing returns:<br/>
![elbow_curve.png](https://github.com/ZeroDarkHardy/Cryptocurrencies/blob/main/images/elbow_curve.png)

Our elbow curve graph shows a sharp dropoff in significance after about 4 clusters, so that's how many we'll use in our K-Means model output.<br/>

### Plotting clusters in 3D Scatter<br/>
![scatter_3d.png](https://github.com/ZeroDarkHardy/Cryptocurrencies/blob/main/images/scatter_3d.png)<br/>
Using the PCA algorithm to reduce our dataset to 3 primary components allows us to visualize the class clusters in three dimensions. We can see that most of the cryptocurrencies are fairly tightly clustered in classes 0, 2 and 3, with BitTorrent showing as a bit of an outlier in class 1 (detailed pic below).<br/>
![outlier.png](https://github.com/ZeroDarkHardy/Cryptocurrencies/blob/main/images/outlier.png)

### Plotting clusters in 2D Scatter<br/>
![scatter_2d.png](https://github.com/ZeroDarkHardy/Cryptocurrencies/blob/main/images/scatter_2d.png)<br/>
When we visualize the four classes in two dimensions, plotted by Total Coin Supply vs. Total Coins Mined, we can confirm that BitTorrent is indeed an outlier.  We also see a bit of divergent behavior in TurtleCoin, in class 2 (detailed pic below).<br/>
![bittorrent_2d.png](https://github.com/ZeroDarkHardy/Cryptocurrencies/blob/main/images/bittorrent_2d.png)<br/>
![turtlecoin_2d.png](https://github.com/ZeroDarkHardy/Cryptocurrencies/blob/main/images/turtlecoing_2d.png)<br/>

### Aggregated Cryptocurrencies Table (Tradable)<br/>
![crypto_table.png](https://github.com/ZeroDarkHardy/Cryptocurrencies/blob/main/images/crypto_table.png)<br/>
A new table was generated, pairing the important features of each cryptocurrency with their corresponding class. The above screenshot shows the first 10 rows of the table.

## Summary

After cleaning and transforming the data, we've successfully classified 532 different cryptocurrencies into 4 groups based on similarity between features.  We've also identified a couple of obvious outliers.  Each group will need to be analyzed for metrics that our client will consider favorable (performance/volatility).
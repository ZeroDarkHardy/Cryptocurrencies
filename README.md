# Cryptocurrencies

## Overview of Project

Using unsupervised machine learning, our goal was to analyze a large dataset of cryptocurrencies and classify them into multiple groups.  We visualized the data with both 2D and 3D scatter plots, and finally produced a report that classified the cryptocurrencies according to their features.

## Resources

Data Source: [crypto_data.csv]()
Software/Code Language(s): 

## Results

### Elbow Curve<br/>
Using K-Means with the Inertia Method, we identify the number of useful clusters before we start seeing diminishing returns:<br/>
![elbow_curve.png]()

Our elbow curve graph shows a sharp dropoff in significance after about 4 clusters, so that's how many we'll use in our K-Means model output.<br/>

### Plotting clusters in 3D Scatter<br/>
![scatter_3d.png]<br/>
Using the PCA algorithm to reduce our dataset to 3 primary components allows us to visualize the class clusters in three dimensions. We can see that most of the cryptocurrencies are fairly tightly clustered in classes 0, 2 and 3, with BitTorrent showing as a bit of an outlier in class 1 (detailed pic below).<br/>
![outlier.png]()

### Plotting clusters in 2D Scatter<br/>
![scatter_2d.png]()<br/>
When we visualize the four classes in two dimensions, plotted by Total Coin Supply vs. Total Coins Mined, we can confirm that BitTorrent is indeed an outlier.  We also see a bit of divergent behavior in TurtleCoin, in class 2 (detailed pic below).<br/>
![bittorrent_2d.png]()<br/>
![turtlecoin_2d.png]()<br/>
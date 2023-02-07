# Crypto_Performance
A cluster analysis for cryptocurrencies by their performance in different time periods, namely 24hrs, 7days, 14days, 30days, 60days, 200days and 1year.  Standard Scaler function and Principal Component Aanalysis was used to further augment the features for a KMean cluster analysis.

The folllowing analysis was conducted:

* Import the Data (provided in the starter code)
* Prepare the Data (provided in the starter code)
* Find the Best Value for `k` Using the Original Data
* Cluster Cryptocurrencies with K-means Using the Original Data
* Optimize Clusters with Principal Component Analysis
* Find the Best Value for `k` Using the PCA Data
* Cluster the Cryptocurrencies with K-means Using the PCA Data
* Visualize and Compare the Results

### Analysis

#### Elbow Curve

In reviewing the data, it is evident that two currency have a different behaviour compared to the rest of the crypto currencies over the last longer period.

![Price Change % by coin_id](https://github.com/KSohi-max/Crypto_Performance/blob/main/Images/Price%20Change%20%25%20by%20coin_id.png)

Using standard scalar function, the features in the dataset were normialized for KMean cluster model.  Below is the Elbow Curve providing the optimium 'k' value to be used in the KMean model using scaled data.

![Elbowcurve using Scaled Data](https://github.com/KSohi-max/Crypto_Performance/blob/main/Images/elbowcurve_scaleddata.png)

Principal Component Analysis function was also used to reduce the number of features to n_components '3' for use in KMean cluster model. The following Elbow Curve was produced showing the optimum 'k' value based on PCA reduction.  The optimum 'k' value to be used in KMean model remains at 4.

![Elbowcurve using PCA Data](https://github.com/KSohi-max/Crypto_Performance/blob/main/Images/elbowcurve_scaleddata.png)

#### KMean Cluster Analaysis

KMean Cluster analysis was carried out using the two datasets, namely scaled data and pca reduced data.

![Crypto Clusters using Scaled Data](https://github.com/KSohi-max/Crypto_Performance/blob/main/Images/cryptoclusters_scaled.png)

![Crypto Clusters using PCA Data](https://github.com/KSohi-max/Crypto_Performance/blob/main/Images/cryptoclusters_pca.png)

#### Conclusion

Visually there is a change in the way crypto_pricechange_clusters are "arranged" in the plot.  The two outlier cryptocurrency are far more clearly identifiable (i.e. ethland and celsius-degree-token) although there is no change in the number of clusters itself. PCA seems to have captured majority of the original data but has isolated the outlier currencies compared to the more clustered currencies (in blue and red) which seem to behave in relative synchronicity. 

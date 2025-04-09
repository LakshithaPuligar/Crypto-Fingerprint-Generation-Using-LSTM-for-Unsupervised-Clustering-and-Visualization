# Crypto-Fingerprint-Generation-Using-LSTM-for-Unsupervised-Clustering-and-Visualization
An unsupervised learning model using LSTM networks to generate unique crypto fingerprints based on historical price data, visualized with t-SNE and clustered using KMeans for market analysis and insights.
Based on past pricing data, this research creates distinct "fingerprints" for cryptocurrencies using Long Short-Term Memory (LSTM) networks. After dimensionality reduction with t-SNE (t-distributed Stochastic Neighbor Embedding), these fingerprints are clustered using KMeans. As a result, an unsupervised model is created that can discover hidden patterns in the price movements of cryptocurrencies. This model may be useful for market analysis, portfolio optimization, or recognizing comparable cryptocurrencies based on past patterns.

Important Features

LSTM-based Encoder: Processes historical bitcoin price data using an LSTM neural network and encodes it into a compact latent form.

For visualization reasons, dimensionality reduction (t-SNE) is used to reduce the high-dimensional latent characteristics to two dimensions.

Clustering with KMeans: Use the KMeans clustering technique to group cryptocurrencies into clusters according to their LSTM-generated fingerprints.

Visualization: Following t-SNE reduction, an interactive scatter plot displays bitcoin data points and their groupings.



Dependencies include:

torch: For LSTM model implementation

seaborn: For data visualization

requests: For fetching cryptocurrency data

numpy: For data manipulation

pandas: For handling and storing data

matplotlib: For plotting results

sklearn: For data scaling, dimensionality reduction, and clustering

Working-:
Data Fetching: The CoinGecko API is used by the project to retrieve historical bitcoin price data. It provides a time series of the values of the top N cryptocurrencies during the previous seven days, retrieved by market capitalization.

Data Preprocessing: To standardize the values between 0 and 1, the price data is scaled using MinMaxScaler. This lessens the possibility of biases during model training brought on by scale disparities.

LSTM Encoder: The historical price data is encoded into latent features (fingerprints) using a specially designed LSTM-based neural network. The scaled price data is used to train the LSTM model, which gradually discovers patterns in the price sequence.
Dimensionality Reduction (t-SNE): The high-dimensional latent vectors are reduced to 2D using t-SNE after the LSTM creates latent representations for every coin. This facilitates the visualization of the connections among cryptocurrencies.

KMeans clustering: The cryptocurrencies are grouped according to their encoded properties using KMeans clustering. This makes it easier to find comparable coins that show comparable price trends over time.

Visualization: The 2D t-SNE reduced data is shown in a scatter plot as the last stage. A point that is colored according to its KMeans cluster represents each coin. This makes it simple to find cryptocurrency groups with comparable past price movements.

Outcomes-:
A 2D representation of cryptocurrencies arranged into clusters according to their price trends is the end result. Which cryptocurrencies have comparable price fluctuations can be inferred from the scatter plot produced by t-SNE. Additional market research or even automated portfolio management may benefit from these findings.

Novelty-:
In order to provide meaningful representations of cryptocurrencies, this study uses unsupervised learning techniques with LSTM, which is commonly used for sequential data modeling. Traditional machine learning algorithms frequently rely on labeled data.

Dimensionality Reduction and Clustering: This method combines t-SNE and KMeans to produce an understandable visual depiction of the relationships between cryptocurrencies based on their price histories, offering distinctive insights into market trends.

Possibility of Market Insights: Without requiring manually labeled data, this technology might be used to offer insights into a variety of financial markets and assist in determining the linkages between assets.


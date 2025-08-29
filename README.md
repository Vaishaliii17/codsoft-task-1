
AIM

The main objective of this notebook is to analyze the Iris dataset using clustering techniques. Specifically, it applies the KMeans clustering algorithm to group data points based on flower features (sepal and petal dimensions) and determine the optimal number of clusters using the elbow method.

DATA EXPLORATION AND PREPROCESSING

Imported Libraries:

pandas → for data loading and manipulation

numpy → for numerical operations

Steps:

Loaded the dataset:

df = pd.read_csv("iris data.csv")
df.head(10)


Encoded categorical labels (species) into numerical values using pd.factorize().

Checked dataset properties: .describe, .shape, .isna().sum() to understand summary statistics, dataset size, and missing values.

DATA VISUALIZATION

Imported Libraries:

matplotlib.pyplot → for plotting

seaborn → for advanced visualizations

mpl_toolkits.mplot3d → for 3D plotting

Steps:

Created 3D scatter plots of:

Petal length vs Petal width vs Species

Sepal length vs Sepal width vs Species

Plotted 2D scatterplots using Seaborn:

Sepal length vs Sepal width

Petal length vs Petal width

Added species as color categories (hue="species") to visualize clustering trends.

APPLYING ELBOW TECHNIQUE

Imported Libraries:

sklearn.cluster.KMeans

Steps:

Applied KMeans clustering with different values of k (number of clusters).

Plotted the Within-Cluster Sum of Squares (WCSS) for each k.

Used the elbow point in the curve to determine the optimal number of clusters.

APPLYING KMEANS ALGORITHM

Steps:

Chose the optimal number of clusters (based on the elbow method).

Applied KMeans to partition the dataset into clusters.

Visualized the clusters along with centroids using Matplotlib/Seaborn scatter plots.

Compared predicted clusters with actual species labels.

OVERALL CONCLUSION

The KMeans algorithm is effective in identifying natural groupings in the Iris dataset.

Petal dimensions (length & width) are the most discriminative features for clustering.

The elbow method validated the use of 3 clusters, aligning with the actual number of species.

# Dissimilarities-of-Movie-Descriptions
Web scraping data, performing cosine similarity, and then performing hierarchical clustering using max linkage

This project first gets titles and movie descriptions from IMDB and cleans the data of stop words. 
Then term frequencies are counted and cosine similarity is performed on all term frequency vectors. The resulting calculations are stored in a distance matrix.
This matrix then has hierarchical clustering with max linkage performed on it and a dendrogram is made from the results.

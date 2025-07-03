# Dissimilarities-of-Movie-Descriptions
Web scraping data, performing cosine similarity, and then performing hierarchical clustering using max linkage

This project first gets titles and movie descriptions from IMDB and cleans the data of stop words. 
Then term frequencies are counted and cosine similarity is performed on all term frequency vectors. The resulting calculations are stored in a distance matrix.
This matrix then has hierarchical clustering with max linkage performed on it and a dendrogram is made from the results.


  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Basic Description of Cosine Similarity\n",
    "\n",
    "Cosine similarity is, in simple terms, taking the angle between two vectors. In machine learning, cosine similarity can be used to measure how similar two documents are by counting how many times every word appears in a document; these word counts are then put into a vector (1 x n matrix). After two documents have their word counts put into a vector, compare the two documents by calculating the angle between the two vectors by using cosine, which can also be calculated in a vector space by using the following equations:\n",
    "\n",
    "$cos(\\theta) = \\dfrac{A\\cdot B}{\\parallel A\\parallel \\parallel B\\parallel}$ = $\\dfrac{\\sum_{i=1}^{n}A_i B_i}{\\sqrt{\\sum_{i=1}^{n}A_i^2}\\sqrt{\\sum_{i=1}^{n}B_i^2}}$\n",
    "\n",
    "Which is the dot product of the two vectors divided by each vector's euclidean distance multiplied together.\n",
    "\n",
    "* The dot product of two vectors can be defined in the algebraic sense as $A\\cdot B = A_1B_1 + A_2B_2 + \\dots + A_nB_n$\n",
    "\n",
    "* In a geometric sense, the dot product can be defined as $A\\cdot B = \\parallel A \\parallel \\parallel B \\parallel cos(\\theta)$\n",
    "\n",
    "\n",
    "\n",
    "The euclidean norm or euclidean distance is the ordinary distance from the origin to the point x.\n",
    "\n",
    "* Euclidean distance of x: $\\parallel x \\parallel = \\sqrt{x_1^2 + x_2^2 + \\dots + x_n^2}$\n",
    "\n",
    "Knowing all of this, cosine similarity is the algebraic definition of dot product divided by the two vector's euclidean distances to get the $cos(\\theta)$ that resides in the geometric definition of dot product.\n",
    "\n",
    "$A\\cdot B = \\parallel A \\parallel \\parallel B \\parallel cos(\\theta) \\longrightarrow cos(\\theta) = \\dfrac{A\\cdot B}{\\parallel A \\parallel \\parallel B \\parallel}$\n",
    "\n",
    "Therefore $cos(\\theta)$ can be calculated from just the elements of both matrices."
   ]
  }

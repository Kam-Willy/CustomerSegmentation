# Customer Segmentation with K-Means Clustering

This project provides a detailed analysis of customer data from a mall to identify distinct customer segments. By leveraging unsupervised machine learning techniques, specifically **K-Means Clustering**, the goal is to group customers with similar characteristics, which can be used to inform targeted marketing strategies, improve customer retention, and optimize resource allocation. The project also explores alternative clustering methods and dimensionality reduction using **Principal Component Analysis (PCA)** for a more robust analysis.

\<hr\>

## Key Features

  * **Data Exploration**: Initial analysis of the dataset, including descriptive statistics and visualizations of key distributions (Age, Income, Spending Score).
  * **K-Means Clustering**: Implementation of the K-Means algorithm to segment customers based on their annual income and spending score.
  * **Elbow Method**: A visual technique used to determine the optimal number of clusters (`k`) for the K-Means model.
  * **Cluster Analysis**: Detailed profiling of each customer segment to understand their unique demographics and behavioral traits. The "high-value" segment is specifically identified and analyzed.
  * **Advanced Clustering Models**: Exploration of **Agglomerative Clustering** and **DBSCAN** to compare their performance and robustness against K-Means.
  * **Model Comparison**: A quantitative comparison of K-Means and Agglomerative Clustering using the **Silhouette Score** to evaluate cluster cohesion and separation.
  * **Dimensionality Reduction**: Use of **PCA** to reduce the dimensionality of the data, which can be crucial for clustering on datasets with a high number of features.

\<hr\>

## Files and Dependencies

### Project Structure

  * `CustomerSegmentation.ipynb`: The main Python script that contains all the code for data loading, analysis, clustering, and visualization.
  * `Mall_Customers.csv`: The dataset used for this project. **Ensure this file is in the same directory as the script.**
  * `README.md`: This file, providing an overview and instructions.

### Dependencies

To run this project, you need to install the following Python libraries. It's recommended to use a virtual environment.

```bash
pip install pandas seaborn matplotlib scikit-learn
```

\<hr\>

## How to Run

1.  **Clone the Repository** (if applicable) or download the files.

2.  **Place the Dataset**: Make sure the `Mall_Customers.csv` file is in the same directory as `Mall_Customer_Segmentation.py`.

3.  **Install Dependencies**: Open your terminal or command prompt, navigate to the project directory, and run the installation command above.

4.  **Execute the Script**: Run the main script from your terminal:

    ```bash
    python CustomerSegmentation.ipynb
    ```

The script will generate several plots and print summary statistics directly to the console.

\<hr\>

## Results and Insights

The script performs the following key steps, with corresponding outputs:

1.  **Initial Data Exploration**: Prints the first few rows of the dataset and summary statistics.
2.  **Distribution Plots**: Displays histograms for `Age`, `Annual Income`, and `Spending Score`, along with a scatter plot showing `Income` vs. `Age` colored by `Gender`.
3.  **Elbow Method Plot**: Shows the WCSS (Within-Cluster Sum of Squares) against the number of clusters. The "elbow" in the plot suggests the optimal `k`.
4.  **K-Means Cluster Plot**: A scatter plot visualizing the customer segments, with each cluster color-coded and labeled with its centroid.
5.  **Cluster Summary**: A table in the console detailing the mean income, spending score, and age for each cluster.
6.  **Comparative Analysis**: Plots for **Agglomerative Clustering** and **DBSCAN** are generated, providing a visual comparison of different clustering solutions.
7.  **Performance Metrics**: The Silhouette Scores for K-Means and Agglomerative Clustering are printed to the console, providing a quantitative metric for comparison.

By analyzing the output, you can identify distinct customer groups, such as "high-income, high-spending," "low-income, low-spending," and "moderate-income, moderate-spending." This information is invaluable for creating targeted marketing campaigns and business strategies.

\<hr\>

## Further Enhancements

  * **More Features**: Incorporate other features from the dataset (like `Age` and `Gender`) into the clustering process.
  * **Automated `k` Selection**: Implement an automated method for selecting the optimal number of clusters instead of relying solely on a visual inspection of the Elbow Method plot.
  * **Production Deployment**: Save the trained models (`KMeans` and `StandardScaler`) using `joblib` or `pickle` so they can be used to predict the segment for new customer data without retraining.
  * **CLV Integration**: If transaction history data is available, calculate Customer Lifetime Value (CLV) and use it as a feature for more advanced segmentation.
  * **Interactive Visualization**: Use libraries like Plotly or Bokeh to create interactive plots that allow for dynamic exploration of the data and clusters.

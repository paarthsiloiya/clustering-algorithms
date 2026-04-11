# Clustering Algorithms Visualization & Animation

This project demonstrates reducing a real 4-dimensional dataset to 2D using Principal Component Analysis (PCA) and then animating the progression of various clustering algorithms, including standard K-Means, K-Means++, and Gaussian Mixture Models (GMM).

## Dataset Chosen
We use the **Iris Dataset** from `scikit-learn` (`sklearn.datasets.load_iris`).
* Source/Credit: R.A. Fisher (1936) via the UCI Machine Learning Repository.
* Features: 4 numerical features representing measurements (sepal length, sepal width, petal length, petal width) in centimeters.
* Justification: It is a canonical, compact real-world dataset that perfectly meets the 3-4 feature requirement and naturally benefits from PCA reduction to 2D for visualization.

## Quick Run Instructions
To reproduce the analyses and regenerate the animations, run these steps in your terminal:

1. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   # On Windows:
   .\venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```
2. Install the exact required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Start the Jupyter Notebook server:
   ```bash
   jupyter notebook
   ```
4. In the browser, navigate to the `notebooks/` directory and open any notebook (e.g., `gmm_animation.ipynb`). Click "Run All Cells" to execute the pipeline end-to-end and generate the corresponding outputs.

## Produced Files
* `notebooks/kmeans_pca_animation.ipynb`: The main reproducible notebook containing EDA, PCA, and custom step-by-step standard K-means visualization.
* `notebooks/kmeans_pp_animation.ipynb`: Exploring the smarter K-Means++ initialization algorithm.
* `notebooks/gmm_animation.ipynb`: Advanced notebook showing probabilistic Gaussian Mixture Model clustering, complete with interactive 3D likelihood surfaces using Plotly and Expectation-Maximization (EM) traces.
* `animations/`: Directory containing the final high-quality animated GIFs (e.g., `kmeans_animation.gif`, `gmm_em_animation.gif`) showcasing the cluster iterations until convergence.
* `requirements.txt`: Package versions matching this project's tested environment.
* `.gitignore`: Project git ignores (explicitly tracking GIFs).

## Future Scope
* **DBSCAN Visualization**: Adding animations for density-based spatial clustering of applications with noise.
* **Hierarchical Clustering**: Visualizing agglomerative clustering and generating interactive dendrograms.

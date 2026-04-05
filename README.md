# PCA and K-Means Animation

This project demonstrates reducing a real 4-dimensional dataset to 2D using Principal Component Analysis (PCA) and then animating the progression of a standard K-Means clustering algorithm step-by-step. 

## Dataset Chosen
We use the **Iris Dataset** from `scikit-learn` (`sklearn.datasets.load_iris`).
* Source/Credit: R.A. Fisher (1936) via the UCI Machine Learning Repository.
* Features: 4 numerical features representing measurements (sepal length, sepal width, petal length, petal width) in centimeters.
* Justification: It is a canonical, compact real-world dataset that perfectly meets the 3–4 feature requirement and naturally benefits from PCA reduction to 2D for visualization.

## Quick Run Instructions
To reproduce the analysis and regenerate the animation, run these steps in your terminal:

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
   jupyter notebook notebooks/kmeans_pca_animation.ipynb
   ```
4. In the browser, click "Run All Cells" to execute the pipeline end-to-end and generate the `kmeans_animation.gif` artifact.

## Produced Files
* `notebooks/kmeans_pca_animation.ipynb`: The main reproducible notebook containing EDA, PCA, and custom step-by-step K-means visualization.
* `kmeans_animation.gif`: The final high-quality animated GIF showcasing the cluster iterations until convergence.
* `requirements.txt`: Package versions matching this project's tested environment.
* `.gitignore`: Project git ignores (explicitly tracking GIFs).

## Future Scope
* **K-Means++ Initialization**: Adding visualizations for the smart centroid initialization technique.
* **Gaussian Mixture Models (GMM)**: Developing a probabilistic framing animation with EM steps showing changing covariance ellipses.


# **Recommendation Systems with ALS in PySpark**

## **Overview**
This project explores the development of recommendation systems using the Alternating Least Squares (ALS) algorithm in PySpark. We leverage the MovieLens and Million Songs datasets to build and fine-tune models that predict user preferences based on implicit feedback. The project demonstrates how to preprocess data, optimize model performance through hyperparameter tuning, and evaluate model predictions using custom metrics.

## **Project Structure**
- **`data/`**: Contains the datasets used in the project, including the MovieLens and Million Songs datasets.
- **`notebooks/`**: Jupyter notebooks that walk through the data preprocessing steps, model training, hyperparameter tuning, and evaluation.
- **`scripts/`**: Python scripts for data processing and ALS model implementation.
- **`results/`**: Stores the outputs, including model evaluation metrics, predictions, and visualizations.
- **`README.md`**: Project documentation.

## **Key Components**
### 1. **Data Preprocessing**
   - Handled missing values and added zeros for user-item interactions that were not explicitly rated.
   - Used cross joins to ensure all possible user-item pairs were considered, even if the user had not interacted with the item.

### 2. **Model Training and Hyperparameter Tuning**
   - Built and evaluated 192 different ALS models by varying hyperparameters like `rank`, `maxIter`, `regParam`, and `alpha`.
   - Applied cross-validation with multiple folds to ensure robust model selection.
   - Selected the best model using the ROEM (Rank Order Error Metric), a custom metric for assessing recommendation accuracy.

### 3. **Model Evaluation**
   - Assessed model performance on test datasets using the ROEM metric.
   - Analyzed specific user predictions to gain insights into the model's ability to generalize and provide meaningful recommendations.

### 4. **Recommendations**
   - Generated and analyzed recommendations for users based on the trained ALS models.
   - Focused on handling binary data and implicit feedback, which is crucial in real-world recommendation systems.

## **Installation**
To run this project locally, ensure you have the following installed:
- Python 3.x
- PySpark
- Jupyter Notebook

### **Installation Steps:**
1. Clone the repository:
   ```bash
   git clone https://github.com/data-nav/ALS_recommendation.git
   cd A_B_testing
   ```
2. Install the necessary Python packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Open the `notebooks/` directory and explore the project.

## **Usage**
- Run the notebooks in the `notebooks/` directory to see the entire workflow from data preprocessing to model evaluation.
- Modify the hyperparameters in the scripts and notebooks to experiment with different model configurations.
- Use the `scripts/` directory to integrate the ALS models into other applications or pipelines.

## **Results**
- The project identified the best-performing ALS model using cross-validation and the ROEM metric.
- The models are capable of generating accurate and meaningful recommendations based on implicit feedback.


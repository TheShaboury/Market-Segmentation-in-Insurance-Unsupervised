# Market Segmentation in Insurance - Unsupervised Learning

This project explores customer data to identify distinct customer segments using unsupervised clustering techniques and builds a classifier to predict these segments for new customers.

## 📊 Project Overview

The project analyzes insurance customer data to:
- Identify meaningful customer segments through clustering
- Build a predictive model to classify new customers into these segments
- Provide insights for targeted marketing and customer relationship management

## 🗂️ Project Structure

```
Market-Segmentation-in-Insurance-Unsupervised/
│
├── Ahmed_ElShaboury_Project_1.ipynb    # Main analysis notebook
├── Customer_Data.csv                   # Customer dataset
├── Customer_Data_Link.docx            # Data source link
├── Project_1_Notebook_Documentation.docx  # Detailed documentation
└── README.md                          # This file
```

## 📈 Dataset

**Source**: [Kaggle - Market Segmentation in Insurance](https://www.kaggle.com/datasets/jillanisofttech/market-segmentation-in-insurance-unsupervised)

**Dataset Characteristics**:
- **Size**: 8,950 customers × 18 features
- **Type**: Mixed (numerical and categorical features)
- **Key Features**: Credit limits, payment behavior, purchase patterns, balance information

## 🔧 Methodology

### 1. Data Exploration & Cleaning
- **Dataset Analysis**: Examined 8,950 rows and 18 columns
- **Missing Value Treatment**: Imputed missing values in `MINIMUM_PAYMENTS` (313 missing) and `CREDIT_LIMIT` (1 missing) using mean values
- **Data Quality**: Verified no duplicate records

### 2. Exploratory Data Analysis (EDA)
- **Distribution Analysis**: Identified skewed distributions in most features
- **Correlation Analysis**: Examined relationships between variables using heatmaps
- **Outlier Detection**: Used boxplots to identify extreme values

### 3. Data Preprocessing
- **Outlier Handling**: Applied IQR (Interquartile Range) method to cap outliers
- **Feature Scaling**: Standardized numerical features using StandardScaler
- **Dimensionality Reduction**: Applied PCA retaining 95% of variance (10 components)
- **Feature Engineering**: Created 7 new ratio and average-based features

### 4. Customer Segmentation
- **Algorithm**: K-Means Clustering
- **Optimal Clusters**: Determined 5 clusters using the elbow method
- **Evaluation**: Achieved silhouette score of ~0.20
- **Visualization**: Created scatter plots using first two PCA components

### 5. Classification Model
- **Algorithm**: Random Forest Classifier
- **Performance**: Achieved 97% accuracy on test data
- **Validation**: Used confusion matrix and classification reports

## 🎯 Key Results

### Customer Segments Identified
The analysis revealed **5 distinct customer segments**, each with unique characteristics related to:
- Spending habits and patterns
- Account balance management
- Credit utilization behavior
- Payment patterns

### Model Performance
- **Clustering Quality**: Silhouette score of ~0.20 indicating reasonable separation
- **Classification Accuracy**: 97% accuracy in predicting customer segments
- **Model Robustness**: Strong performance across all customer segments

## 🛠️ Technologies Used

- **Python 3.x**
- **Libraries**:
  - `pandas` - Data manipulation and analysis
  - `numpy` - Numerical computations
  - `scikit-learn` - Machine learning algorithms
  - `matplotlib` - Data visualization
  - `seaborn` - Statistical data visualization

## 📋 Requirements

```python
pandas>=1.3.0
numpy>=1.20.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
```

## 🚀 Usage

1. **Clone the repository**
   ```bash
   git clone [repository-url]
   cd Market-Segmentation-in-Insurance-Unsupervised
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the notebook**
   ```bash
   jupyter notebook Ahmed_ElShaboury_Project_1.ipynb
   ```

## 📊 Business Applications

This segmentation model can be used for:

- **Targeted Marketing**: Customize marketing campaigns for each customer segment
- **Product Development**: Design insurance products tailored to segment needs
- **Risk Assessment**: Better understand customer behavior patterns
- **Customer Retention**: Develop segment-specific retention strategies
- **Pricing Strategies**: Implement segment-based pricing models

## 🔍 Future Enhancements

- Experiment with different clustering algorithms (DBSCAN, Hierarchical clustering)
- Implement ensemble methods for improved classification
- Add temporal analysis for customer behavior evolution
- Develop segment-specific churn prediction models
- Create interactive dashboards for business stakeholders

## 📝 Documentation

For detailed methodology and findings, refer to:
- `Project_1_Notebook_Documentation.docx` - Comprehensive project documentation
- `Ahmed_ElShaboury_Project_1.ipynb` - Interactive analysis notebook

## 👨‍💻 Author

**Ahmed ElShaboury**

## 📄 License

This project is available under the MIT License.

---

*This project demonstrates the application of unsupervised learning techniques for customer segmentation in the insurance industry, providing actionable insights for business decision-making.*

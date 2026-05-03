# Customer Segmentation using K-Means Clustering

## 📋 Problem Statement

Retail businesses often struggle to identify distinct customer groups with different purchasing behaviors and spending patterns. Without clear segmentation, marketing strategies are often one-size-fits-all, leading to inefficient resource allocation and missed opportunities for targeted campaigns.

**Objective**: Segment customers based on their income and spending behavior to create targeted marketing strategies and improve customer engagement.

---

## 🎯 Approach

This project uses **K-Means Clustering**, an unsupervised machine learning algorithm, to automatically group customers into distinct segments based on:
- **Annual Income** (in thousands)
- **Spending Score** (1-100 scale based on purchase behavior)

### Methodology Steps:

1. **Data Understanding**: Load and explore the Mall Customer Segmentation dataset
2. **Exploratory Data Analysis (EDA)**: Visualize relationships between features
3. **Feature Selection**: Select Annual Income and Spending Score as clustering features
4. **Feature Preprocessing**: Standardize features using StandardScaler for better clustering
5. **Elbow Method**: Determine optimal number of clusters (K=5)
6. **K-Means Training**: Apply K-Means algorithm with optimal K
7. **Cluster Visualization**: Visualize and interpret customer segments
8. **Business Insights**: Provide actionable recommendations for each segment

---

## 💡 Why K-Means Clustering?

### Advantages:
- ✅ **Simple & Fast**: Computationally efficient for large datasets
- ✅ **Scalable**: Works well with hundreds or thousands of customers
- ✅ **Interpretable**: Easy to understand and explain results to stakeholders
- ✅ **Practical**: Ideal for creating actionable business segments
- ✅ **Proven**: Widely used in retail and e-commerce industries

### How It Works:
1. Randomly initializes K cluster centers
2. Assigns each customer to the nearest cluster center
3. Recalculates cluster centers based on assigned members
4. Repeats until convergence (no change in assignments)
5. **Elbow Method** helps determine optimal K by analyzing Within-Cluster Sum of Squares (WCSS)

---

## 📊 Dataset

**Source**: [Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) from Kaggle

### Features:
| Feature | Description | Range |
|---------|-------------|-------|
| Age | Customer's age | 18-76 years |
| Annual Income | Customer's annual income | $15k - $137k |
| Spending Score | Score based on spending behavior | 1-100 |

### Dataset Size:
- **Total Records**: 200 customers
- **Total Features**: 3 (Age, Income, Spending Score)

---

## 🔍 Key Findings

### Optimal Number of Clusters: K = 5

The Elbow Method analysis revealed that **K=5 clusters** provides the optimal balance between model complexity and cluster quality.

### Customer Segments Identified:

#### 🎯 **Cluster 0: Premium Customers**
- High Income + High Spending
- Target for luxury products and exclusive offers
- Highest customer lifetime value

#### 💼 **Cluster 1: Potential Customers**
- High Income + Low Spending  
- Opportunity for upselling and cross-selling
- Focus on building customer engagement

#### 🛍️ **Cluster 2: High-Value Budget Shoppers**
- Low Income + High Spending
- Loyal customers with limited budget
- Target with value deals and frequent promotions

#### 📉 **Cluster 3: Low-Engagement Customers**
- Low Income + Low Spending
- Need re-engagement strategies
- Consider retention campaigns

#### 👥 **Cluster 4: Young/Middle-Income Customers**
- Mixed characteristics
- Growing segment with potential
- Good target for new product launches

---

## 📈 Visualizations

The notebook includes the following visualizations:

1. **Age vs Spending Score** - Identify behavior patterns
2. **Income vs Spending Score** - Understanding purchasing power relationship
3. **Distribution Plots** - Feature distributions across the dataset
4. **Elbow Curve** - Optimal K determination
5. **Cluster Scatter Plot** - 2D visualization of customer segments
6. **Box Plots** - Feature distributions by cluster
7. **Centroid Markers** - Visual representation of cluster centers

---

## 🚀 Business Recommendations

### For Each Customer Segment:

**Premium Customers (High Income, High Spending)**
- Strategy: Loyalty programs, VIP treatments, exclusive products
- Budget: Higher marketing investment justified by high value
- Channel: Premium channels, personalized services

**Potential Customers (High Income, Low Spending)**
- Strategy: Product discovery, demos, free trials
- Budget: Moderate investment for upselling opportunities
- Channel: Educational content, webinars

**High-Value Budget Shoppers (Low Income, High Spending)**
- Strategy: Value deals, bundle offers, frequent promotions
- Budget: High engagement but lower individual transaction value
- Channel: Email campaigns, loyalty programs

**Low-Engagement Customers (Low Income, Low Spending)**
- Strategy: Re-engagement campaigns, retention offers
- Budget: Lower investment, focus on cost-effective channels
- Channel: Social media, seasonal promotions

---

## 📦 Installation & Setup

### Prerequisites:
- Python 3.7+
- Jupyter Notebook or JupyterLab

### Step 1: Clone or Download the Project
```bash
cd "Customer Segmentation"
```

### Step 2: Install Required Packages
```bash
pip install -r requirements.txt
```

### Step 3: Download the Dataset
1. Go to [Kaggle - Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)
2. Download `Mall_Customers.csv`
3. Place it in the `data/` folder

### Step 4: Run the Notebook
```bash
jupyter notebook Customer_Segmentation.ipynb
```

---

## 📁 Project Structure

```
Customer Segmentation/
├── README.md                          # This file
├── requirements.txt                   # Python dependencies
├── Customer_Segmentation.ipynb        # Main Jupyter notebook
├── data/
│   └── Mall_Customers.csv            # Dataset (download from Kaggle)
└── results/
    └── (Generated visualizations)
```

---

## 🛠️ Technologies Used

- **Python 3.x**: Programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib**: Static visualizations
- **Seaborn**: Statistical data visualization
- **Scikit-learn**: Machine learning library for K-Means
- **Jupyter Notebook**: Interactive computing environment

---

## 📊 Model Performance Metrics

### Elbow Method Results:
- **Optimal K**: 5 clusters
- **WCSS at K=5**: Significant drop-off (elbow point)
- **Customer Distribution**: Well-balanced across clusters

### Clustering Quality:
- Clear separation between clusters
- Interpretable cluster characteristics
- Actionable business segments

---

## 🎓 Learning Outcomes

By completing this project, you'll learn:
1. ✅ How to prepare data for clustering
2. ✅ Feature scaling and normalization techniques
3. ✅ The Elbow Method for determining optimal clusters
4. ✅ K-Means algorithm implementation
5. ✅ Cluster interpretation and business insights
6. ✅ Data visualization for exploratory analysis
7. ✅ Creating actionable business recommendations from data

---

## 🔗 References

- [K-Means Clustering - Scikit-learn Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)
- [Elbow Method Explanation](https://en.wikipedia.org/wiki/Elbow_method_(clustering))
- [Feature Scaling - StandardScaler](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html)
- [Kaggle - Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

---

## 📝 License

This project is open source and available under the MIT License.

---

## 👤 Author

Created as a comprehensive guide to customer segmentation using K-Means clustering.

**Last Updated**: May 2, 2026

---

## ❓ FAQ

**Q: What if I don't have the dataset yet?**  
A: Download it from Kaggle (link provided above) and place `Mall_Customers.csv` in the `data/` folder.

**Q: Can I use a different number of clusters?**  
A: Yes! The Elbow Method is a guide. You can modify the K value based on business needs.

**Q: How do I interpret the spending score?**  
A: Higher scores (70+) indicate high spending frequency and value. Lower scores (<30) indicate low engagement.

**Q: Can this be applied to other datasets?**  
A: Absolutely! The methodology works for any numerical features and can be adapted for different business contexts.

---

**🎉 Happy Segmenting!**

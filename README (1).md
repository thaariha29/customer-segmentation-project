# Customer Segmentation using K-Means Clustering

A complete ML project applying K-Means clustering to segment mall customers based on age, income, and spending behavior.

## Project Structure

```
├── customer_segmentation.ipynb   # Main notebook
├── requirements.txt              # Python dependencies
├── README.md                     # This file
└── Mall_Customers.csv            # Dataset (download from Kaggle — link below)
```

## Dataset

**Mall Customer Segmentation Data**  
🔗 https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

Features used:
- `Age` — customer age
- `Annual Income (k$)` — yearly income in thousands
- `Spending Score (1-100)` — mall-assigned spend behavior score

> If the CSV is not present, the notebook auto-generates synthetic data with the same structure so you can run everything immediately.

## Setup & Run

```bash
# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook customer_segmentation.ipynb
```

## Results

| Segment | Description |
|---|---|
| Young High-Spenders | Young customers with high spending scores |
| Premium Active | High income + high spending — top value customers |
| Mature Steady | Middle-aged, moderate income/spend |
| Senior Cautious | Older customers, conservative spending |

## Outputs Generated

| File | Description |
|---|---|
| `eda_distributions.png` | Feature distribution histograms |
| `eda_gender.png` | Gender pie chart |
| `eda_correlation.png` | Feature correlation heatmap |
| `optimal_k.png` | Elbow + Silhouette plots |
| `clusters_scatter.png` | 2D scatter plots for all feature pairs |
| `segment_analysis.png` | Bar charts comparing segment characteristics |
| `radar_profile.png` | Radar chart of normalized segment profiles |
| `customer_segments_output.csv` | Final dataset with cluster labels |

## Algorithm

- **K-Means++** initialization for better centroid placement
- **StandardScaler** normalization before clustering
- Optimal K selected via **Elbow Method** and **Silhouette Score**
- Final model: K=4 clusters

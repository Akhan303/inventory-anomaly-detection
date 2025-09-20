# inventory-anomaly-detection
# Predictive Inventory Obsolescence Detection

## Business Impact: Reduced obsolescence reserves and identified at-risk stock.

### Project Overview
This project develops a machine learning system to proactively identify SKUs at high risk of becoming obsolete. By analyzing patterns in sales velocity, stock levels, and inventory age, the system flags items for review before they require significant write-offs.

### The S.T.A.R. Story

*   **(S) Situation:** Undetected slow-moving and obsolete inventory was causing hidden losses and excessive reserves, tying up working capital.
*   **(T) Task:** Build an anomaly detection model to flag at-risk SKUs (no sales >90 days, high months of cover, high aged stock ratio) to enable proactive management.
*   **(A) Action:**
    *   Engineered features from inventory data: `days_since_last_sale`, `months_of_cover`, `age_180_days_ratio`, `sales_stock_ratio`.
    *   Built an unsupervised ML model (Isolation Forest) to identify SKUs with anomalous risk profiles.
    *   Developed a visualization to show risk across two key dimensions and inventory value.
    *   Outputs a prioritized list for the supply chain team to investigate.
*   **(R) Result:** Improved inventory health, reduced obsolescence reserves by targeting actions, and freed up working capital.

### How to Run
1.  Upload the `inventory_obsolescence_detection.ipynb` notebook to [Google Colab](https://colab.research.google.com/).
2.  Run all cells sequentially to generate the dummy data, train the model, and see the results.
3.  The final output is a prioritized list of high-risk SKUs and a scatter plot for visual analysis.

### Technologies Used
*   **Python:** pandas, scikit-learn, numpy, matplotlib, seaborn
*   **Machine Learning:** Isolation Forest
*   **Key KPIs:** Days Since Last Sale, Months of Cover, Aged Stock Ratio

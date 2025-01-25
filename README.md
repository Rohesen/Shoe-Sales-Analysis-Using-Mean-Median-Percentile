# 👟 Shoe Sales Analysis: Advanced Metrics with Python

## 📋 Overview  
This project focuses on analyzing shoe sales data to uncover key metrics like the **mean**, **median**, and **percentiles** of sales quantities for different brands. The project also includes 📊 visualization of sales trends over time using Python.

## ✨ Features  
- 📈 Calculate **mean**, **median**, and **percentiles** for sales quantities.  
- 📉 Visualize sales trends using **line charts** for each brand.  
- 🧠 Provide actionable insights based on the data analysis.

## 📂 Dataset  
The dataset contains the following columns:  
- 🗓️ `date`: The date of sales.  
- 🏷️ `brand`: The shoe brand (e.g., Nike, Adidas).  
- 🔢 `sold_qty`: The quantity of shoes sold on a specific date.

## 💻 Key Code Examples  

### 1️⃣ Calculate Median for "Nike" Sales  
This snippet calculates and rounds the median sales quantity for the "Nike" brand:  
```python
# Calculate the median of Nike sold quantities
df_nike.sold_qty.median()

# Round the median value
val = round(df_nike.sold_qty.median())
val
```

### 2️⃣ Line Chart for Sales Trends  
Visualize sales trends over time for both "Nike" and "Adidas":  
```python
import pandas as pd
import matplotlib.pyplot as plt

def plot_sales_trend(dataframe):
    nike_data = dataframe[dataframe['brand'] == 'Nike']
    adidas_data = dataframe[dataframe['brand'] == 'Adidas']

    plt.figure(figsize=(10, 6))

    # Plot Nike sales
    plt.plot(nike_data['date'], nike_data['sold_qty'], label='Nike', marker='o')

    # Plot Adidas sales
    plt.plot(adidas_data['date'], adidas_data['sold_qty'], label='Adidas', marker='o')

    plt.xlabel('Date')
    plt.ylabel('Sold Quantity')
    plt.title('Sales Trend for Nike and Adidas')
    plt.legend()
    plt.grid()
    plt.show()

# Call the function
plot_sales_trend(dataframe)
```

![Line Chart](https://github.com/Rohesen/Shoe-Sales-Analysis-Using-Mean-Median-Percentile/blob/main/Screenshot%202025-01-25%20171304.png)

### 3️⃣ Percentile Calculation  
Calculate the 90th percentile for sales quantities:  
```python
# Calculate the 90th percentile for Nike sales
nike_90th_percentile = df_nike.sold_qty.quantile(0.9)
nike_90th_percentile
```

## 🔍 Insights  
- 📊 Median sales for Nike provide a central value to benchmark performance.  
- 📅 Sales trends help identify peak sales periods for better inventory management.  
- 🏆 Percentile analysis highlights the top-performing days for each brand.



## ⚙️ Prerequisites  
- 🐍 Python 
- 📦 Pandas  
- 📈 Matplotlib  

## 🚀 How to Run  
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/shoe-sales-analysis.git
   ```  
2. Install the required libraries:  
   ```bash
   pip install pandas matplotlib
   ```  
3. Run the Jupyter Notebook to view the analysis:  
   ```bash
   jupyter notebook shoe_sales_analysis.ipynb
   ```  

## 🏁 Conclusion  
This project demonstrates how to use Python for data analysis and visualization to extract meaningful insights from sales data. The combination of statistical metrics and visualizations provides a comprehensive view of brand performance over time.  

![Conclusion](https://github.com/Rohesen/Shoe-Sales-Analysis-Using-Mean-Median-Percentile/blob/main/Screenshot%202025-01-25%20171630.png)

---  
Feel free to explore the code and contribute! 🚀✨  

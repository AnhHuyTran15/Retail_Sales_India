# Retail_Sales_India
# 📦 Supply Chain Demand Forecasting: Making Sense of Retail Chaos

Hi there! Welcome to my forecasting project. 👋

If there's one thing I've learned about retail data, it's that real-world sales don't look like the perfectly smooth curves we see in textbooks; it is so messy as well as chaotic

I built this project because I wanted to bridge the gap between academic Retail World and the actual, dealing with and analysing chaotic data that businesses deal with every day. Instead of just building a standard descriptive dashboard in Power BI, I decided to embed Python directly into it to turn historical data into actionable, forward-looking insights.

## 🤔 The Problem I Tried to Solve
Imagine you're managing inventory for a retail brand. If you order too much, cash gets tied up in the warehouse (Overstock). If you order too little, you miss out on sales and anger customers (Stockouts). 

My goal here was to answer two critical Sales & Operations Planning (S&OP) questions:
1. **How much will we sell next month?** (Baseline Demand)
2. **How much extra should we keep in the back room just in case?** (Safety Stock)

## 🛠️ The Journey & The Models
I didn't just throw one algorithm at the data and call it a day. I experimented with a few different calculation models to see what actually works for messy retail data:

* **Facebook Prophet:** I started here because it's fantastic at handling missing data and recognizing holiday spikes. It gave me a great visual of the "Safety Stock Boundary" (the 95% confidence interval). 
* ***Holt-Winters (The Winner for this dataset!):** When the data got too wild, ARIMA just gave me a flat line. I switched to Holt-Winters and applied a *Damped Trend* with auto-optimized parameters (Alpha, Beta, Gamma). This forced the algorithm to respect recent weekly cycles without letting the long-term forecast shoot up to unrealistic numbers.

## 💻 Tech Stack Used
* **Power BI:** For the frontend dashboard and data modeling.
* **Python:** Embedded directly into Power BI to do the heavy lifting.
* **Libraries:** `pandas`, `matplotlib`, `prophet`, `pmdarima`, `statsmodels`.

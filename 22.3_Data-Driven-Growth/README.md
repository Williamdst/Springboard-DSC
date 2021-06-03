<h2>Growth Hacking - <i>Data Driven Growth</i></h2>
<b>Part 1: Know Your Metrics</b><br />
In the first part I had information from an online retail store and used the "North Star Metric" of Monthly Revenue to guide the analytics. <i>The North Star Metric is the single metric that best captures the core value that your product delivers to customers.</i> Some of the analytics done were:
<ul>
  <li> Revenue by Type of Customer </li>
  <li> New Customer Ratio </li>
  <li> Cohort Based Retention Rate </li>
</ul>

<b>Part 2: Customer Segmentation</b><br /> 
In this part I used the same data to do a Recency, Frequency, Monetary customer segmentation. For each category I used a simple KMeans with 4 clusters to determine the segment. Then for each customer they got a overall score based on the summation of each cluster. <br /> 

<b>Part 3: Customer Lifetime Value Prediction</b><br />
Building off the ideas in the last part a machine learning model that predicts customers' lifetime value was created. To do this, 3 months of data was used and the same RFM clustering was done as before. Then a lifetime value column was artificially created using KMeans (in the same way) on the revenue generated from a customer 6 months later. This artificial LTV column is what was the supervised XGBoost model was trained to predict. <br /> 

<h2>Reflection</h2>

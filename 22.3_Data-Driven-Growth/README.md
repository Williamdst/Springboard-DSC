<h2>Growth Hacking - <i>Data Driven Growth</i></h2>
<b>Part 1: Know Your Metrics</b><br />
In the first part I had transaction information from an online retail store and used the "North Star Metric" of Monthly Revenue to guide the analytics. <i>The North Star Metric is the single metric that best captures the core value that your product delivers to customers.</i> Some of the analytics done were:
<ul>
  <li> Revenue by Type of Customer </li>
  <li> New Customer Ratio </li>
  <li> Cohort Based Retention Rate </li>
</ul>

<b>Part 2: Customer Segmentation</b><br /> 
In this part I used the same data to do a Recency, Frequency, Monetary customer segmentation. For each category I used a simple KMeans with 4 clusters to determine the segment. Then for each customer they got a overall score based on the summation of each cluster. <br /> 

<b>Part 3: Customer Lifetime Value Prediction</b><br />
Building off the ideas in the last part a machine learning model that predicts customers' lifetime value was created. To do this, 3 months of data was used and the same RFM clustering was done as before. Then a lifetime value column was artificially created using KMeans (in the same way) on the revenue generated from a customer 6 months later. This artificial LTV column is what was the supervised XGBoost model was trained to predict. <br /> 

<b>Part 5: Predicting Next Purchase Day</b><br />
To build a model that can be used to predict next customer purchase the transaction data into two parts: 6 months and the following 3 months. The six months of data is used to predict customers' first purchase data in the following three months. All of the basic models with defualt settings were used, but XGBoost Classifier had the best accuracy and it was further tuned to increase from 58% to 62%. <br />

<b>Part 6: Predicting Sales</b><br />
In this part, sales was predicted by using time series forecasting data and the Keras LSTM model. The idea here was to find the difference between a month’s sales and every previous month’s sales to create a dataframe that had 12 months of lag data, and then train forecasting model on that dataframe. Before implementing this strategy two things were important:
<ol>
  <li>Differencing was used to make the time series stationary.</li>
  <li>The lag data are features that are good enought to explain the variation in the target label. To check this Ordinary Least Squares was used to calculate the adjusted r-squared value. When all the lag data was used, it explains 98% of the variance of the target label. </li>
</ol>

<b>Part 7: Market Response Models </b><br />
Customers have been segmented, their lifetime value has been predicted, and sales have been predicted as well. The next natural question is how to increase sales, specifically do offeres increase conversion and if yes what kind of offer performs best on what segment of customers. In this part I had general data on customers combined with the results of a marketing campaign. The marketing data showed which type of coupon the customer used in the past (if any), which offer was sent to them, and if they converted based on the offer sent. A model was built to predict the probability of conversion and the resuting uptick in orders and revenue. The results were compared to the actual conversion and its uptick in orders and revenue.

<b>Part 8: Uplift Modeling</b><br />
Uplift modeling is a predictive technique that directly models the incremental impact of a treatment on an individual's behavior. When planning to launch a promotional campaign you don't need to send the offer to everyone. For example, you don't need to send an offer to someone who is going to buy from you regardless. There are four kinds of customers:
<ol>
  <li><b>Treatment Responders (<i>Persuadables</i>)</b>: Customers that will purchase something only if they receive some sort of offer.</li>
  <li><strike>Treatment Nonresponders (<i>Lost Causes</i>)</strike>: Customers that aren’t going to buy anything regardless of what you do.</li>
  <li><strike>Control Responders (<i>Sure Things</i>)</strike>: Customers that are going to buy something regardless of what you do.</li>
  <li><b>Control Nonresponders (<i>Sleeping Dogs</i>)</b>: Customers that will not purchase anything if they don’t receive an offer. <i>You have to dangle a treat in front of them to "wake" them up.</i></li>
</ol>
The idea behind uplift modeling is to give customers an overall uplift score based on the predicted probabilites of the class labels. Then determine the potential uptick in orders and revenue for a specific discount on a specific range of uplift scores (<i>Typically a high or low uplift grouping based on some cutoff value </i>).<br> </br>

<b>Part 9: A/B Testing</b><br />

<h2>Reflection</h2>

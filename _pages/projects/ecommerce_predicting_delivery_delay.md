---
permalink: /projects/ecommerce_predicting_delivery_delay/
title: " "
---
<!-- leave title:" " and we make the title ourself below -->

<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>

<!-- title of the project -->
<div style="font-size: 1.3em; font-weight: bold; margin-top: 2em; margin-bottom: 0.2em;">
  Predicting Delivery Delays with Machine Learning
</div>

<span style="color:#D0D0D0; font-size: 0.7em">
<a href="https://github.com/Camille-Le-Roy/" target="_blank" style="color:#A8A8A8; text-decoration: underline;">See the project on GitHub</a>
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/delivery delay header.png" alt=" " style="width: 90%; max-height: 430px; object-fit: cover; border-radius: 10px;">
</div>



## Project Overview

<span style="color:#D0D0D0; font-size: 0.9em">
Delivery delays are a major driver of customer dissatisfaction, often resulting in negative reviews and, ultimately, churn. In a <a href="https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce" target="_blank" style="color:#D0D0D0; text-decoration: underline;">previous project</a> analyzing customer behavior using the Olist e-commerce dataset, I identified logistics issues impacting the customer experience. Here, I address those issues by building a machine learning model, powered by XGBoost, to predict delivery delays and help logistics teams reducing late shipments.
<br><br>
My analysis aims at answering the following questions:
</span>

<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
  <li>Which factors related to orders, logistics, and customers have the greatest impact on whether a delivery is late?</li>
  <li>Do temporal patterns influence delivery performance?</li>
  <li>What actionable steps can be taken to prevent future delivery delays?</li>
</ul>


## Working Datasets

<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
  This analysis uses the <a href="https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce" target="_blank" style="color:#D0D0D0; text-decoration: underline;">Olist Brazilian E-commerce dataset</a> , which originally comprises nine relational tables covering orders, customers, products, sellers, payments, and reviews. For efficient exploration and modeling, these tables were cleaned, merged, and transformed in a previous data-pipeline project, resulting in three Analytical Base Tables (ABTs) focusing on orders, customers, and products. This project focuses on the order-level dataset.
</ul>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/Fig. 1. ERD customer analysis.png" alt=" " style="width: 90%; object-fit: cover; border-radius: 10px;">
</div>

<div style="text-align: center; color: #A8A8A8; font-size: 0.8em; margin-bottom: 2em;">
  <strong>Figure 1.</strong> Entity Relationship Diagram showing the three relational datasets used in this project.  
  <br>See the <a href="/projects/ecommerce_data_pipeline/" target="_blank" style="color:#A8A8A8; text-decoration: underline;">Data Pipeline</a> project for details on data preprocessing. 
  <br><span style="font-size: 0.75em;">PK: Primary Key; FK: Foreign Key.</span>
</div>


## Feature Engineering

<ul style="color:#D0D0D0; font-size:0.9em; margin-top:0.5em; line-height:1.5em; list-style:none; padding-left:0;">

  <li>
    <strong>Target variable</strong>:<br>
    The model aims at predicting 
    <code style="background-color:#333; color:#fff; padding:2px 4px; border-radius:4px; font-family:monospace;">is_late</code>
    (0 or 1), derived from the difference between the actual delivery date and the estimated delivery date.
  </li>

  <br>

  <li>
    <strong>Candidate features</strong>:<br>
    Based on the original dataset, I engineered a set of predictors capturing temporal patterns, economic behavior, logistics complexity, and customer loyalty:
    <br><br>
  </li>

</ul>


<!-- Feature Engineering Table -->
<table style="width:100%; color:#D0D0D0; font-size:0.85em; border-collapse:collapse; margin-top:1em;">
  <thead>
    <tr style="border-bottom:1px solid #555;">
      <th style="text-align:left; padding:6px;">Feature</th>
      <th style="text-align:left; padding:6px;">Source</th>
      <th style="text-align:left; padding:6px;">Computation Method</th>
    </tr>
  </thead>
  <tbody>

    <tr>
      <td style="padding:6px;">Temporal</td>
      <td style="padding:6px;">order purchase timestamp</td>
      <td style="padding:6px;">Extract year/month/hour components</td>
    </tr>

    <tr>
      <td style="padding:6px;">is_weekend</td>
      <td style="padding:6px;">Day of week</td>
      <td style="padding:6px;">Binary flag for Sat/Sun</td>
    </tr>

    <tr>
      <td style="padding:6px;">is_holiday_season</td>
      <td style="padding:6px;">Month</td>
      <td style="padding:6px;">Binary flag for Nov/Dec</td>
    </tr>

    <tr>
      <td style="padding:6px;">approval_delay_hours</td>
      <td style="padding:6px;">Timestamps</td>
      <td style="padding:6px;">approved_at − purchase_timestamp</td>
    </tr>

    <tr>
      <td style="padding:6px;">carrier_pickup_days</td>
      <td style="padding:6px;">Timestamps</td>
      <td style="padding:6px;">carrier_date − approved_at</td>
    </tr>

    <tr>
      <td style="padding:6px;">freight_percentage</td>
      <td style="padding:6px;">Price ratio</td>
      <td style="padding:6px;">(freight / price) × 100</td>
    </tr>

    <tr>
      <td style="padding:6px;">total_order_value</td>
      <td style="padding:6px;">Price</td>
      <td style="padding:6px;">price + freight_value</td>
    </tr>

    <tr>
      <td style="padding:6px;">revenue_per_km</td>
      <td style="padding:6px;">Price + distance</td>
      <td style="padding:6px;">price / distance_km</td>
    </tr>

    <tr>
      <td style="padding:6px;">is_high_value</td>
      <td style="padding:6px;">Threshold</td>
      <td style="padding:6px;">Top 10% quantile flag</td>
    </tr>

    <tr>
      <td style="padding:6px;">customer_order_count</td>
      <td style="padding:6px;">Aggregation</td>
      <td style="padding:6px;">Count orders per customer_unique_id</td>
    </tr>

    <tr>
      <td style="padding:6px;">days_since_last_order</td>
      <td style="padding:6px;">Date difference</td>
      <td style="padding:6px;">dataset_end − last_order_date</td>
    </tr>

    <tr>
      <td style="padding:6px;">distance_km</td>
      <td style="padding:6px;">Geospatial calculation</td>
      <td style="padding:6px;">Geodesic distance (seller ↔ customer)</td>
    </tr>

    <tr>
      <td style="padding:6px;">distance_category</td>
      <td style="padding:6px;">Binning</td>
      <td style="padding:6px;">Distance discretized into 4 categories</td>
    </tr>

  </tbody>
</table>


<ul style="color:#D0D0D0; font-size:0.9em; margin-top:2.5em; line-height:1.5em; list-style:none; padding-left:0;">

  <li>
    <strong>Redundant Features and Data Leakage</strong>:<br>
    To simplify the model and improve generalization, highly correlated features (correlation coefficient > 0.7) were removed. Additionally, variables that were directly derived from the target, or reflecting information that would not be available at prediction time, was excluded to prevent data leakage.
  </li>

  <br>

  <li>
    <strong>Encodings</strong>:<br>
    Categorical variables including less that 50 levels were one-hot-encoded to improve model interpretability.
  </li>

</ul>



## Modeling Approach

<span style="color:#D0D0D0; font-size: 0.9em">
I used a <strong>Gradient Boosting approach (XGBoost)</strong> for predicting delivery delays because it is well suited to model complex, non-linear relationships in structured data (typical of logistics datasets). Moreover, it handles real-world messy data (skewed distribution, outliers, missing values, etc) very well, and is widely recognized as one of the top-performing algorithms for tabular classification.
</span>

<ul style="color:#D0D0D0; font-size:0.9em; margin-top:0.5em; line-height:1.5em; list-style:none; padding-left:0;">

  <li>
    <strong>Data Splitting</strong>:<br>
    The dataset of 95,936 orders was divided into training, validation, and test subsets to train, tune, and evaluate the model respectively.
  </li>
</ul>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/delivery delay data splitting.png" alt=" " style="width: 70%; object-fit: cover; border-radius: 10px;">
</div>

<ul style="color:#D0D0D0; font-size:0.9em; margin-top:0.5em; line-height:1.5em; list-style:none; padding-left:0;">
  <li>
    <strong>Hyper parameter tuning</strong>:<br>
    Initially, early stopping was applied to identify the optimal number of boosting rounds and mitigate overfitting. Second, a randomized search was conducted to optimize key hyperparameters of the XGBoost model, further improving predictive performance and generalization.
    <br><br>
  </li>
</ul>


## Model Evaluation

<span style="color:#D0D0D0; font-size: 0.9em">
The final XGBoost model achieved a ROC AUC score of 0.84 on the unseen test set. This indicates that the model can correctly predict whether a delivery will be late 84% of the time.
</span>


## Feature Importance & Insights

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/delivery delay feature importance.png" alt=" " style="width: 70%; object-fit: cover; border-radius: 10px;">
</div>
<span style="color:#D0D0D0; font-size: 0.9em">
The model identified the seller’s handling speed as the strongest predictor of delivery delays (an intuitive result). Although not directly controllable, the company could prioritize or incentivize sellers with faster processing times.
<br><br>
</span>

<ul style="color:#D0D0D0; font-size:0.9em; margin-top:0.5em; line-height:1.6em; list-style:none; padding-left:0;">

  <li>
    <strong>Temporal Patterns</strong>:
  </li>

  <div style="margin-top: 1.2em; margin-bottom: 1.2em; display: flex; justify-content: center;">
    <img src="/assets/images/delivery delay time effect.png" alt="Temporal effect on delivery delays" style="width: 100%; max-width: 1000px; object-fit: cover; border-radius: 10px;">
  </div>

  <li>
    Temporal dynamics played a significant role in predicting delivery delays.  
    In Olist’s early development phase (2016), deliveries were generally faster, but delays increased as the company scaled.  
    Seasonality also emerged: delays peaked in <strong>March</strong> and <strong>November</strong>, while <strong>June</strong> showed the most on-time deliveries.  
    Additionally, orders placed on <strong>Fridays</strong> tended to experience slightly longer delays.
    <br><br>
  </li>

  <li>
    <strong>Geographic Distance</strong>:
  </li>

  <div style="margin-top: 1.2em; margin-bottom: 1.2em; display: flex; justify-content: center;">
    <img src="/assets/images/delivery delay distance effect.png" alt="Temporal effect on delivery delays" style="width: 60%; max-width: 1000px; object-fit: cover; border-radius: 10px;">
  </div>

  <li>
    Delivery delays tend to increase with distance. While this is an intuitive pattern, it highlights an issue in the delivery date estimation process, which appears to insufficiently account for distance.
    <br><br>
  </li>

  <li>
    <strong>Customer Recency</strong>:
  </li>

  <li>
    Orders placed by customers who have been inactive for a long time show a lower likelihood of late delivery. While the factors underlying this pattern warrant further investigation, it most likely reflects the temporal trend observed earlier in the analysis.
  </li>

</ul>


## Conclusion & Next Steps 



<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>
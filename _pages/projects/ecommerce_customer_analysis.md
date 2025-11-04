---
permalink: /projects/ecommerce_customer_analysis/
title: " "
---
<!-- leave title:" " and we make the title ourself below -->

<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>

<!-- title of the project -->
<div style="font-size: 1.3em; font-weight: bold; margin-top: 2em; margin-bottom: 0.2em;">
  E-Commerce Sales Trends and Customer Analysis
</div>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/header image ecommerce saels trend and customer analysis.png" alt=" " style="width: 90%; max-height: 380px; object-fit: cover; border-radius: 10px;">
</div>


## Introduction

<span style="color:#D0D0D0; font-size: 0.9em">
Olist is one of Brazil’s leading e-commerce platforms. Founded in 2015, it connects small and medium-sized businesses by connecting them with major online marketplaces across the country, and is now expanding its presence internationally.
<br><br>
This project uses real commercial data from Olist's early operational period (2016–2018), encompassing over 100,000 orders, to explore the following questions:
</span>

<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
  <li>How did Olist’s total sales evolve across months and product categories? Are there clear seasonal patterns or growth phases?</li>
  <li>Can customers be grouped into clusters based on their purchasing behavior and value?</li>
  <li>Which customer segments and product categories contribute most to total revenue, and which represent growth opportunities?</li>
</ul>


## Executive Summary
<span style="color:#D0D0D0; font-size: 0.9em">
To be written at the end.<br><br>
</span>


## Working Datasets
<span style="color:#D0D0D0; font-size: 0.9em">
The entity Relationship Diagram for the 3 relational datasets used in this project (see the Data Pipeline project for more detail about the data preprocessing).
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/ERD customer analysis.png" alt=" " style="width: 90%; object-fit: cover; border-radius: 10px;">
</div>
<span style="color:#D0D0D0; font-size: 0.7em">
PK: Principal Key; FK Foreign Key. <br>
</span>


## Detailed Insights

### Sales Trends and Growth Rate

<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
  <li>Olist recorded over $4.8 million in online sales between 2016 and 2018 (~$2.2 million per year), receiving an average of 48,000 orders per year.</li>
  <li>The company experienced strong growth in 2016-2017, with an average monthly growth rate of 14.7%, while it slowed to 2.6% in 2018, indicating a period of stabilization after rapid expansion</li>
  <li>The Southeast region (comprising the states of São Paulo, Rio de Janeiro, and Minas Gerais) accounts for 63% of total sales, totaling approximately 3 millions USD.</li>
</ul>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/Fig. 1. ecommerce sale trends.png" alt=" " style="width: 60%; object-fit: cover; border-radius: 10px;">
</div>


### Customer Behavior

<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
    <li>Only 3.1% of Olist customers made repeat purchases, generating 5.6% of the total revenue.</li>
    <li>
        Four distinct customer segments were identified based on purchasing behavior, satisfaction, and delivery experience:
        
        <ul style="color:#D0D0D0; font-size: 1em; margin-top: 0.5em; list-style-type: none;">
            
            <li>
                <strong>Cluster 1 – High-Value Premium Buyers:</strong>
                <ul style="font-size: 0.9em; margin-top: 0.3em;">
                    <li>Customers with the highest spending per order (≈ 192 USD) and strong satisfaction (4.0/5).</li>
                    <li>They purchase high-value products and experience early deliveries.</li>
                    <li>Although mostly one-time buyers, they represent highly profitable transactions.</li>
                </ul>
            </li>

            <li>
                <strong>Cluster 2 – Satisfied Low-Spending Shoppers:</strong>
                <ul style="font-size: 0.9em; margin-top: 0.3em;">
                    <li>The largest group, making single, low-value purchases (~34 USD) with excellent satisfaction (4.7/5).</li>
                    <li>They experience early deliveries and pay relatively high freight costs.</li>
                    <li>Represent happy but casual customers with low long-term engagement.</li>
                </ul>
            </li>

            <li>
                <strong>Cluster 3 – Unsatisfied Low-Spending Shoppers:</strong>
                <ul style="font-size: 0.9em; margin-top: 0.3em;">
                    <li>Lowest satisfaction segment (1.8/5) with small purchases (~37 USD).</li>
                    <li>Deliveries are slower, and freight costs are high (~37% of total order value).</li>
                    <li>This group highlights potential service and logistics issues affecting customer experience.</li>
                </ul>
            </li>
            
            <li>
                <strong>Cluster 4 – Loyal Repeat Customers:</strong>
                <ul style="font-size: 0.9em; margin-top: 0.3em;">
                    <li>The only segment with repeat purchasing behavior (~2 orders per customer).</li>
                    <li>They are satisfied (4.1/5), buy moderately priced items (~45 USD), and maintain average freight costs.</li>
                    <li>This cluster represents loyal, consistent customers and a key retention opportunity.</li>
                </ul>
            </li>

        </ul>
        </li>
     <li>Overall, the majority of revenue is driven by Cluster 2, with an average monthly share of 47.1%, followed by Cluster 1 at 36.6%, while Cluster 3 and Cluster 4 contribute smaller but significant amounts, averaging 10.3% and 6.0% of monthly revenue, respectively.</li>    
</ul>





## Recommendation

<span style="color:#D0D0D0; font-size: 0.9em">
 I built an data processing pipeline in Python that transforms 9 relational datasets (100K+ orders) into two analytics-ready base tables with 40+ engineered features for business intelligence.
</span>


## Assumptions and Caveats


## Code

<div style="margin-top: 1.5em; font-size: 0.9em; color: #D0D0D0;">
  <span>
    This pipeline is implemented in Python and is openly available on 
    <i class="fab fa-github" style="color:#fff;"></i>
    <a href="https://github.com.git" 
       target="_blank" 
       style="color: #3B82F6; text-decoration: none; font-weight: bold;">
      GitHub
    </a>.
  </span>
</div>


<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>
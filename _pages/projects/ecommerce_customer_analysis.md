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


## Table of Contents

<div style="color:#D0D0D0; font-size: 0.9em; line-height: 1.6em; margin-top: 0.5em;">
  <ol style="margin-left: 1.2em;">
    <li><a href="#introduction" style="color:#D0D0D0; text-decoration: none;">Introduction</a></li>
    <li><a href="#executive-summary" style="color:#D0D0D0; text-decoration: none;">Executive Summary</a></li>
    <li><a href="#working-datasets" style="color:#D0D0D0; text-decoration: none;">Working Datasets</a></li>
    <li><a href="#detailed-insights" style="color:#D0D0D0; text-decoration: none;">Detailed Insights</a>
      <ul style="margin-top: 0.2em; margin-bottom: 0.5em;">
        <li><a href="#sales-trends-and-growth-rate" style="color:#D0D0D0; text-decoration: none;">Sales Trends and Growth Rate</a></li>
        <li><a href="#customer-behavior" style="color:#D0D0D0; text-decoration: none;">Customer Behavior</a></li>
      </ul>
    </li>
    <li><a href="#recommendation" style="color:#D0D0D0; text-decoration: none;">Recommendations</a></li>
    <li><a href="#assumptions-and-caveats" style="color:#D0D0D0; text-decoration: none;">Assumptions and Caveats</a></li>
    <li><a href="#code" style="color:#D0D0D0; text-decoration: none;">Code</a></li>
  </ol>
</div>



## Introduction

<span style="color:#D0D0D0; font-size: 0.9em">
Olist is one of Brazil’s leading e-commerce platforms. Founded in 2015, it connects small and medium-sized businesses by connecting them with major online marketplaces across the country, and is now expanding its presence internationally.
<br><br>
This project uses <a href="https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce" target="_blank" style="color:#D0D0D0; text-decoration: underline;">real commercial data</a> from Olist's early operational period (2016–2018), encompassing over 100,000 orders, to explore the following questions:
</span>

<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
  <li>How did Olist’s total sales evolve across months and product categories? Are there clear seasonal patterns or growth phases?</li>
  <li>Can customers be grouped into clusters based on their purchasing behavior and value?</li>
  <li>Which customer segments and product categories contribute most to total revenue, and which represent growth opportunities?</li>
</ul>


## Executive Summary

<div style="color:#D0D0D0; font-size: 0.9em;">
    Between 2016 and 2018, Olist processed over 100,000 orders, generating approximately <strong>$4.8 million in sales</strong>. The company experienced rapid expansion in 2017, with an average monthly growth rate of <strong>14.7%</strong>, followed by a period of stabilization in 2018 (<strong>2.6% monthly growth</strong>).
    <br><br>
    The <strong>Southeast region</strong>, including São Paulo, Rio de Janeiro, and Minas Gerais, emerged as the dominant market, contributing <strong>63% of total revenue</strong>.
    <br><br>
    Customer segmentation revealed <strong>four main behavioral profiles</strong> based on purchasing patterns, satisfaction, and delivery experience:
    
    <ul style="margin-top: 0.5em; /* Inherits color and font-size from the parent div */">
        <li><strong>High-Value Premium Buyers:</strong> Highest spend per order and strong satisfaction, though mostly one-time purchasers.</li>
        <li><strong>Satisfied Low-Spending Shoppers:</strong> Largest group; highly satisfied but with low transaction values.</li>
        <li><strong>Unsatisfied Low-Spending Shoppers:</strong> Lowest satisfaction due to delayed deliveries and high freight costs.</li>
        <li><strong>Loyal Repeat Customers:</strong> Small but valuable group with consistent repeat purchases and steady satisfaction.</li>
    </ul>
    
    Overall, <strong>Clusters 1 and 2 account for over 80% of total revenue</strong>, while improving logistics and customer retention offers significant opportunities for sustained growth.
</div>


## Working Datasets

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/Fig. 1. ERD customer analysis.png" alt=" " style="width: 90%; object-fit: cover; border-radius: 10px;">
</div>

<div style="text-align: center; color: #A8A8A8; font-size: 0.8em; margin-bottom: 2em;">
  <strong>Figure 1.</strong> Entity Relationship Diagram showing the three relational datasets used in this project.  
  <br>See the <a href="/projects/ecommerce_data_pipeline/" target="_blank" style="color:#A8A8A8; text-decoration: underline;">Data Pipeline</a> project for details on data preprocessing. 
  <br><span style="font-size: 0.75em;">PK: Primary Key; FK: Foreign Key.</span>
</div>


## Detailed Insights

### Sales Trends and Growth Rate

<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
  <li>Olist recorded over $4.8 million in online sales between 2016 and 2018 (~$2.2 million per year), receiving an average of 48,000 orders per year. The Average Order Value (AOV) is of 50 USD and remained constant across time.</li>
  <li>The company experienced strong growth in 2016-2017, with an average monthly growth rate of 14.7%, while it slowed to 2.6% in 2018, indicating a period of stabilization after rapid expansion.</li>
  <li>The Southeast region (comprising the states of São Paulo, Rio de Janeiro, and Minas Gerais) accounts for 63% of total sales, totaling approximately 3 millions USD.</li>
</ul>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/Fig. 2. ecommerce sale trends.png" alt=" " style="width: 50%; object-fit: cover; border-radius: 10px;">
</div>

<div style="text-align: center; color: #A8A8A8; font-size: 0.8em; margin-bottom: 2em;">
  <strong>Figure 2.</strong> Monthly growth rate, average order value, and total sales, from top to bottom, respectively. The trends capture Olist’s early development phase across 2017–2018. Data from late 2016 were excluded due to limited volume and irregular patterns in this initial period.
</div>


### Customer Behavior

<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
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
</ul>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/Fig. 3. ecommerce customer clusters.png" alt=" " style="width: 60%; object-fit: cover; border-radius: 10px;">
</div>

<div style="text-align: center; color: #A8A8A8; font-size: 0.8em; margin-bottom: 2em;">
  <strong>Figure 3.</strong> Top: Monthly sales by customer cluster during the 2017–2018 period. Bottom: Radar chart illustrating the key behavioral and value attributes of each cluster.
</div>


<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
  <li>Overall, the majority of revenue is driven by Cluster 2, with an average monthly share of 47.1%, followed by Cluster 1 at 36.6%, while Cluster 3 and Cluster 4 contribute smaller but significant amounts, averaging 10.3% and 6.0% of monthly revenue, respectively.</li>
  <li>Only 3.1% of Olist customers made repeat purchases, which nonetheless contributed to 5.6% of the total revenue.</li>
</ul>



## Recommendation

<div style="color:#D0D0D0; font-size: 0.9em;">
    The analysis highlights key opportunities to improve Olist’s growth trajectory and customer satisfaction. Strategic actions should focus on <strong>enhancing retention, optimizing logistics, and differentiating customer experiences</strong> across segments.
    
    <ul style="margin-top: 0.5em; /* Inherits font size and color from parent div */">
        <li><strong> Retain High-Value Buyers:</strong> Implement loyalty incentives, premium delivery options, or exclusive product bundles to foster repeat purchases among top spenders, with a focus on <strong>Customer Cluster 1</strong>.</li>
        <li><strong> Convert Satisfied Low-Spending Shoppers:</strong> Encourage higher basket values through targeted upselling, product recommendations, or free-shipping thresholds, specifically targeting <strong>Customer Cluster 2</strong>.</li>
        <li><strong> Improve Delivery Performance:</strong> Address delays and high freight costs affecting low-satisfaction customers through better carrier partnerships and delivery tracking.</li>
        <li><strong> Strengthen Customer Retention:</strong> Given that only 3.1% of customers make repeat purchases, develop reactivation campaigns and personalized follow-ups to increase repeat rates.</li>
        <li><strong> Regional Expansion:</strong> Build on the Southeast region’s strong performance by replicating best practices in emerging markets with growing e-commerce adoption.</li>
    </ul>
    
    By implementing these strategies, Olist can <strong>leverage its existing customer base, improve satisfaction, and unlock long-term profitability</strong> across its marketplace network.
</div>


## Assumptions and Caveats

<ul style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
  <li>The analyzed dataset covers a relatively short time period and reflects an early stage in the company’s development. This limits the ability to identify seasonal patterns, which typically emerge more clearly over longer time spans.</li>
  <li>Despite the large volume of data (over 100,000 orders), the dataset contains very few repeat customers. This limits the feasibility of a traditional Recency–Frequency–Monetary (RFM) segmentation approach. nstead, a combination of alternative customer characteristics was used to identify behavioral clusters, providing a broader range of insights, albeit through an unconventional approach.. </li>
</ul>

## Code

<div style="margin-top: 1.5em; font-size: 0.9em; color: #D0D0D0;">
  <span>
    The analysis was implemented in Python and is openly available on 
    <i class="fab fa-github" style="color:#fff;"></i>
    <a href="https://github.com/Camille-Le-Roy/E-Commerce-Sales-Trends-and-Customer-Analysis/tree/main" 
       target="_blank" 
       style="color: #3B82F6; text-decoration: none; font-weight: bold;">
      GitHub
    </a>.
  </span>
</div>


<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>
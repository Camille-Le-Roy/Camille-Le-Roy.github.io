---
permalink: /projects/ecommerce_data_pipeline/
title: " "
---
<!-- leave title:" " and we make the title ourself below -->

<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>

<!-- title of the project -->
<div style="font-size: 1.3em; font-weight: bold; margin-top: 2em; margin-bottom: 0.2em;">
  E-Commerce Data Processing Pipeline
</div>

<span style="color:#D0D0D0; font-size: 0.7em">
<a href="https://github.com/Camille-Le-Roy/E-Commerce-Data-Processing-Pipeline" target="_blank" style="color:#A8A8A8; text-decoration: underline;">See the project on GitHub</a>
</span>

<span style="color:#D0D0D0; font-size: 0.9em">
 I built an data processing pipeline in Python that transforms 9 relational datasets (100K+ orders) into three analytics-ready base tables with 40+ engineered features for business intelligence.
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/AI_Generated_ecommerce_elongate.png" alt=" " style="width: 100%; max-height: 380px; object-fit: cover; border-radius: 10px;">
</div>



## Motivation

<span style="color:#D0D0D0; font-size: 0.9em">
Real-world e-commerce data is rarely analysis-ready and often lacks key features needed for modeling tasks such as pricing optimization, churn prediction, or logistics improvement. A critical step is transforming raw, fragmented transactional tables into clean analytical datasets.
In this project, I used a publicly available <a href="https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce" target="_blank" style="color:#D0D0D0; text-decoration: underline;">Brazilian marketplace dataset (2016–2018)</a> to demonstrate this process.
</span>




## Raw datasets

<span style="color:#D0D0D0; font-size: 0.9em">
The initial 9 relational datasets are presented via an Entity Relationship Diagram (ERD), defining the cardinality and mapping the relationships between entities.
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/ERD list datasets.png" alt=" " style="width: 90%; object-fit: cover; border-radius: 10px;">
</div>

<span style="color:#D0D0D0; font-size: 0.7em">
PK: Principal Key; FK Foreign Key. <br>
</span>


## How It Works

<div style="color:#D0D0D0; font-size: 0.9em; margin-top: 1.5em; margin-bottom: 1.5em;">
    <p style="margin-bottom: 0.5em;">The data pipeline is built on a four-phase approach:</p>
    <ol style="padding-left: 20px;">
        <li><strong> Ingestion:</strong> Data is loaded from 9 interconnected CSV files (Orders, Items, Payments, Reviews, Customers, Sellers, Products, Geolocation, and Translations) to form the initial relational model.</li>
        <li><strong> Preparation:</strong> Data is cleaned, standardized, and aggregated to resolve one-to-many relationships (e.g., aggregating multiple payments per order).</li>
        <li><strong> Merging:</strong> Strategic Left Joins are used to enrich the core `Orders` table with contextual data (items, payments, reviews, customer info).</li>
        <li><strong> Feature Engineering:</strong> Over 40 business-relevant metrics are derived, including RFM scores, delivery logistics features, and seller performance indicators.</li>
    </ol>
    <p style="margin-top: 0.5em;">The process outputs three complementary Analytical Base Tables (ABTs): at the order, product, and customer level, ready for modeling. .</p>
</div>



<div style="margin-top: 1.5em; margin-bottom: 1.5em; display: flex; justify-content: center;">
  <img src="/assets/images/dataprocessing scheme full.png" alt=" " style="width: 90%; object-fit: cover; border-radius: 10px;">
</div>


## Engineered Features

<div style="color:#D0D0D0; font-size: 0.9em; margin-top: 0.5em;">
    <p style="margin-bottom: 0.5em;">The engineered features derives from the initial columns span the following analytical dimensions:</p>
    <ul>
        <li>
            <strong>Temporal Features:</strong> Year/month/day/hour extraction, weekend indicators, holiday season flags, approval delays, and carrier pickup times.
        </li>
        <li>
            <strong>Delivery Performance:</strong> Delivery delay calculations, purchase-to-delivery time, delivery status categories (early/on-time/late), and speed classifications.
        </li>
        <li>
            <strong>Customer Analytics (RFM):</strong> Order frequency, recency (days since last order), customer lifetime value, and repeat customer identification.
        </li>
        <li>
            <strong>Economic Metrics:</strong> Average price per item, freight percentage of total, high-value order flags, and customer lifetime value calculations.
        </li>
        <li>
            <strong>Product & Seller Analytics:</strong> Category popularity, seller performance rankings, weight-to-price ratios, premium product identification, and top seller indicators.
        </li>
    </ul>
</div>


## Results

<span style="color:#D0D0D0; font-size: 0.9em">
The pipeline successfully processed 100,000+ orders across a 2-year period, reducing analytical query complexity by merging 9 tables into 3 purpose-built ABTs. The engineered features enable advanced analytics including RFM customer segmentation, delivery KPI monitoring, seller performance benchmarking, and product catalogue optimization, without requiring complex multi-table joins at query time.
</span>


## Code

<div style="margin-top: 1.5em; font-size: 0.9em; color: #D0D0D0;">
  <span>
    This pipeline is implemented in Python and is openly available on 
    <i class="fab fa-github" style="color:#fff;"></i>
    <a href="https://github.com/Camille-Le-Roy/E-Commerce-Data-Processing-Pipeline" 
       target="_blank" 
       style="color: #3B82F6; text-decoration: none; font-weight: bold;">
      GitHub</a>.
  </span>
</div>


<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>
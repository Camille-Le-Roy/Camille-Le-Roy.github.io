---
layout: splash
title: "Camille Le Roy, Ph.D."
excerpt: "Researcher • Data Scientist • Founder of Morpho Editing"
description: "Camille Le Roy, Ph.D — Data Scientist and Biologist working at the intersection of data, research, and communication"
classes: wide
header:
  overlay_image: /assets/images/canopy resized.jpg
  overlay_filter: "0.3"
  caption: " "
author_profile: true
show_social: true
related: false
comments: false
---

<style>
.page__hero--overlay {
  min-height: 40vh;
  display: flex;
  align-items: flex-end;
}

.page__hero--overlay .wrapper {
  padding-bottom: 10px;
}

/* --- PROFILE SECTION --- */
.profile-section {
  display: flex;
  align-items: stretch;
  gap: 40px;
  margin: 0 auto 80px 0;
}

/* image */
.profile-image {
  flex: 0 0 43%;
}

.profile-image img {
  width: 100%;
  height: auto;
  border-radius: 15px;
  display: block;
}

/* text */
.profile-text {
  flex: 0 0 60%;
}

.profile-text p {
  font-size: 1.1rem;
  line-height: 1.6;
  color: #D0D0D0;
  margin: 0;
}

/* --- PROJECTS --- */
.featured-projects {
  display: flex;
  flex-wrap: wrap;
  gap: 2em;
  justify-content: space-evenly;
}

.project-card {
  flex: 1 1 300px;
  max-width: 420px;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease, border 0.3s ease;
  border: 1px solid #555;
  border-radius: 8px;
  background-color: #1a1a1a;
}

.project-card img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 8px;
}

.project-card h3 {
  color: #E0E0E0;
  font-size: 1.2em;
  margin: 0.8em 0 0.4em;
}

.project-card h3 a {
  text-decoration: none;
  color: inherit;
}

.project-card:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 20px rgba(0,0,0,0.35);
  z-index: 10;
  border-color: #888;
}

/* --- MOBILE --- */
@media (max-width: 960px) {
  .featured-projects {
    justify-content: center;
  }
}

@media (max-width: 768px) {
  .profile-section {
    flex-direction: column;
    gap: 20px;
  }

  .profile-image,
  .profile-text {
    flex: 1 1 100%;
  }

  .profile-image img {
    max-height: 350px;
    object-fit: cover;
  }
}

@media (max-width: 650px) {
  .project-card {
    width: 100%;
  }
}
</style>

<div class="profile-section">

  <!-- profile picture -->
  <div class="profile-image">
    <img 
      src="/assets/images/profile picture balcony black and white zoomed.png" 
      alt="Camille Le Roy - Research Scientist">
  </div>

  <!-- text -->
  <div class="profile-text">
    <p>
      I am a scientist working at the intersection of data, research, and communication.
      <br><br>
      
      After 7+ years of academic research in <strong>biology</strong> and <strong>biomechanics</strong>, I now focus on how complex work is communicated. I founded  <a href="https://camille-le-roy.github.io/MorphoEdit/" target="_blank" style="color: #3B82F6; text-decoration: none; font-weight: bold;">Morpho Editing</a>, an academic editorial and coaching service where I help students and researchers shape their work into clear and compelling narratives.
      <br><br>
      
      Besides my editorial work, I am also a <strong>data science</strong> instructor. I leverage my research skills to tackle complex data challenges, utilizing analytics, visualization, and machine learning to extract meaningful insights from raw information.
    </p>
  </div>

</div>

<br>

<!-- Featured Projects -->
<h2 style="color:#E0E0E0; font-size:1.5em; margin-bottom:1em;">
  Featured Projects
</h2>

<!-- Research Section FIRST -->
<h3 style="color:#BBBBBB; font-weight:500; text-align:center; width:100%; margin-bottom:1em; margin-top:0.5em;">
  <br>Research-Driven Projects<br><br>
</h3>

<div class="featured-projects">

  <!-- Research Project 1 -->
  <div class="project-card">
    <a href="/projects/3D_reconstruction/">
      <img src="/assets/images/AI wb kinematics figure 2 for main index transparent.png" alt="Quantifying 3D Motion">
    </a>
    <h3>
      <a href="/projects/3D_reconstruction/">
        Quantifying 3D Motion
      </a>
    </h3>
  </div>

  <!-- Research Project 2 -->
  <div class="project-card">
    <a href="/projects/wing_heatmap_generator/">
      <img src="/assets/images/wing heatmap_smaller transparent.png" alt="Wing Damage Heatmap Generator">
    </a>
    <h3>
      <a href="/projects/wing_heatmap_generator/">
        Wing Damage Heatmap Generator
      </a>
    </h3>
  </div>

  <!-- Research Project 3 -->
  <div class="project-card">
    <a href="/projects/IN_PROGRESS/">
      <img src="/assets/images/butterflies 3 views transparent.png" alt="Video Tracking">
    </a>
    <h3>
      <a href="/projects/IN_PROGRESS/">
        Video Tracking
      </a>
    </h3>
  </div>

</div>

<!-- Divider -->
<div style="width:100%; border-bottom:1px solid #444; margin:4em 0 2em 0;"></div>

<!-- Applied Analytics Section -->
<h3 style="color:#BBBBBB; font-weight:500; text-align:center; width:100%; margin-bottom:1em; margin-top:0.5em;">
  Applied Analytics<br><br>
</h3>

<div class="featured-projects">

  <!-- Analytics Project 1 -->
  <div class="project-card">
    <a href="/projects/Diptera_Tableau_dashboard/">
      <img src="/assets/images/Diptera_Dashboard_screenshot transparent.png" alt="Interactive Data Visualization">
    </a>
    <h3>
      <a href="/projects/Diptera_Tableau_dashboard/">
        Interactive Data Visualization using <em>Tableau</em>
      </a>
    </h3>
  </div>

  <!-- Analytics Project 2 -->
  <div class="project-card">
    <a href="/projects/ecommerce_customer_analysis/">
      <img src="/assets/images/header image ecommerce short transparent.png" alt="E-Commerce Sales Trends & Customer Analysis">
    </a>
    <h3>
      <a href="/projects/ecommerce_customer_analysis/">
        E-Commerce Sales Trends & Customer Analysis
      </a>
    </h3>
  </div>

  <!-- Analytics Project 3 -->
  <div class="project-card">
    <a href="/projects/ecommerce_predicting_delivery_delay/">
      <img src="/assets/images/delivery delay header rounded.png" alt="Predicting Delivery Delays with Machine Learning">
    </a>
    <h3>
      <a href="/projects/ecommerce_predicting_delivery_delay/">
        Predicting Delivery Delays with Machine Learning
      </a>
    </h3>
  </div>

  <!-- Analytics Project 4 -->
  <div class="project-card">
    <a href="/projects/ecommerce_data_pipeline/">
      <img src="/assets/images/dataprocessing scheme no text transparent 2.png" alt="E-Commerce Data Processing Pipeline">
    </a>
    <h3>
      <a href="/projects/ecommerce_data_pipeline/">
        E-Commerce<br> Data Processing Pipeline
      </a>
    </h3>
  </div>

</div>
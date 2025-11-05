---
layout: splash
title: "Camille Le Roy, Ph.D."
excerpt: "Data scientist and biologist"
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

<div style="display: flex; align-items: center; gap: 0px; margin: 30px auto 80px 0;">  <!-- margin is defined in the order "top, right, bottom, left" -->

  <!-- Image Section -->
  <div style="max-width: 35%; margin-right: 0px;"> 
    <img src="/assets/images/WUR profile picture black&white.png" alt="WUR profile picture black&white" style="width: 73%; height: auto; display: block; border-radius: 15px;">
  </div>

  <!-- Text Section -->
  <div style="max-width: 60%; margin-left: 0px; margin-right: 0px;">
    <p style="font-size: 1rem; line-height: 1.6; color: #D0D0D0;">
      Hi, I'm Camille, a researcher turned data scientist. <br><br>
      After 7+ years of academic research in biology and biomechanics, 
    I’m now focusing on applied data science, using analytics, visualization, and machine learning to solve real-world problems and guide decision-making.
    </p>
  </div>
</div>

<!-- OLD TEXT
      Hi, and welcome to my website! <br><br>
      I’m a postdoctoral researcher in the Experimental Zoology Group at Wageningen University. 
      My research combines computational analysis, biomechanics, and ecological approaches in the field to investigate the evolution of animal locomotion, morphology, and behavior.
 -->



<br>



<!-- Featured Projects Section -->
<h2 style="color:#E0E0E0; font-size:1.5em; margin-bottom:1em;">Featured Projects</h2>

<h3 style="color:#BBBBBB; font-weight:500; text-align:center; width:100%; margin-bottom:1em; margin-top:0.5em;">
  Applied Analytics
</h3>

<div class="featured-projects" style="display:flex; flex-wrap:wrap; gap:2em; justify-content:center;">

  <!-- Applied Analytics Project 1 -->
  <div class="project-card" style="text-align:center; width:280px;">
    <a href="/projects/ecommerce_customer_analysis/">
      <img src="/assets/images/header image ecommerce short.png" alt="E-Commerce Sales Trends & Customer Analysis" style="width:100%; border-radius:10px;">
    </a>
    <h3 style="margin-top:0.6em;">
      <a href="/projects/ecommerce_customer_analysis/" style="color:#E0E0E0; text-decoration:none;">
        E-Commerce Sales Trends & Customer Analysis
      </a>
    </h3>
  </div>

  <!-- Applied Analytics Project 2 -->
  <div class="project-card" style="text-align:center; width:280px;">
    <a href="/projects/ecommerce_data_pipeline/">
      <img src="/assets/images/dataprocessing scheme no text.png" alt="E-Commerce Data Processing Pipeline" style="width:100%; border-radius:10px;">
    </a>
    <h3 style="margin-top:0.6em;">
      <a href="/projects/ecommerce_data_pipeline/" style="color:#E0E0E0; text-decoration:none;">
        E-Commerce Data Processing Pipeline
      </a>
    </h3>
  </div>

  <!-- Applied Analytics Project 3 -->
  <div class="project-card" style="text-align:center; width:280px;">
    <a href="/projects/Diptera_Tableau_dashboard/">
      <img src="/assets/images/Diptera_Dashboard_screenshot.png" alt="Interactive Data Visualization" style="width:100%; border-radius:10px;">
    </a>
    <h3 style="margin-top:0.6em;">
      <a href="/projects/Diptera_Tableau_dashboard/" style="color:#E0E0E0; text-decoration:none;">
        Interactive Data Visualization using <em>Tableau</em>
      </a>
    </h3>
  </div>

  <!-- Divider -->
  <div style="width:100%; border-bottom:1px solid #444; margin:2em 0;"></div>

  <!-- Research Section -->
  <h3 style="color:#BBBBBB; font-weight:500; text-align:center; width:100%; margin-bottom:1em; margin-top:0.5em;">
    Research
  </h3>

  <!-- Research Project 1 -->
  <div class="project-card" style="text-align:center; width:280px;">
    <a href="/projects/3D_reconstruction/">
      <img src="/assets/images/AI wb kinematics figure 2 for main index.png" alt="Quantifying 3D Motion" style="width:100%; border-radius:10px;">
    </a>
    <h3 style="margin-top:0.6em;">
      <a href="/projects/3D_reconstruction/" style="color:#E0E0E0; text-decoration:none;">
        Quantifying 3D Motion
      </a>
    </h3>
  </div>

  <!-- Research Project 2 -->
  <div class="project-card" style="text-align:center; width:280px;">
    <a href="/projects/wing_heatmap_generator/">
      <img src="/assets/images/wing heatmap_smaller.png" alt="Wing Damage Heatmap Generator" style="width:100%; border-radius:10px;">
    </a>
    <h3 style="margin-top:0.6em;">
      <a href="/projects/wing_heatmap_generator/" style="color:#E0E0E0; text-decoration:none;">
        Wing Damage Heatmap Generator
      </a>
    </h3>
  </div>

  <!-- Research Project 3 -->
  <div class="project-card" style="text-align:center; width:280px;">
    <a href="/projects/IN_PROGRESS/">
      <img src="/assets/images/butterflies 3 views.png" alt="Video Tracking" style="width:100%; border-radius:10px;">
    </a>
    <h3 style="margin-top:0.6em;">
      <a href="/projects/IN_PROGRESS/" style="color:#E0E0E0; text-decoration:none;">
        Video Tracking
      </a>
    </h3>
  </div>

</div>




<!-- Styles -->
<style>
.featured-projects {
  display: flex;
  flex-wrap: wrap;
  gap: 2em;
  justify-content: space-evenly; /* distribute evenly across the row */
}

.project-card {
  flex: 1 1 300px; /* flexible growth: min width 300px, expands to fill */
  max-width: 420px;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 8px;
}

.project-card h3 {
  color: #E0E0E0;
  font-size: 1.2em;  /* size of title */
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
}

/* Mobile responsive */
@media (max-width: 960px) {
  .featured-projects {
    justify-content: center;
  }
}

@media (max-width: 650px) {
  .project-card {
    width: 100%;
  }
}
</style>


---
layout: splash
title: "Camille Le Roy, Ph.D."
excerpt: "Researcher • Biologist • Data Scientist"
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
  align-items: center;
  gap: 40px;
  margin: 0 auto 40px 0;
}

/* image */
.profile-image {
  flex: 0 0 38%;
}

.profile-image img {
  width: 90%;
  height: auto;
  border-radius: 12px;
  display: block;
}

/* text */
.profile-text {
  flex: 0 0 58%;
}

.profile-text p {
  font-size: 1.15rem;
  line-height: 1.65;
  color: #D0D0D0;
  margin: 0 0 1rem 0;
}

.profile-text p:last-child {
  margin-bottom: 0;
}

.profile-text strong {
  color: #D0D0D0;
  font-weight: 600;
}

/* --- ACTIVITIES GRID --- */
.activities-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 28px;
  margin-bottom: 60px;
}

.activity-card {
  display: flex;
  flex-direction: column;
  text-decoration: none !important;
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 10px;
  overflow: hidden;
  transition: border-color 0.25s ease, background 0.25s ease, transform 0.25s ease;
}

.activity-card:hover {
  background: rgba(255, 255, 255, 0.04);
  border-color: rgba(255, 255, 255, 0.18);
  transform: translateY(-2px);
  text-decoration: none !important;
}

/* Unzoomed framing while maintaining clean card bleed */
.activity-card-img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  object-position: center;
  display: block;
  transition: transform 0.3s ease;
}

.activity-card:hover .activity-card-img {
  transform: scale(0.98);
}

.activity-card-body {
  padding: 20px 24px 24px 24px;
}

/* Centering the 3rd card on row 2 */
.activity-card.full-width-centered {
  grid-column: 1 / -1;
  max-width: 640px;
  width: 100%;
  justify-self: center;
  box-sizing: border-box;
}

.activity-title {
  font-size: 0.90rem;
  font-weight: 600;
  line-height: 1.4;
  color: #E0E0E0;
  margin-bottom: 12px;
  letter-spacing: 0.2px;
  text-decoration: none !important;
}

.activity-desc {
  font-size: 0.90rem;
  line-height: 1.6;
  color: #A0A0A0;
  margin: 0;
  text-decoration: none !important;
}

/* --- EXTERNAL LINKS STYLING --- */
.ext-link {
  font-weight: 600;
  display: inline-flex;
  align-items: center;
  gap: 3px;
  margin-top: 2px;
  text-decoration: none !important;
}

.ext-link::after {
  content: "↗";
  font-size: 0.85em;
  line-height: 1;
  display: inline-block;
}

.activity-card:hover .ext-link,
.activity-card:hover .activity-title {
  text-decoration: none !important;
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
@media (max-width: 900px) {
  .activities-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }

  .activity-card.full-width-centered {
    grid-column: auto;
    max-width: 100%;
  }

  .activity-card-img {
    height: 190px;
  }
}

@media (max-width: 768px) {
  .profile-section {
    flex-direction: column;
    gap: 25px;
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

<!-- TOP PROFILE SECTION -->
<div class="profile-section">

  <!-- profile picture -->
  <div class="profile-image">
    <img 
      src="/assets/images/profile picture balcony black and white zoomed.png" 
      alt="Camille Le Roy - Research Scientist">
  </div>

  <!-- intro text -->
  <div class="profile-text">
    <p>
      I am a scientist working at the intersection of data, research, and communication.
    </p>
    <p>
      After 7+ years of academic research in <strong>biology</strong> and <strong>biomechanics</strong>, I now work across research consulting, academic coaching, and data science education.
    </p>
  </div>

</div>

<br>

<!-- SUBTLE ACTIVITY CARDS -->
<div class="activities-grid">

  <!-- Card 1: Wild Kinematics -->
  <a href="https://camille-le-roy.github.io/wildkinematics/" target="_blank" class="activity-card">
    <img 
      src="/assets/images/activity_card_wil_kinematics.png" 
      alt="Wild Kinematics Illustration" 
      class="activity-card-img">
    <div class="activity-card-body">
      <div class="activity-title">
        Research consulting<br>
        <span class="ext-link" style="color: #68a795;">Wild Kinematics</span>
      </div>
      <p class="activity-desc">
        I help researchers and organizations design movement studies, capture high-quality motion data, and turn it into meaningful biological insights.
      </p>
    </div>
  </a>

  <!-- Card 2: Morpho Editing -->
  <a href="https://camille-le-roy.github.io/MorphoEdit/" target="_blank" class="activity-card">
    <img 
      src="/assets/images/activity_card_academic_coaching.jpg" 
      alt="Academic Coaching Illustration" 
      class="activity-card-img">
    <div class="activity-card-body">
      <div class="activity-title">
        Academic coaching<br>
        <span class="ext-link" style="color: #3B82F6;">Morpho Editing & Coaching</span>
      </div>
      <p class="activity-desc">
        I help students and researchers improve their scientific writing, develop their research narratives, and cross the finish line with their manuscripts and theses.
      </p>
    </div>
  </a>

  <!-- Card 3: Data Science Bootcamp -->
  <a href="https://github.com/Camille-Le-Roy/Python_Data_Analytics_Bootcamp" target="_blank" class="activity-card full-width-centered">
    <img 
      src="/assets/images/analytics_banner.png" 
      alt="Python Data Analytics Bootcamp Banner" 
      class="activity-card-img">
    <div class="activity-card-body">
      <div class="activity-title">
        Data science teaching<br>
        <span class="ext-link" style="color: #E5A83B;">Python Data Analytics Bootcamp</span>
      </div>
      <p class="activity-desc">
        I teach in a Python and data analytics bootcamp, helping students tackle complex data challenges using statistical analysis, data visualization, and machine learning.
      </p>
    </div>
  </a>

</div>
<br>


{% comment %}
<!-- Featured Projects -->
<h2 style="color:#E0E0E0; font-size:1.5em; margin-bottom:1em;">
  Featured Projects
</h2>

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
  
  <!-- Tableau DataViz project -->
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
{% endcomment %}
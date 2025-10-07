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
      Hi, and welcome to my website! <br><br>
      I’m a postdoctoral researcher in the Experimental Zoology Group at Wageningen University. 
      My research combines computational analysis, biomechanics, and ecological approaches in the field to investigate the evolution of animal locomotion, morphology, and behavior.
    </p>
  </div>
</div>


<br>



<!-- Featured Projects Section -->
<h2 style="color:#E0E0E0; font-size:1.5em; margin-bottom:1em;">Featured Projects</h2>

<div class="featured-projects">
  <!-- Project 1 -->
  <div class="project-card">
    <a href="/projects/3D_reconstruction/">
      <img src="/assets/images/AI wb kinematics figure 2 for main index.png" alt="Quantifying 3D Motion">
    </a>
    <h3><a href="/projects/3D_reconstruction/">Quantifying 3D Motion</a></h3>
  </div>

  <!-- Project 2 -->
  <div class="project-card">
    <a href="/projects/wing_heatmap_generator/">
      <img src="/assets/images/wing heatmap_smaller.png" alt="Wing Damage Heatmap Generator">
    </a>
    <h3><a href="/projects/wing_heatmap_generator/">Wing Damage Heatmap Generator</a></h3>
  </div>

  <!-- Project 3 -->
  <div class="project-card">
    <a href="/projects/IN_PROGRESS/">
      <img src="/assets/images/butterflies 3 views.png" alt="Video Tracking">
    </a>
    <h3><a href="/projects/IN_PROGRESS/">Video Tracking</a></h3>
  </div>
</div>

  <!-- Project 4 -->
  <div class="project-card">
    <a href="/projects/Diptera_Tableau_dashboard/">
      <img src="/assets/images/Diptera_Dashboard_screenshot.png" alt="Diptera dashboard">
    </a>
    <h3><a href="/projects/Diptera_Tableau_dashboard/">Interactive Data Vizualisation</a></h3>
  </div>



<!-- Styles -->
<style>
.featured-projects {
  display: flex;
  flex-wrap: wrap;
  gap: 2em;
  justify-content: center;
}

.project-card {
  text-align: center;
  width: 360px;       /* size of the card */
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


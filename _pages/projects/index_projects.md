---
permalink: /projects/
title: "Projects"
---

<a id="projects"></a> <!-- Scroll target -->

<!-- format style to add an hovering effect on each project section -->
<style>
  .project-card {
    display: flex;
    gap: 1.5em;
    align-items: center;
    margin-bottom: 2em;
    padding: 8px; /* slight breathing room */
    border-radius: 12px;
    transition: transform 0.25s ease, box-shadow 0.25s ease;
  }

  .project-card:hover {
    transform: scale(1.02);
    box-shadow: 0 6px 14px rgba(0,0,0,0.35);
  }

  .project-card img {
    border-radius: 8px;
  }

  .project-title a {
    color: #E0E0E0;
    text-decoration: none;
    font-size: 1.3em;
    font-weight: bold;
  }

  .project-subtitle {
    color: #D0D0D0;
    font-size: 0.9em;
  }

  .project-subtitle a {
    color: #999;
    text-decoration: none;
  }

  .divider {
    height: 2px;
    background: linear-gradient(to right, #333, #666, #333);
    margin: 3em 0;
  }
</style>

<!-- Project 1 -->
<div class="project-card">
  <a href="/projects/in_progress/">
    <img src="/assets/images/Diptera_Dashboard_screenshot.png" style="width: 380px; height: auto;">
  </a>
  <div>
    <div class="project-title">
      <a href="/projects/in_progress/">
        Visualizing Complex Data using <em>Tableau</em>
      </a>
    </div>
    <span class="project-subtitle">
      An interactive visualization of wingbeat kinematics diversity in Dipteran insects <br>
      <a href="/projects/in_progress/">Read more →</a>
    </span>
  </div>
</div>

<div class="divider"></div>

<!-- Project 2 -->
<div class="project-card">
  <a href="/projects/3D_reconstruction/">
    <img src="/assets/images/AI wb kinematics figure 2.png" style="width: 290px; height: auto;">
  </a>
  <div>
    <div class="project-title">
      <a href="/projects/3D_reconstruction/">
        Quantifying 3D Motion
      </a>
    </div>
    <span class="project-subtitle">
      Behind the scenes of 3D motion capture for insect flight <br>
      <a href="/projects/3D_reconstruction/">Read more →</a>
    </span>
  </div>
</div>

<div class="divider"></div>

<!-- Project 3 -->
<div class="project-card">
  <a href="/projects/wing_heatmap_generator/">
    <img src="/assets/images/wing heatmap.png" style="width: 400px; height: auto;">
  </a>
  <div>
    <div class="project-title">
      <a href="/projects/wing_heatmap_generator/">
        Wing Damage Heatmap Generator
      </a>
    </div>
    <span class="project-subtitle">
      An R-based tool for mapping spatial frequency of wing damage on insect wings <br>
      <a href="/projects/wing_heatmap_generator/">Read more →</a>
    </span>
  </div>
</div>

<div class="divider"></div>



<!-- Ideas of project to show in this section:

- tracking movements (deeplabcut) 
- trimming synching and background subtraction using openCV
- Ilam's python equivalent to wingImage processor?

-->
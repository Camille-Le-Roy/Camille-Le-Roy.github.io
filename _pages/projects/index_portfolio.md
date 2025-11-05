---
permalink: /projects/
title: "Portfolio"
---

<a id="projects"></a>

<!-- Intro text -->
<div style="color:#D0D0D0; font-size: 0.9em; flex: 1; line-height: 1.6; text-align: justify; margin-bottom: 2em;">
  <p>
    My portfolio highlights both research-driven projects and applied analytics work. Click a category below to explore projects in each area.<br>
  </p>
</div>

<!-- ===== STYLES ===== -->
<style>
  /* Section header buttons */
  .section-header {
    text-align: center;
    background: linear-gradient(90deg, #222, #333);
    color: #E0E0E0;
    font-weight: bold;
    font-size: 1.2em;
    padding: 0.8em 0;
    border-radius: 10px;
    margin: 1.5em 0;
    cursor: pointer;
    transition: all 0.25s ease;
  }

  .section-header:hover {
    background: linear-gradient(90deg, #333, #444);
    transform: scale(1.03);
    box-shadow: 0 6px 12px rgba(0,0,0,0.3);
  }

  .section-header img {
    width: 95%;
    max-width: 650px;
    height: auto;
    border-radius: 10px;
    margin-top: 0.6em;
  }

  /* Project cards */
  .project-card {
    display: flex;
    gap: 1.5em;
    align-items: center;
    margin-bottom: 2em;
    padding: 8px;
    border-radius: 12px;
    transition: transform 0.25s ease, box-shadow 0.25s ease;
  }

  .project-card:hover {
    transform: scale(1.07);
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

  /* Hidden sections */
  .project-section {
    display: none;
    animation: fadeIn 0.4s ease;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(-10px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>

<!-- ===== JAVASCRIPT (toggle functionality) ===== -->
<script>
  function toggleSection(id) {
    const section = document.getElementById(id);
    const currentlyVisible = section.style.display === 'block';
    document.querySelectorAll('.project-section').forEach(s => s.style.display = 'none');
    if (!currentlyVisible) section.style.display = 'block';
    window.scrollTo({ top: section.offsetTop - 100, behavior: 'smooth' });
  }

  // have open "Applied Analytics Projects" by default:
  window.addEventListener('DOMContentLoaded', () => {
    document.getElementById('analytics-projects').style.display = 'block';
  });
</script>

<!-- ===== CATEGORY HEADERS ===== -->

<div class="section-header" onclick="toggleSection('research-projects')">
  Research
  <br>
  <img src="/assets/images/research_banner.png" alt=" ">
</div>

<div class="section-header" onclick="toggleSection('analytics-projects')">
  Applied Analytics
  <br>
  <img src="/assets/images/analytics_banner.png" alt=" ">
</div>


<!-- ===== RESEARCH PROJECTS ===== -->
<div id="research-projects" class="project-section">

  <div class="divider"></div>

  <div class="project-card">
    <a href="/projects/3D_reconstruction/">
      <img src="/assets/images/AI wb kinematics figure 2.png" style="width: 290px; height: auto;">
    </a>
    <div>
      <div class="project-title">
        <a href="/projects/3D_reconstruction/">Quantifying 3D Motion</a>
      </div>
      <span class="project-subtitle">
        Behind the scenes of 3D motion capture for insect flight <br>
        <a href="/projects/3D_reconstruction/">Read more →</a>
      </span>
    </div>
  </div>

  <div class="divider"></div>

  <div class="project-card">
    <a href="/projects/Diptera_Tableau_dashboard/">
      <img src="/assets/images/Diptera_Dashboard_screenshot.png" style="width: 380px; height: auto;">
    </a>
    <div>
      <div class="project-title">
        <a href="/projects/Diptera_Tableau_dashboard/">Interactive Data Visualization</a>
      </div>
      <span class="project-subtitle">
        An interactive visualization of wingbeat kinematics diversity in Dipteran insects <br>
        <a href="/projects/Diptera_Tableau_dashboard/">Read more →</a>
      </span>
    </div>
  </div>

  <div class="divider"></div>

  <div class="project-card">
    <a href="/projects/wing_heatmap_generator/">
      <img src="/assets/images/wing heatmap.png" style="width: 400px; height: auto;">
    </a>
    <div>
      <div class="project-title">
        <a href="/projects/wing_heatmap_generator/">Wing Damage Heatmap Generator</a>
      </div>
      <span class="project-subtitle">
        An R-based tool for mapping spatial frequency of wing damage on insect wings <br>
        <a href="/projects/wing_heatmap_generator/">Read more →</a>
      </span>
    </div>
  </div>

   <div class="divider"></div>

  <div class="project-card">
    <a href="/projects/IN_PROGRESS/">
      <img src="/assets/images/butterflies 3 views.png" style="width: 400px; height: auto;">
    </a>
    <div>
      <div class="project-title">
        <a href="/projects/IN_PROGRESS/">Video Tracking</a>
      </div>
      <span class="project-subtitle">
        <!-- write something here --> <br>
        <a href="/projects/IN_PROGRESS/">Read more →</a>
      </span>
    </div>
  </div>

</div>


<!-- ===== ANALYTICS PROJECTS ===== -->
<div id="analytics-projects" class="project-section">

  <div class="divider"></div>

  <div class="project-card">
    <a href="/projects/ecommerce_customer_analysis/">
      <img src="/assets/images/header image ecommerce short.png" style="width: 350px; height: auto;">
    </a>
    <div>
      <div class="project-title">
        <a href="/projects/ecommerce_customer_analysis/">E-Commerce Sales Trends & Customer Analysis</a>
      </div>
      <span class="project-subtitle">
        A BI-approach to analyzing customer segments and growth <br>
        <a href="/projects/ecommerce_customer_analysis/">Read more →</a>
      </span>
    </div>
  </div>

  <div class="divider"></div>

<div class="project-card">
    <a href="/projects/ecommerce_data_pipeline/">
      <img src="/assets/images/dataprocessing scheme no text.png" style="width: 350px; height: auto;">
    </a>
    <div>
      <div class="project-title">
        <a href="/projects/ecommerce_data_pipeline/">E-Commerce Data Processing Pipeline</a>
      </div>
      <span class="project-subtitle">
        A Python pipeline transforming raw e-commerce data into clean analytical tables <br>
        <a href="/projects/ecommerce_data_pipeline/">Read more →</a>
      </span>
    </div>
  </div>

  <div class="divider"></div>

  <div class="project-card">
    <a href="/projects/Diptera_Tableau_dashboard/">
      <img src="/assets/images/Diptera_Dashboard_screenshot.png" style="width: 380px; height: auto;">
    </a>
    <div>
      <div class="project-title">
        <a href="/projects/Diptera_Tableau_dashboard/">Interactive Data Visualization</a>
      </div>
      <span class="project-subtitle">
        An interactive visualization of wingbeat kinematics diversity in Dipteran insects <br>
        <a href="/projects/Diptera_Tableau_dashboard/">Read more →</a>
      </span>
    </div>
  </div>

</div>




<!-- Ideas of project to show in this section:

- tracking movements (deeplabcut) 
- trimming synching and background subtraction using openCV
- Ilam's python equivalent to wingImage processor?

-->
---
permalink: /projects/
title: "Portfolio"
---

<a id="projects"></a>

<!-- Intro text -->
<div style="color:#D0D0D0; font-size: 0.9em; flex: 1; line-height: 1.6; text-align: justify; margin-bottom: 2em;">
  <p>
    My portfolio highlights both applied analytics and research-driven projects. Click a category below to explore projects in each area.
  </p>
</div>

<!-- ===== STYLES ===== -->
<style>

  /* ==== CATEGORY BANNERS ==== */
  .section-header {
    text-align: center;
    color: #D0D0D0;
    font-weight: bold;
    font-size: 2rem;
    padding: 0;
    height: 180px;
    border-radius: 12px;
    margin: 1.5em 0;
    cursor: pointer;

    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;

    display: flex;
    justify-content: center;
    align-items: center;

    transition: transform 0.25s ease, box-shadow 0.25s ease;
    text-shadow: 0 0 8px rgba(0,0,0,0.6);
  }

  .section-header:hover {
    transform: scale(1.03);
    box-shadow: 0 6px 12px rgba(0,0,0,0.3);
  }

  /* banner image assignment */
  .research-banner {
    background-image: url('/assets/images/research_banner_2.png');
  }
  .analytics-banner {
    background-image: url('/assets/images/analytics_banner_2.png');
  }

  /* ===== BANNERS SIDE BY SIDE ===== */
  .banner-row {
    display: flex;
    gap: 1.5em;
    justify-content: center;
    margin: 1.5em 0;
  }

  .banner-row .section-header {
    flex: 1;
    max-width: 50%;
  }

  @media (max-width: 750px) {

  /* Larger banners on mobile */
  .section-header {
    height: 260px;
    font-size: 1.8rem;
    max-width: 100% !important;   /* ✅ override desktop rule */
    width: 100%;                  /* ✅ ensure full width */
  }

  /* Stack banners vertically on mobile */
  .banner-row {
    flex-direction: column;
    gap: 1.2em;
    width: 100%;
  }

  /* Mobile-specific images */
  .research-banner {
    background-image: url('/assets/images/research_banner_mobile.png');
    background-size: cover;
    background-position: center;
  }

  .analytics-banner {
    background-image: url('/assets/images/analytics_banner_mobile.png');
    background-size: cover;
    background-position: center;
  }
}



  /* ==== PROJECT CARDS ===== */
  .project-card {
    display: flex;
    gap: 1.5em;
    align-items: center;
    margin-bottom: 2em;
    padding: 10px;
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

  /* Responsive layout */
  @media (max-width: 750px) {
    .project-card {
      flex-direction: column;
      text-align: center;
    }
    .project-card img {
      width: 90% !important;
    }
  }

</style>

<!-- ===== JAVASCRIPT (toggle functionality) ===== -->
<script>
  function toggleSection(id) {
    const section = document.getElementById(id);
    const isVisible = section.style.display === 'block';
    document.querySelectorAll('.project-section').forEach(s => s.style.display = 'none');
    if (!isVisible) section.style.display = 'block';
    window.scrollTo({ top: section.offsetTop - 100, behavior: 'smooth' });
  }

  // open Analytics by default
  window.addEventListener('DOMContentLoaded', () => {
    document.getElementById('analytics-projects').style.display = 'block';
  });
</script>

<!-- ===== CATEGORY HEADERS (SIDE BY SIDE) ===== -->

<div class="banner-row">
  <div class="section-header research-banner" onclick="toggleSection('research-projects')">
    Research
  </div>

  <div class="section-header analytics-banner" onclick="toggleSection('analytics-projects')">
    Applied Analytics
  </div>
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
        A BI-approach to analyzing customer segments and growth analysis <br>
        <a href="/projects/ecommerce_customer_analysis/">Read more →</a>
      </span>
    </div>
  </div>

  <div class="divider"></div>

  <div class="project-card">
    <a href="/projects/ecommerce_data_pipeline/">
      <img src="/assets/images/dataprocessing scheme no text transparent.png" style="width: 350px; height: auto;">
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
        <a href="/projects/Diptera_Tableau_dashboard/">Interactive Data Visualization using <em>Tableau</em></a>
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
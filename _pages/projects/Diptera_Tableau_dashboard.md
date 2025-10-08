---
permalink: /projects/Diptera_Tableau_dashboard/
title: " "
---
<!-- leave title:" " and we make the title ourself below -->

<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>

<!-- title of the project -->
<div style="font-size: 1.3em; font-weight: bold; margin-top: 2em; margin-bottom: 0.2em;">
  Interactive Data Visualization using <em>Tableau</em>
</div>

<div style="color:#D0D0D0; font-size:0.9em; line-height:1.6;">
  <p>
    I built this Tableau dashboard using insect flight data collected during my postdoctoral research. 
    The goal was to translate a complex, research-grade dataset into an interactive, accessible format. 
    In the process, I learned how to design and communicate data insights using <em>Tableau</em>.
  </p>
  <p>
    My dataset describes wingbeat kinematics of flying insects, which is inherently complex and multidimensional. 
    By making it interactive, I could enable exploration of the data across different subsets (in this case, various insect lineages), 
    while also providing intuitive descriptions of the wing angle parameters that were measured and how these parameters vary across species.
  </p>
</div>

<!-- show the dashboard -->
<div class="tableauPlaceholder" id="vizInsectFlight" style="width:100%; max-width:1200px; margin:auto;">
  <noscript>
    <a href="https://public.tableau.com/views/Doallfliesflythesame/Dashboard1">
      <img alt="Dashboard 1" 
           src="https://public.tableau.com/static/images/Do/Doallfliesflythesame/Dashboard1/1.png" 
           style="border:none;" />
    </a>
  </noscript>
  <object class="tableauViz" style="display:none;">
    <param name="host_url" value="https%3A%2F%2Fpublic.tableau.com%2F"/>
    <param name="embed_code_version" value="3"/>
    <param name="site_root" value=""/>
    <param name="name" value="Doallfliesflythesame/Dashboard1"/>
    <param name="tabs" value="no"/>
    <param name="toolbar" value="yes"/>
    <param name="display_static_image" value="yes"/>
    <param name="display_spinner" value="yes"/>
    <param name="display_overlay" value="yes"/>
    <param name="display_count" value="yes"/>
    <param name="language" value="en-US"/>
  </object>
</div>

<script type="text/javascript">
  var divElement = document.getElementById('vizInsectFlight');
  var vizElement = divElement.getElementsByTagName('object')[0];
  vizElement.style.width = '100%';
  vizElement.style.height = (divElement.offsetWidth * 0.65) + 'px';
  var scriptElement = document.createElement('script');
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
  vizElement.parentNode.insertBefore(scriptElement, vizElement);
</script>

<!-- link to Tableau Public -->
<div style="text-align:center; margin-top: 0.8em;">
  <a href="https://public.tableau.com/views/Doallfliesflythesame/Dashboard1"
     target="_blank"
     style="color:#a0a0a0; font-size:0.9em; text-decoration:none;">
    Open in Tableau Public
  </a>
</div>



## From Static Figures to Interactive Dashboards

<div style="color:#D0D0D0; font-size:0.9em; line-height:1.6;">
  <p>
    In my research work, I typically handle data using programming environments like R, where I generate figures and statistical analyses directly through code. Those figures are designed for publication. They are static, highly precise, and optimized for readers with specialized scientific knowledge. In academia, the challenge is to condense a complex dataset into a single static figure that conveys the key message without overwhelming detail.
  </p>
  <p>
    However, in the applied world of data analytics and business intelligence, the goal is different. Data must often be communicated to audiences with diverse backgrounds, from domain experts to decision-makers without technical expertise. Interactive dashboards provide a powerful way to achieve this: they invite exploration, allowing users to view the same dataset through multiple lenses and focus on the aspects most relevant to their needs.
  </p>
</div>







<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>

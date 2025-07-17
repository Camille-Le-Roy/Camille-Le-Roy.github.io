---
permalink: /projects/wing_heatmap_generator/
title: " "
---
<!-- leave title:" " and we make the title ourself below -->

<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>

<!-- title of the project -->
<div style="font-size: 1.3em; font-weight: bold; margin-top: 2em; margin-bottom: 0.2em;">
  Wing Damage Heatmap Generator
</div>

<span style="color:#D0D0D0; font-size: 0.9em">
A custom R pipeline that generates spatial heatmaps of wing damage from insect wing image data to visualize spatial location of wing damage.
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em;">
  <img src="/assets/images/figure wing damage heatmap.png" alt=" " style="width: 100%; max-height: 300px; object-fit: cover; border-radius: 10px;">
</div>

## Motivation

<span style="color:#D0D0D0; font-size: 0.9em">
When investigating the effect of wing damage on butterfly flight performance, I began to wonder how to not only quantify the extent of damage (e.g., percentage of missing wing area), but also capture its spatial distribution across the wing surface.
</span>



## How It Works

<span style="color:#D0D0D0; font-size: 0.9em">
I superimposed standardized images of the wings from wild specimens using EBImage R package. This allowed counting the missing area at the pixel scale. The heat map is then built from a matrix summing the occurrences of missing pixels, and plotted with autoimage R package.
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em;">
  <img src="/assets/images/figure wing damage heatmap pixels.png" alt=" " style="width: 100%; max-height: 300px; object-fit: cover; border-radius: 10px;">
</div>

<span style="color:#D0D0D0; font-size: 0.9em">
Using the mean shape of intact wings as a template (first image), I superimposed damaged wings on the intact one by fitting the corresponding undamaged wing outlines (second and third image). After each superimposition, missing wing area is counted at the pixel scale. The pixel matrix shown here is at very low resolution for the sake of simplicity. Note that the natural shape variation between individuals (i.e. not due to wing
damage) is eliminated in the process to match the intact template.
</span>

## Code

<div style="margin-top: 1.5em; font-size: 0.9em; color: #D0D0D0;">
  <span>
    The code is freely available on 
    <i class="fab fa-github" style="color:#fff;"></i>
    <a href="https://github.com/Camille-Le-Roy/wing_damage_heatmap_generator.git" 
       target="_blank" 
       style="color: #6CC644; text-decoration: none; font-weight: bold;">
      GitHub
    </a>.
  </span>
</div>


## Usage examples

<div style="font-size: 0.95em; color: #D0D0D0; line-height: 1.6;">
  <p>
    Check out the use of <strong>Wing Damage Heatmap Generator</strong> in my paper published in the 
    <a href="https://journals.biologists.com/jeb/article/222/16/jeb204057/223419/Effects-of-natural-wing-damage-on-flight" 
       target="_blank" 
       style="color: #6CC644; text-decoration: none; font-weight: bold;">
      Journal of Experimental Biology
    </a>.
  </p>
  <p>
    See another example in this study on the evolution of butterfly wing tails, published in the 
    <a href="https://royalsocietypublishing.org/doi/full/10.1098/rspb.2022.0562" 
       target="_blank" 
       style="color: #6CC644; text-decoration: none; font-weight: bold;">
      Proceedings of the Royal Society B
    </a>.
  </p>
</div>


<div style="margin-top: 1.5em; margin-bottom: 1.5em;">
  <img src="/assets/images/wing damage heatmap Ariane Chotard example.png" alt=" " style="width: 30%; border-radius: 10px;">
</div>

<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>
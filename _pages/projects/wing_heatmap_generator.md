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
 I built a custom R pipeline that generates spatial heatmaps of wing damage from insect wing image data to visualize spatial location of wing damage.
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em;">
  <img src="/assets/images/figure wing damage heatmap.png" alt=" " style="width: 100%; max-height: 300px; object-fit: cover; border-radius: 10px;">
</div>

## Motivation

<span style="color:#D0D0D0; font-size: 0.9em">
While investigating the effect of wing damage on butterfly flight performance during my PhD, I aimed at quantifying not only the extent of damage (e.g., percentage of missing wing area), but also its spatial distribution across the wing surface.
</span>



## How It Works

<span style="color:#D0D0D0; font-size: 0.9em">
I superimposed standardized images of the wings from wild specimens using EBImage R package. This allowed counting the missing area at the pixel scale. The heatmap is then built from a matrix summing the occurrences of missing pixels, and plotted with autoimage R package.
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em;">
  <img src="/assets/images/figure wing damage heatmap pixels.png" alt=" " style="width: 100%; max-height: 300px; object-fit: cover; border-radius: 10px;">
</div>

<span style="color:#D0D0D0; font-size: 0.9em">
The pixel matrix shown here is at very low resolution for the sake of simplicity. Note that the natural shape variation between individuals (i.e. not due to wing
damage) is eliminated in the process to match the intact template.
</span>

## Code

<div style="margin-top: 1.5em; font-size: 0.9em; color: #D0D0D0;">
  <span>
    This tool is implemented entirely in R and is openly available on 
    <i class="fab fa-github" style="color:#fff;"></i>
    <a href="https://github.com/Camille-Le-Roy/wing_damage_heatmap_generator.git" 
       target="_blank" 
       style="color: #3B82F6; text-decoration: none; font-weight: bold;">
      GitHub
    </a>.
  </span>
</div>


## How It's Been Used

<!-- First example with embedded link -->
<div style="display: flex; font-size: 0.9em; align-items: center; gap: 1.5em; margin-top: 1.5em; max-width: 900px; margin-bottom: 1.5em; color: #D0D0D0;">
  <p style="margin: 0;">
    Check out the use of <strong>Wing Damage Heatmap Generator</strong> in my research article published in the 
    <a href="https://journals.biologists.com/jeb/article/222/16/jeb204057/223419/Effects-of-natural-wing-damage-on-flight" 
       target="_blank" 
       style="color: #3B82F6; text-decoration: none;">
      Journal of Experimental Biology
    </a>.
  </p>
  <a href="https://journals.biologists.com/jeb/article/222/16/jeb204057/223419/Effects-of-natural-wing-damage-on-flight" target="_blank" style="margin-left: auto;">
    <img src="/assets/images/cover JEB.png" 
         style="border-radius: 10px; width: 230px; object-fit: contain; display: block;">
  </a>
</div>

<!-- Second example with embedded link -->
<div style="display: flex; font-size: 0.9em; align-items: center; gap: 1.5em; margin-top: 1.5em; max-width: 900px; margin-bottom: 1.5em; color: #D0D0D0;">
  <p style="margin: 0;">
    Another interesting example is this study on the evolution of butterfly wing tails by Ariane Chotard, published in the 
    <a href="https://royalsocietypublishing.org/doi/full/10.1098/rspb.2022.0562" 
       target="_blank" 
       style="color: #3B82F6; text-decoration: none;">
      Proceedings of the Royal Society B
    </a>.
  </p>
  <a href="https://royalsocietypublishing.org/doi/full/10.1098/rspb.2022.0562" target="_blank" style="margin-left: auto;">
    <img src="/assets/images/royal society Ariane cover.png" 
         style="border-radius: 10px; width: 265px; object-fit: contain; display: block;">
  </a>
</div>






<!--
<div style="margin-top: 1.5em; margin-bottom: 1.5em;">
  <img src="/assets/images/wing damage heatmap Ariane Chotard example.png" alt=" " style="width: 30%; border-radius: 10px;">
</div>
-->

<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>

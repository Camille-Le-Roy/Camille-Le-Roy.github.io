---
permalink: /projects/3D_reconstruction/
title: " "
---
<!-- leave title:" " and we make the title ourself below -->

<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>

<!-- title of the project -->
<div style="font-size: 1.7em; font-weight: bold; margin-top: 2em; margin-bottom: 0.2em;">
  Quantifying 3D Motion
</div>

<span style="color:#D0D0D0; font-size: 0.9em">
I studied how flying insects move through the air, not just where they go, but exactly how their wings and bodies behave in three dimensions. Using high-speed cameras and 3D reconstruction softwares, I’ve analyzed the flight of butterflies, flies, and bumblebees, both in the lab and in natural environments.
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em;text-align: center;">
  <img src="/assets/images/3D reconstruction hoverfly - climb - glide no description.gif" alt=" " style="border-radius: 10px; width: 100%; object-fit: contain; margin-top: 0.25em;">
</div>

<span style="color:#D0D0D0; font-size: 0.9em">
  Below, I present the key steps of the workflow behind 3D reconstruction, using the quantification of <em>Morpho</em> butterfly flight as an example project.
</span>



## Recording Free-Flying Butterflies

<div style="display: flex; align-items: center; gap: 1.5em; margin-top: 1.5em; max-width: 900px; margin-bottom: 1.5em;">
  <span style="color:#D0D0D0; font-size: 0.9em; line-height: 1.5; flex: 1;">
    To study butterfly flight, I built a "insect flight studio” in the middle of the Amazon rainforest. It was a 9‑meter long outdoor tunnel, where wild butterflies could fly freely, equipped it with a stereoscopic motion capture system: three synchronized high-speed cameras filming at 240 frames per second.
  </span>
  <img src="/assets/images/flight cage tarapoto.png" style="border-radius: 10px; width: 32%; object-fit: contain; margin-top: 0.25em;">
</div>

<span style="color:#D0D0D0; font-size: 0.9em">
Here is an example of the flight trajectory of a <em>Morpho</em> butterfly filmed from both a side and a top view. 
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em;text-align: center;">
  <img src="/assets/images/side and top view menelaus flight GIF.gif" alt=" " style="border-radius: 10px; width: 65%; object-fit: contain; margin-top: 0.25em;">
</div>

<span style="color:#D0D0D0; font-size: 0.9em">
Three-dimensional reconstruction works by filming the same scene from multiple viewpoints and then combining those views. The more viewpoints used, the more precise the reconstruction becomes.
</span>

## From Video to 3D Motion

<span style="color:#D0D0D0; font-size: 0.9em">
A critical step in obtaining 3D information from multiple 2D videos is the calibration. Before recording any flight, the three high-speed cameras need to be accurately calibrated so that even a tiny insect’s wing, moving faster than the human eye can see, appears in exactly the right 3D place for each frame.
<br><br>
To achieve this, I used a calibration wand, moving it throughout the recording area much like a majorette twirling a baton. The extremities of the wand were tracked in each camera view to capture the spatial positions of a known-length object (tracking is shown in only one of the views, below). While other calibration devices can also be used, the wand method is highly adaptable to virtually any space.
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em;text-align: center;">
  <img src="/assets/images/wand calibration large cage GIF.gif" alt=" " style="border-radius: 10px; width: 80%; object-fit: contain; margin-top: 0.25em;">
</div>

<span style="color:#D0D0D0; font-size: 0.9em">
  Using a method called 
  <a href="http://www.kwon3d.com/theory/dlt/dlt.html" target="_blank" style="color:#E0E0E0;">Direct Linear Transformation (DLT)</a>
  along with the recorded wand movements, 2D pixel coordinates can be converted into 3D positions for any object passing through the calibrated space.<br><br>
  Here is the reconstructed flight trajectory for the flight sequence shown earlier.
</span>

<div style="margin-top: 1.5em; margin-bottom: 1.5em;text-align: center;">
  <img src="/assets/images/example reconstructed trajectory.png" alt=" " style="border-radius: 10px; width: 70%; object-fit: contain; margin-top: 0.25em;">
</div>


## Extracting Meaningful Flight Metrics

<span style="color:#D0D0D0; font-size: 0.9em;">
  Once the 3D flight paths were reconstructed, I processed them to turn raw coordinates into interpretable performance and behavioral metrics. 
  For example, I could investigate difference in flight behavior among species using measures of sinuosity, flight speed, acceleration, or the average flight height. 
  I also evaluated critical performance metrics such as gliding efficiency by computing the glide angle during gliding flight phases.
  <br><br>
  <span>
    The data processing and analysis pipeline is implemented in R and openly available on
    <i class="fab fa-github" style="color:#fff;"></i>
    <a href="https://github.com/Camille-Le-Roy/flight_data_analysis" 
       target="_blank" 
       style="color: #3B82F6; text-decoration: none; font-weight: bold;">
      GitHub
    </a>.
  </span>
</span>



## Softwares

<span style="color:#D0D0D0; font-size: 0.9em;">
  <ul style="list-style-type: disc; padding-left: 50px; margin: 0; color:#D0D0D0; font-size: 0.9em;">
    <li style="margin-bottom: 8px;">
      <strong><a href="https://biomech.web.unc.edu/dltdv/" style="color:#3B82F6; text-decoration: none; font-weight: bold">DLTdv</a>:</strong>
      A MATLAB-based digitizing tool, designed specifically for 3D reconstruction.
    </li>
    <li style="margin-bottom: 8px;">
      <strong><a href="https://biomech.web.unc.edu/wand-calibration-tools/" style="color:#3B82F6; text-decoration: none; font-weight: bold">easyWand</a>:</strong>
      A companion tool to DLTdv for calibrating camera setups using the wand method.
    </li>
    <li>
      <strong><a href="https://deeplabcut.github.io/DeepLabCut/README.html" style="color:#3B82F6; text-decoration: none; font-weight: bold">DeepLabCut</a>:</strong>
      A Python library for pose estimation, allowing you to fine-tune deep neural networks for automatic tracking of your object of interest.
    </li>
  </ul>


## Applications

<span style="color:#D0D0D0; font-size: 0.9em">
 I've used three-dimensional reconstruction approaches to investigate insect flight in diverse contexts, from examining how wing damage affects performance, to studying how microhabitat specialization shapes flight behavior, and even uncovering the dynamics of sexual flight interactions. You can find more about these studies on my <a href="/research/" target="_blank" style="color:#3B82F6; text-decoration: none; font-weight: bold">Research page</a>.
</span>



<p style="font-size: 0.9em; margin-top: 2em;">
  <a href="/projects/#projects" style="color: #AAA;">← Back to Projects Overview</a>
</p>

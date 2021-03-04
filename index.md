# Emma's Endeavours

A little look into a few of the projects I've toyed around with.

## Billboarded Planets (2020, February)

Combining raymarching with impostors, sampling fractal coherent noise across a signed distance field sphere.

<video width="640" controls>
  <source type="video/webm" src="/files/billboarded-planets.webm">
</video>

Every single dot on the (regrettably) grey background is another fully detailed planet. No level of detail lowering happens, everything is handled in the shader.

Each pixel only evaluates for the planet or planets it covers, so performance is directly tied to how many pixels are occupied by planets.



## Sketch Shader (2019, July)

Going for a hand-drawn look, I wrote a shader to apply a screen-space sketched texture to shadows and shading, blended based on light attenuation.

<video width="640" controls>
	<source type="video/webm" src="/files/sketch-shader.webm">
</video>

Aesthetically, the shader works even better if the pattern is randomly rotated at 90-degree angles, 4-12 times per second.

The outline is a post-processing effect taking into account colour changes and depth changes between pixels.

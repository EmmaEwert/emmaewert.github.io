# Emma's Endeavours

A little look into a few of the projects I've toyed around with.

## Billboard Planets (2020, February)

Combining raymarching with impostors, sampling fractal coherent noise across a signed distance field sphere.

<video width="640" controls>
  <source type="video/webm" src="/files/billboard-planets.webm">
</video>

Every single dot on the (regrettably) grey background is another fully detailed planet. No level of detail lowering happens, everything is handled in the shader.

Each pixel only evaluates for the planet or planets it covers, so performance is directly tied to how many pixels are occupied by planets.

A dither post-processing effect keeps the colour count at four, and dithers those to make up for other colours.



## Sketch Shader (2019, July)

Going for a sketchbook doodle look, I wrote a shader to apply a screen-space sketched texture to shadows and shading, blended based on light attenuation.

<video width="640" controls>
	<source type="video/webm" src="/files/sketch-shader.webm">
</video>

Aesthetically, the shader works even better if the pattern is randomly rotated at 90-degree angles, 4-12 times per second.

The outline is an older post-processing effect of mine, taking into account colour changes and depth changes between pixels.



## Art Shader (2019, May)

After creating a standard outline post-processing effect, I wanted to see how much I could make it color outside the lines, so to speak.

<video width="640" controls>
	<source type="video/webm" src="/files/art-shader.webm">
</video>

The end result is a shader that makes every frame look somewhat like it was drawn with watercolours.



## Sable Shader (2019, April)

Inspired by the art style of the game [Sable](https://www.shed-works.co.uk/), I wanted to implement a decent deferred cel-shaded surface shader, and an outline post-process shader based on depth *and* colour.

<video width="640" controls>
	<source type="video/webm" src="files/sable-shader.webm">
</video>

Shadows, lights, and otherwise sharp changes in contrast - like pebbles on the ground and particle effects - all cause the edge detector to emit outlines, configurable in threshold, width, and colour.
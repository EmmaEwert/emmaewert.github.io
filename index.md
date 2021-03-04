# Emma's Endeavours

## Billboarded Planets (2020)

Combining raymarching with impostors, sampling fractal coherent noise across a signed distance field sphere.

<video width="638" height="638" controls>
  <source type="video/webm" src="/files/billboarded-planets.webm">
</video>

Every single dot on the (regrettably) grey background is another fully detailed planet. No level of detail lowering happens, everything is handled in the shader.

Each pixel only evaluates for the planet or planets it covers, so performance is directly tied to how many pixels are occupied by planets.

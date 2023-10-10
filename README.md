# Procedural Jellyfish

## Project Overview
A procedural jellyfish using Houdini.

![]()

## Components
This Jellyfish consists of the bell, arms, venins, tentacles, and organs

### Bell
[Jellyfish Bell Setup Video](https://www.youtube.com/watch?v=J3X8BB0yNRE)

### Arms
[Jellyfish Arms Setup Video](https://www.youtube.com/watch?v=A_oNXqx8XH4)

### Veins
For the Venins, I firstly applied the *Remesh* node to triangulate the bell surface and then used the *GroupExpression* node to sellect the **start points** and the **end points** for *FindShortestPath* node. Sebsequently, I applied the *Resample* node, *Smooth* node and *PolyWire* node. 

## Organs
For Organs, I used the spline to model its skeleton and then used *Duplicate* node. After that, I added a *Sweep* node to make it polygon. 

## Tentacles
For Tentacles, I used *GroupExpression* to extract some points at the buttom of the bell. Subsequently, I used a *Line* and a *CopyToPoint* node to make multiple tentacles. Finally, I applied hair simulation to tentacles to make the simulation better. 

## Third party credit
- [Jellyfish Bell Setup Video](https://www.youtube.com/watch?v=J3X8BB0yNRE)
- [Jellyfish Arms Setup Video](https://www.youtube.com/watch?v=A_oNXqx8XH4)
- [Underwater Environment](https://www.deviantart.com/namtaar/art/Underwater-Hdri-805776729?ga_submit_new=10%3A1563205557)
- [Backgournd Image](https://4kwallpapers.com/photography/underwater-sun-rays-ocean-hawaii-5k-8k-8301.html)

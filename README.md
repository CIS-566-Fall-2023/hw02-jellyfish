# Procedural Jellyfish

![](https://github.com/Diana-ou/hw01-fireball/blob/master/calcifer%20gif.gif)

[Live Demo Link] (https://diana-ou.github.io/hw01-fireball/)

## Objective
- Learn how to use Houdini for the first time

## Inspiration
I was inspired by plush toys, and wanted to try making the jelly plush-style!

## Implementation details

The Bell:
* Revolved a curve
* Carved out patches using voronoi noise
* Added revolved seams to voronoi edges 

The Veins: 
* Used shortest path to calculate veins on sides of jelly
* Revolved veins

The Organs: 
* Copied extruded curve 4 times

The Tentacles:
* Deformed a plane using sine curves
* Scattered smaller tentacles to points
* Simulated using vellum hair simulation, etc. 
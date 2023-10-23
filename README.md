# Procedural Jellyfish

[see the HIP file here!] (https://drive.google.com/file/d/1OJE3G5J6TwUa0AFRf9qrRIE1JXpcrs3Z/view?usp=sharing)
[Video Demo](https://drive.google.com/file/d/1HzRkZeabLmmwkA_GAhiIFzLpTP8KAu1-/view?usp=sharing)

## Objective
- Learn basics on how to use Houdini for the first time

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

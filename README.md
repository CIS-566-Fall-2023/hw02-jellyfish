# Procedural Jellyfish

## Project Overview

In this project, I created a procedural jellyfish using Houdini, using procedural modeling and simulation. 

![Jelly Fish Demo](https://www.youtube.com/watch?v=mr_SnPgcRcI)

---

## Bell
First, I made the Bell of the jellyfish. I began with a line, bent it to the desired shape, and revolved it around the y-axis to create a parabolic shape. Next, I used the mountain node to add some noise to create a much less uniform shape, and extruded to get the final bell. 

![Bell](https://github.com/kyraSclark/hw02-jellyfish/assets/60115638/7cc5ef80-9230-4ae2-aa4d-2172aa9b68a3)

## Veins
Next, I created the veins across the jellyfish's bell. This required that I remesh the bell in order to create more non-uniform (non-square) points around the shape. I started by using the group expression node to create two groups of points: start points which are located in the top region of the bell with some random change, and end points which are located in the lower region of the bell. Then, I used the Find Shortest Path node to create the lines that connect the start points to the end points. Next, I swept over the lines to give a round tubular shape. 

![Veins](https://github.com/kyraSclark/hw02-jellyfish/assets/60115638/14c8ba49-d726-4b7e-9212-9cc8436ed4c4)

## Puckering Bumps (extra credit)
For a more interesting shape, I added some bumps to the bell to give the shape some puckering. I began with a transformed sphere to get the shape that I wanted, and rotated it such that the normal aligned. Then, I used the remeshed bell again to collect a group of random points that existed within a bounding box around the bell, exluding the flairing bottom of the bell. Then, I copied the sphere shape to the grouped points on the bell. 

![Bumps](https://github.com/kyraSclark/hw02-jellyfish/assets/60115638/d22c826f-025e-4a5c-bf70-d147238a47c9)

## Organs
For the organs, I made a curve that matched the desired shape, and resampled it to create a better curve. I used the Sweep node to give it an extruded shape, and then copied the shape around the middle of the bell. Finally, I added some noise to change each organ's size and shape slightly. 

![Organs](https://github.com/kyraSclark/hw02-jellyfish/assets/60115638/39dc2175-6b5c-4337-92c9-239ca8ab0c4f)

## Arms
For the arms of the jellyfish, I started with a grid and added ruffles to it. I needed to twist it and remesh it to get the shape that I wanted. Then, I used a group node to pin the tops of the arms to the bell, but the rest of the arm was free to move around. Then, I transformed it to the size I wanted and copied it around the center of the bell. Finally, I used the vellum constraints and the vellum solvers to give the arms simulated spring-liek qualities that would bounce and move in a low-gravity environment as the bell moved up and down. 

![Arms](https://github.com/kyraSclark/hw02-jellyfish/assets/60115638/a7b31bef-5a81-454c-adf1-3c9a4e66de2e)

## Tentacles
Finally, for the tentacles, I started with a simple line. Then I selected points around the base edge of the bell, and copied the line to those points. Similarly to the arms, I used a group node to pin the tops of the tentacles to the base of the bell. Then, I used the vellum hair and vellum solver to simulate the movement of hair. To polish, I cleaned up the lines, resampled them, and swept across to give them shape. 

![Tentacles](https://github.com/kyraSclark/hw02-jellyfish/assets/60115638/0718a010-cd58-49d5-af3f-cf6f9195f73c)

## Polish and Finish 
To finish the project, I added a material to all the different parts to give it a transparent or pink color. Then, I animated the model. I used a null node, that I called the Controller to house the keyframes for the jellyfish. I copied selected properties of the fish that I wanted to animate. In this project, I animated the jellyfish's Y Position to make it move up and down, controlled the bend of the bell as well as the bend of the tip of the bell, and I animated the noise of the organs to make them move and fluctuate slightly. Finally, I merges all the pieces together. 

![Final Merge](https://github.com/kyraSclark/hw02-jellyfish/assets/60115638/498fc3cc-83ac-4cd1-8541-8db57fe7c55f)

# Procedural Jellyfish

Kisha Yan

## Final Video
![Jellyfish](https://github.com/kishayan02/hw02-jellyfish/assets/97934823/6f54d71d-5761-4e4b-a0c6-130e4f8d501e)

## Bell 
![image](https://github.com/kishayan02/hw02-jellyfish/assets/97934823/b5b046a3-6512-4a03-b8d5-32386cc129e1)

For the bell, I created a line and bent it twice, then used the revolve node to create the shape of the bell. I used the mountain node to create a bit of noise and irregularity on the surface, as well as polyextrude to give the primitive some thickness.

## Arms
![image](https://github.com/kishayan02/hw02-jellyfish/assets/97934823/4fa7a986-2f14-464b-8d69-ad76574aab42)

To create the arms of the jellyfish, I deformed a grid using twist, an attributeWrangler, and remeshing. Then, after creating 4 more copies of this grid, I pinned the arms to the bottom of the bell and used cloth and pin vellumconstraints, as well as vellumsolver, to create the movement. 

## Veins
![image](https://github.com/kishayan02/hw02-jellyfish/assets/97934823/f3c6a43b-7ace-4d3c-b6fc-1b8b5f0b1bd2)

To make the veins, I used the bell of the jellyfish and remeshed it into triangles. Then, I sorted by y-value and created two groups, one for startpoints and one for endpoints, through randomly sampling points using groupexpression nodes. I used the findshortestpath node, followed by resampling, fusing, and smoothing to ensure the smoothness of the veins, as well as a sweep to give the veins some volume. I made sure to timeshift after creating groups and after the sweep to prevent the veins from changing shape in every frame. I made the veins move with the  bell using a pointdeform node. 

## Organs
![image](https://github.com/kishayan02/hw02-jellyfish/assets/97934823/fae9747c-417c-4e84-9652-d77c9b8a7f66)

To create the organs, I started with a sphere primitive, elongated it along the z-axis, and then bent it to create the horseshoe shape. Then, I used the ripple node to deform and add some noise to the organs. I tilted the shape so that the organs would appear to fan out/downwards from the center of the jellyfish, and finally, I created 3 copies of the original shape. I also made sure that the organs moved with the jellyfish bell using a pointdeform node. 

## Tentacles
![image](https://github.com/kishayan02/hw02-jellyfish/assets/97934823/2a42451b-4d97-4e78-84f0-b13ea489e5aa)

For the tentacles, I grouped all the points that created the bottom edge of the jellyfish bell. I used this point group, along with a line (volumized with a sweep node), as inputs to the copytopoints node to create the multiple tentacles. Finally, I used vellumhair and vellumsolver to create some movement and dimension, along with pointdeform to sure that the tentacles moved with the bell.

## Extra

For each part of the jellyfish, I added color and opacity to make the jellyfish appear more realistic and to make the organs visible. For the animation of the jellyfish itself, I added y-translation movement, adjustments to the bend of the bell, as well as rotation about the y-axis. Finally, I rendered my jellyfish using the PBR mode in a mantra node, a camera, and an environment light. Thanks :)

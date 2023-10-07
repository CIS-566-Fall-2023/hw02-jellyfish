# Procedural Jellyfish

## Result

https://github.com/IwakuraRein/CIS-566-hw02-jellyfish/assets/28486541/1c8e53d7-9d2c-4722-86b6-6cb9e25fe44d

## Bell, Arms, and Veins

I followed the tutorials to create the bell, arms, and veins.

## Tentacles

I first created a line node and used a resample node to increase its tessellation. Then I created a point group by selecting the edges of the bell and used a copy-to-point node to layout the tentacles. 

I used the vellum solver to perform hair simulation on the tentacles. Then I used a sweep node to create the meshes along the tentacles.

## Organs

I first created a torus and used the clip node to halve it. Then I used the mountain node to add some noise to the surface and the poly extrude node to create the mesh.

I used a copy node to make another 3 organs and used the point deform node to make them follow the animation of the bell.

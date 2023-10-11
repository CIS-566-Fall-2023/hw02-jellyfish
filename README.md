# Procedural Jellyfish

![image](https://github.com/RachelDLin/hw02-jellyfish/assets/43388455/a96c8176-874e-4e8f-8a02-205d775c597c)
![Screenshot 2023-10-11 000232](https://github.com/RachelDLin/hw02-jellyfish/assets/43388455/68439d59-62e0-4315-915a-201af41b967e)
![Screenshot 2023-10-11 000221](https://github.com/RachelDLin/hw02-jellyfish/assets/43388455/486e8f96-a1ca-4f95-bf27-cbbafe9c976a)


The bell was created by rotating a curve to sweep out a mesh and extruding it. The arms were created by using noise and twisting to deform a plane. The plane was then extruded and had additional deformation applied to it as a function of time through the cloth vellum constraints node. The veins were created by randomly selecting points from the top and bottom of the bell and finding the shortest paths between them. The organs were created by smoothing a tube that was based on a curve. The organ was then duplicated and rotated by 90 degrees 3 times. The tentacles were formed by duplicating a line around randomly selected points on a torus. A hair simulation was then run on it using the vellumhair node. All of these components were bound to the bell at the appropriate vertices and translated to match the bell's movements. The veins had an additional scale applied to match the shape of the bell. 

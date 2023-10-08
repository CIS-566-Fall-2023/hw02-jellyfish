# Claire Lu Procedural Jellyfish

## Project Overview
For my procedural jellyfish, I decided to create a glowy, shiny gold and white jellyfish.

I started by creating the bell and the arms of the jellyfish. 

I made the bell by using a line node, bending it, and then revolving it to create a hemispherical shape. I then used the mountain node to give it a more organic look, and extruded it to give it some thickness.

For the arms, I started with a rectangular grid, added ruffles to it by adding a noise values to the points based on their location on the grid, and then applied a twist to it. I used a cloth constraint to make it look stretchier and matched it to the animation of the bell by using a point deform node.

<img height="200" alt="Jellyfish Parts" src="https://github.com/ClaireL21/hw02-jellyfish/assets/102630261/c64fd87c-bced-4d15-9eb5-923d9f59035d">

<img height="200" alt="Jellyfish Parts" src="https://github.com/ClaireL21/hw02-jellyfish/assets/102630261/495c70cb-644e-4ad3-b1bc-5f677f6cfc6a">

<img height="200" alt="Jellyfish Parts" src="https://github.com/ClaireL21/hw02-jellyfish/assets/102630261/46f8004c-eb34-400d-9045-2db23012a775">


To create the veins, I used the shortest path node. First, I described a set of points on the jellyfish bell to be the start points and another set of points to be the end points. Calculating the shortest paths from each of the endpoints to a subset of the startpoints gave a nice veiny look that worked well for the jellyfish. The most challenging part about using the shortest path node, though, was getting the animation to run smoothly with the bell. At first, when trying to deform the paths to match the surface of the bell, the shortest path node would recalculate paths and the veins would change. I then tried using a timeshift node to freeze the calculations at the first frame - however, this caused the veins to no longer move with the bell. In the end, I found the solution to be using two timeshifts. The first timeshift is for calculating the shortest paths and creating the veins. Then, the second one references the original bell geometry and deforms the veins points based on that. This allowed the veins to move with the bell without recalculating paths!


<img height="200" alt="Jellyfish Parts" src="https://github.com/ClaireL21/hw02-jellyfish/assets/102630261/478d07cc-1050-4fba-b10e-ac925ca78ff9">

Next, I created the organs. For this, I created a line, used several bends to make it in the shape I wanted, and then gave it thickness and copied it for a total of four pieces. 

<img height="200" alt="Jellyfish Parts" src="https://github.com/ClaireL21/hw02-jellyfish/assets/102630261/2e284b8b-0f7f-4ea1-a062-33d4c5af4000">


Lastly, I created the tentacles. I wanted the tentacles to be attached to the jellyfish along the circumference of the bottom of the bell. I used a torus and a scatter node to create a ring of points from which I could later generate lines. The jellyfish's bell isn't completely circular, though, so the points didn't match up perfectly with the bottom of the node. In order to fix this, I used a ray node to project the points onto the surface of the bell. However, because of the bell's upward-downward animation, the points weren't always projected onto the rim of the bell, so I first deformed the points to move along with the animation of the jellyfish and then used the ray node to project the points. After this, I copied lines to the points to give it more of a tentacle shape, used a hair constraint and vellum solver to help capture the movement of the tentacles, and used a sweep node to give it some thickness.

<img height="200" alt="Jellyfish Parts" src="https://github.com/ClaireL21/hw02-jellyfish/assets/102630261/1aaa3331-5d0e-4f4a-aa4b-46004b3373c9">

<img height="200" alt="Jellyfish Parts" src="https://github.com/ClaireL21/hw02-jellyfish/assets/102630261/d8971adb-294e-49d6-85ea-5d5cec299ed0">


## Video Demo
<video height="500" src="https://github.com/ClaireL21/hw02-jellyfish/assets/102630261/1cf97cc5-831b-4469-b8e6-ed407c43989b">


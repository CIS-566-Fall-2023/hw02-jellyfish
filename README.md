# Procedural Jellyfish
<img width="1000" alt="FinalModel1" src="/assets/final_bottom_view.png">
<img width="1000" alt="FinalModel2" src="/assets/final_top_view.png">

### Animation:

<img width="1000" alt="FinalDemo" src="/assets/final-demo.gif">

## Project Overview
I created a procedural jellyfish using Houdini. The focus of this project is to dig into procedural modeling, as well as some physical simulation. Below is a breakdown of how I implemented the different jellyfish parts using node network.

## Bell
<img width="1000" alt="BellDemo" src="/assets/bell-demo.gif">

[Jellyfish Bell Setup Video](https://www.youtube.com/watch?v=J3X8BB0yNRE)
1. Draw line, so that can LATER revolve around y-axis.
2. Add organic deformation using two Bend nodes: one to control the rim and the other for the central main.
3. Keyframing animation using the timeline bar.


## Bell Arms
<img width="1000" alt="Arms" src="/assets/arms.png">

[Jellyfish Arms Setup Video](https://www.youtube.com/watch?v=A_oNXqx8XH4)

1. Vellum constraint node: pre setup of geometry attributes for cloth simulation
2. Vellum solver node: driver for actual simulation


## Veins
<img width="1000" alt="Veins" src="/assets/veins-v2.png">

Reference: [Dungeon Corridor - Houdini Playground](https://www.youtube.com/watch?v=K6IGdoc77Nk&list=PLWxLLKXNHPFz13s5Obs0CQ1RWW8mBO0XB&index=11)


1. Remesh the jellyfish into triangles (otherwise will end up with very square looking veins).
2. Create two `groupByRange` nodes to select the start points and end points for each tree branch pattern.
3. Use the shortest path node to generate veins.
4. Smooth out the veins for a more organic look. Use resample and fuse nodes before the "smooth" node to ensure continuous closed geometry.
5. Use a sweep node to give the veins width, i.e. use round tube as its cross-section instead of a string.
6. Lastly, stick the veins to the bell's animation using the "Point Deform" node that I used on the arms. 

## Organs
<img width="1000" alt="Organs" src="/assets/organs-basic.png">

1. Draw a Bezier curve, and use sweep node to create a worm-shaped mesh.
2. Rotate and duplicate the base organ.
3. Add variation on the mesh using noise --> the mountian node!


## Tentacles
<img width="1000" alt="Tentacles" src="/assets/tentacles-copytopoints.png">

Reference: [This video](https://www.youtube.com/watch?v=LN4XXaHQkmU) demonstrates how to simulate hairs.

1. Extract the rim points of the bell.
2. Use a copytopoints node to scatter a basic line at some randomly selected points within the group of extracted points.
3. Use vellumconstraints and vellumsolver to simulate hair movement.

### Bloopers
Saggy arms

<img width="1000" alt="SaggyArms" src="/assets/arms-saggy-cloth-simulation.png">

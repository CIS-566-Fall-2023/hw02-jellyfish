# Procedural Jellyfish

## Animated Jellyfish
https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/adea950a-142b-48f8-a575-e4a6310bc4a2

https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/f6f52478-1907-45c3-9ef0-a4b60b971cc9

## Project Overview

<img width="328" alt="Jellyfish" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/8ccc908f-9c73-423d-8449-627cca3e1629">

The jellyfish is made up of five parts: the Bell, the Arms, the Veins, the Organs, and the Tentacles.

<img height="500" alt="Jellyfish Parts" src="/assets/JellyfishParts.png">

## Bell
<img width="304" alt="Bell" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/2d5f1b89-157f-4ae4-bdcc-6c2ff0e6a7a5">

The bell is created using a line as the base, that is then bent into a curve that is revolved to create the general shape of the bell. Finally, noise is adding using a mountain noise to give the bell a more organic look.

## Arms
<img width="361" alt="Arms+Bell" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/a693bff1-245e-4d22-81cf-8e8857add058">

The arms are created using a grid as a base, that is then modified to have ruffles using a VEXpression. The copy node is used to duplicate the one arm. The movement of the arms is based on a cloth simulation done through Vellum Constraints and Vellum Solver nodes. 

<img width="242" alt="Arms" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/b4df5790-c78e-4ccb-b746-1449a0da5a81">

## Veins
<img width="304" alt="Veins+Bell" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/5f9c2de6-e577-4b43-812d-a433d1d265f6">

The veins are created by selecting 2 groups of points from the bell of the jellyfish and then it utilizes these two groups in the Find Shortetst Path node to create the veins. After the shortest paths are created, they are smoothed out using Resample, Fuse, and Smooth nodes. Then the veins are given width using a sweep node. Finally, to ensure that the deformation of the veins matches the bell of the jellyfish a point deform node is utilized.

<img width="284" alt="Veins" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/7f613fc6-0c4d-4bd2-a0c1-fbe4d0c0fceb">

## Organs
<img width="287" alt="Organs+Bell" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/d2e665ef-af7e-4141-b9ea-9bac5b2c6568">

The organs are created by using a tube as the base for one, filling it to add rounded caps, and then bending it to create the general shape of one organ. Noise is then added using a mountain node to make the shape more organic. Afterwards, the copy node is utilized to create 4 organs resulting in something like this:

<img width="288" alt="Organs" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/e0784f75-dae6-4992-a192-50dfd849cb27">

## Tentacles

<img width="323" alt="Tentacles + Bell" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/10b1c1bd-4613-48e3-8d19-72db7561d21d">

The tentacles are created using a line as the base, that is then copied onto the points of the "edge" of the bell. These lines are then simulated as hair using the Vellum Hair and Vellum Solver nodes. The movement of the tentacles is affected by Pop Attract and Pop Force nodes being added to the output force of the Vellum Solver.

<img width="303" alt="Tentacles" src="https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/bd8d2b71-7950-4494-81a6-4dd373d69e77">

## Render
![jellyfishRender1](https://github.com/hansen-yi/hw02-jellyfish/assets/97490525/b57d96fb-598b-4686-b74a-db5e57864866)

## References
- Elyssa Choudini Tutorials
    - [Houdini PLayground](https://youtube.com/playlist?list=PLWxLLKXNHPFz13s5Obs0CQ1RWW8mBO0XB&si=0poQWdqSfBQvE7Qp)
    - [Bell](https://www.youtube.com/watch?v=J3X8BB0yNRE)
    - [Arms](https://www.youtube.com/watch?v=A_oNXqx8XH4)
    - [Exporting Videos](https://www.youtube.com/watch?v=gXtDd1lPDmc)
- [Hair Simulation](https://www.youtube.com/watch?v=LN4XXaHQkmU) 
- Rendering Tutorials
    - [Houdini in 5 Minutes 04](https://www.youtube.com/watch?v=1Ph-7ZpN5oY)
    - [Houdini in 5 Minutes 05](https://www.youtube.com/watch?v=mCQPDf-bupY)

# Procedural Jellyfish - Xiaoxiao(Crystal) Zou

## Project Overview

<video src="./untitled.mov"> </video>
![jellyfish](./untitled.mov)

In this project, I made jellyfish that composed of 5 parts as instructed below. For belly and arms, I followed the videos that are provided. 

For Veins, I used the points select by range with together of sort by y-size in order to select the points I want to pick in order to generate shortest path (tree structure). Then, I resample and fuse the points for the path, then sweep the path with boxs in order to generate some volume. In order to let the vein floating on belly and with some organic shape, I remesh and scale the belly before doing selection. 

For Organs, I just used bezier curve (resample with points on curve ) with together of sweep with sphere in order to generate shape (with some noise in scale with sweeping). 

For Tentacles, I first generate some points at bottom of belly, then followed from hair instruction to generate some hairs. I still add small gravity since tentacles have to fall down. Then, I sweep the lines with boxes to generate mesh. 

<img height="500" alt="Jellyfish Parts" src="./assets/JellyfishParts.png">

[Jellyfish Bell Setup Video](https://www.youtube.com/watch?v=J3X8BB0yNRE)

[Jellyfish Arms Setup Video](https://www.youtube.com/watch?v=A_oNXqx8XH4)

[Hair](https://www.youtube.com/watch?v=LN4XXaHQkmU)

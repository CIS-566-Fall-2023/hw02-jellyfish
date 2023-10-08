# Procedural Jellyfish

The goal of the project was to create an animated jellyfish using procedural modeling and simulation in Houdini. 
The jellyfish contains 5 main parts: the bell, the arms, inner organs, veins, and tentacles.

## Bell
To create the bell, I first used a _line node_ and _3 bend nodes_ to get the desired shape and controls for animating later on. After revolving the line around the Y-axis, I added noise using a _mountain node_ to create a more organic shape. Finally, I used 2 _polyextrude nodes_ and a _subdivide node_ to create a scalloped/ridged edge on the bottom of the bell.

## Arms
For the arms, I closely followed [Elyssa Chou's tutorial:](https://www.youtube.com/watch?v=A_oNXqx8XH4). I used VEX to apply a ruffled effect to the arms, twisted the arms about the Y-axis, pinned the top points of the arms to the centroid of the bell, and finally used Vellum Cloth simulation to create an effect of the arms drifting through water.

## Organs
To create the inner organs, I first modified a _line_ using the _bend node_ to get the desired shape. I then used a _polywire node_ to create thickness and experimented with noise values/patterns in the _mountain node_ to create an organic shape. After creating four organs, they were pinned to a fixed location within the bell for animating.

## Veins

## Tentacles


## Extra Credit
- added scalloped edges to the bell
- WIP: created a background with procedurally generated seaweed
- WIP: created a render of the jellyfish
    - A description of your project
    - A video of your animated jellyfish ([video](https://www.youtube.com/watch?v=gXtDd1lPDmc) of how to save a video of your viewport out of Houdini)
- Create a pull request to this repository
- Submit your Houdini file to Canvas along with a link to your pull request
(Don't upload your houdini files to github -- it's a pain to upload big/binary files. Just canvas is fine!)

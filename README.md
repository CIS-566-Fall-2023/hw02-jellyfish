# Procedural Jellyfish

## Project Overview

Houdini procedural jellyfish with 5 main components, animated with keyframes and cloth simulation.

![jelly](https://github.com/wc41/hw02-jellyfish/assets/97757188/27802cc2-00cd-4018-bd94-2a4c85ceec68)

Better material image render:

![image](https://github.com/wc41/hw02-jellyfish/assets/97757188/bb30fabc-7178-43b6-bb98-4316f9777eb4)


## Bell

![image](https://github.com/wc41/hw02-jellyfish/assets/97757188/0fbac468-1200-4ad7-a607-04f4566b3a33)

Created with the help of: [Jellyfish Bell Setup Video](https://www.youtube.com/watch?v=J3X8BB0yNRE)

## Arms

![image](https://github.com/wc41/hw02-jellyfish/assets/97757188/aed02768-5f5c-4d56-858d-4e1963267890)

Created with the help of: [Jellyfish Arms Setup Video](https://www.youtube.com/watch?v=A_oNXqx8XH4)

## Veins

![image](https://github.com/wc41/hw02-jellyfish/assets/97757188/9eb378ed-96ce-48e3-8d20-86dfba8c09a1)

Created by taking a remesh of the bell shape, taking a group of vertices at its top and a group of vertices at its bottom rim, and extracting lines connecting them using the findshortestpath node. These are made more natural by adjusting random vertex picking and a carve node.

## Organs

![image](https://github.com/wc41/hw02-jellyfish/assets/97757188/d670719c-15ca-48db-80f0-2434e5bde11f)

Created by taking a line and bending it, using polywire to give thickness, smoothing ends by converting to vdb and using vdbsmooth then converting back, and using a mountain node for noise. A copy node is used to duplicate the line 4 times.


## Tentacles

![image](https://github.com/wc41/hw02-jellyfish/assets/97757188/448ad411-fa34-416a-a6ba-5f982df60a54)

Created by making a polywired line with mountain node noise and using copytopoints node to attach them to a group of evenly spaced points on the bell's bottom rim. Simulated with cloth and pin-to-target vellum constraints.

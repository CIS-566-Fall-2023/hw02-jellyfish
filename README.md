# Procedural Jellyfish

## Result

Color animation:

![](/colorJellyAnim.gif)

Plain animation

![](/JellyFlipbook.gif)

Static PBR render image
![](/pbrRender.png)

## Desciption
In this project, I create a procedural jellyfish model and its animation using Houdini. It contains five parts: bell, arms, veins, organs ans tentacles. Also, I use some noise to generate the color of each part.

The bell is shaped from revolving a bended line. Arms are shaped from distorted grids, together with cloth simulation nodes.

For veins, I first remash the bell and group the start points and end points seperately, then use the find-shortest-path node to build route between each end points to any start point. Additionally, I freeze the vein shape to frame 1 with time-shift node, to make the path between start points and end points not change along the time. Then I use node-deform to make vein deform with bell.

For organs, I use similar way as the bell. I first bend a line and sweep it in round tube. Then I use mountain node to add some noise on the organ shape and copy it to four points.

And for tentacles, I use hair simulation to make its movement looks alive, with beginnning points of tentacles pinned on bottom of the bell.
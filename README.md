# Procedural Jellyfish Project

Note: I used a late day on this! Also, I do not see a place to submit my Houdini files on Canvas, so I just updated my README and made a PR.

## Procedural Jellyfish Project
In this project, I set out to create a procedural jellyfish using Houdini! I learned so much about procedural graphpics and Houdini through this process and am excited to create more exciting works in the future! I ended up having a lot of technical issues with my computer crashing and Houdini refusing to launch, but hopefully with more practice I'll be able to get through these hurdles faster too :)

The finished product:

<img width="300" alt="Final Jellyfish" src="/assets/Final.mp4">

[Google Drive video link](https://drive.google.com/file/d/1hY8OcFfnATgumvt7NZdxIK_choXAFDTW/view?usp=drive_link)

Now let's dive into how I did it!
My jellyfish has 5 major components:
- Bell
- Arms
- Veins
- Organs
- Tentacles

<img height="500" alt="Jellyfish Parts" src="/assets/JellyfishParts.png">

---

## Bell
The first part I decided to tackle was the bell of the jellyfish. To do this, the first step was to create a line. Then, we use Bend nodes to bend the overall line, and then separately bend the tip to create a curve. After aligning the curve properly with the y-axis, we use a revolve node and adjust the settings to create the bell shape. I added a gradient to my bell using the attribute adjust color node.

## Arms
For the arms, I started out with a grid node and applied a VEX script to use noise and point manipulation to add ruffles. Then, I used the twist node to add a more interesting shape, and some Vellum nodes to add some movement.

## Veins
In order to create the veins for the jellyfish, I used the "Find Shortest Path" node.
I remeshed the jellyfish into triangles to create more organic-looking paths. I also used the resample function for additional smoothing, and the sweep node to add some depth to the veins. Then, I pinned the veins to the bell's animation using the "Point Deform" node similarly to the arms.

## Organs
Next, I created the jellyfish organs by starting with a line, bending, and revolving it around an axis similary to the way I created the Bell. I added a mountain node to create a more lumpy, organic look.


## Tentacles
Next, I created some very fine, hair-like tentacles to float around the perimeter of the Jellyfish. I used a grouping node to select only the bottom rim of the Bell, where I wanted to attach the hairs. I then used the Vellum hair node, and the point deform node (similarly to the Arms) to copy the main animation. I lowered the gravity in the Forces tab of the Vellum Solver to create an underwater effect as well.

## Extra Credit
- I added some lighting and an image background, and attempted to render my final project. However, my computer struggled to finish the render before crashing.
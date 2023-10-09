# Procedural Jellyfish

## Project Overview
In this homework, you'll create a procedural jellyfish using Houdini. This will give you a chance to dig into procedural modeling, as well as some simulation. Here is a breakdown of the different jellyfish parts you'll be putting together:

<img height="500" alt="Jellyfish Parts" src="/assets/JellyfishParts.png">

---

Here are some SideFX docs that you might find helpful:

[Geometry Nodes Documentation](https://www.sidefx.com/docs/houdini/nodes/sop/index.html)

[VEX Documentation](https://www.sidefx.com/docs/houdini/vex/functions/index.html)

## Bell and Arms
Follow along to the videos to create the bell and arms of the jellyfish. Although I provide the values I used to create my jellyfish, you're heavily encouraged to play around and customize the setup to your liking! 

[Jellyfish Bell Setup Video](https://www.youtube.com/watch?v=J3X8BB0yNRE)

[Jellyfish Arms Setup Video](https://www.youtube.com/watch?v=A_oNXqx8XH4)

## Veins
In order to create the veins for the jellyfish, you'll make use of the "Find Shortest Path" node. The Dungeon Corridor example in the Houdini Playground is a helpful reference for using this node. Here is some rough guidance for how to approach making the veins:

Remesh the jellyfish into triangles (otherwise you'll end up with very square looking veins)

<img width="300" alt="Remesh" src="/assets/Remesh.png">

Use the shortest path node to generate veins ([here](https://www.sidefx.com/docs/houdini/nodes/sop/findshortestpath.html) are the docs for the Find Shortest Path node)

<img width="300" alt="ShortestPath" src="/assets/ShortestPath.png">

Smooth out the veins for a more organic look. You might find yourself needing the "resample" and "fuse" nodes in addition to the "smooth" node (and remember, the [docs](https://www.sidefx.com/docs/houdini/nodes/sop/index.html) are a great resource if you're confused about what a node does or how to use it)

<img width="300" alt="ResampleFuseSmooth" src="/assets/ResampleFuseSmooth.png">

Use a "sweep" node to give the veins width

<img width="300" alt="Sweep" src="/assets/Sweep.png">

Lastly, stick the veins to the bell's animation using the "Point Deform" node that we used on the arms. The final result should look something like this:

<img width="300" alt="VeinsGif" src="/assets/VeinsGif.gif">

## Organs
Next, create organs for your jellyfish. You can approach this any way you'd like! The final result should look something like this:

<img width="300" alt="Organs" src="/assets/Organs.png">


## Tentacles
When you're working on Houdini projects in the future, you usually won't be able to find tutorials for exactly what you're trying to do. Instead, you'll need to be able to take semi-related tutorials and apply the relevant techniques to your projects. This exercise is designed to give you some experience with that.

Your goal is to create tentacles that look like this for your jellyfish:

<img width="300" alt="TentaclesGif" src="/assets/TentaclesGif.gif">

[This video](https://www.youtube.com/watch?v=LN4XXaHQkmU) demonstrates how to simulate hairs to create renders like this:

<img width="300" alt="HairRender3" src="/assets/HairRender1.png">
<img width="300" alt="HairRender2" src="/assets/HairRender2.png">
<img width="300" alt="HairRender1" src="/assets/HairRender3.png">

Your task is to watch the video and extract the applicable information to make the tentacles! (also, just a heads up, the second half of the tutorial is all irrelevant rendering stuff in C4D, so you only need to watch the first 12 minutes or so).

## (Optional) Extra Credit
- Add another part to your jellyfish. This can be something real (ex: crown jellyfish and lions mane jellyfish have some pretty crazy features that might be fun to recreate) or whatever zany alien jellyfish addition you can imagine!
- Refine one of the existing parts (ex: adding scalloped edges and dents/puckering to the bell of the jellyfish)
- Render your jellyfish (a good place to start is watching [part 4](https://www.youtube.com/watch?v=1Ph-7ZpN5oY) and [part 5](https://www.youtube.com/watch?v=mCQPDf-bupY) of Entagma's Houdini in 5 Minutes series where they briefly cover rendering basics
- Add some flair to your scene by adding a background (ex: coral or rock formations)
## Submission
- Fork this repository
- Update your README
    - Please delete the assignment README text
    - A description of your project
    - A video of your animated jellyfish ([video](https://www.youtube.com/watch?v=gXtDd1lPDmc) of how to save a video of your viewport out of Houdini)
- Create a pull request to this repository
- Submit your Houdini file to Canvas along with a link to your pull request
(Don't upload your houdini files to github -- it's a pain to upload big/binary files. Just canvas is fine!)

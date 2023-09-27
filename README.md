# Procedural Jellyfish

## Project Overview
In this homework, you'll create a procedural jellyfish using Houdini. This will give you a chance to dig into procedural modeling, as well as some simulation. Here is a breakdown of the different jellyfish parts you'll be putting together:

<img height="500" alt="Jellyfish Parts" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/fcc81124-8a51-4637-a618-b7bae13724a8">

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

<img width="300" alt="Remesh" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/c358185e-a93d-4198-9d66-5199f7220d22">

Use the shortest path node to generate veins ([here](https://www.sidefx.com/docs/houdini/nodes/sop/findshortestpath.html) are the docs for the Find Shortest Path node)

<img width="300" alt="ShortestPath" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/4b6f4829-4012-4fee-92a6-e16739c590d8">

Smooth out the veins for a more organic look. You might find yourself needing the "resample" and "fuse" nodes in addition to the "smooth" node (and remember, the [docs](https://www.sidefx.com/docs/houdini/nodes/sop/index.html) are a great resource if you're confused about what a node does or how to use it)

<img width="300" alt="ResampleFuseSmooth" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/1160bb65-b71f-4a0e-96a5-e813d7b31626">

Use a "sweep" node to give the veins width

<img width="300" alt="Sweep" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/1180b046-2323-44ad-8f7f-1e37b4496c52">

Lastly, stick the veins to the bell's animation using the "Point Deform" node that we used on the arms. The final result should look something like this:

<img width="300" alt="Organs" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/e40e18bc-8cab-4a26-be59-79597fbb887f">

## Organs
Next, create organs for your jellyfish. You can approach this any way you'd like! The final result should look something like this:
<img width="300" alt="Veins" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/b8fba148-4fec-4af7-8364-0b2a036aae53">


## Tentacles
When you're working on Houdini projects in the future, you usually won't be able to find tutorials for exactly what you're trying to do. Instead, you'll need to be able to take semi-related tutorials and apply the relevant techniques to your projects. This exercise is designed to give you some experience with that.

Your goal is to create tentacles that look like this for your jellyfish:

![TentaclesGif](https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/f2832a19-64a7-442f-9a86-a11581b9ff0c)

[This video](https://www.youtube.com/watch?v=LN4XXaHQkmU) demonstrates how to simulate hairs to create renders like this:

<img width="300" alt="HairRender3" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/7fd95413-311f-4761-91ca-eaedda337be1">
<img width="300" alt="HairRender2" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/aabb9188-defd-49eb-b0f5-537f3a34f456">
<img width="300" alt="HairRender1" src="https://github.com/e-chou/CIS566-FA23-JellyfishDraft/assets/25019996/40ac3b53-1e76-4aeb-8319-0f20b54c1e9e">

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

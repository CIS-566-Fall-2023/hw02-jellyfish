# Procedural Bee

I used Houdini and VEX to create a procedural ~jellyfish~ bee. 
Below is the final Mantra render. 

<img height="500" alt="renderbee" src="/bee_render.png">

---

Let's get into the breakdown:

## Head and Body
I began with primitive spheres and added noise to make the shape more organic. Remeshing the head and body into triangles also made the connection between the two spheres seem more natural. 

<img height="400" alt="headbody" src="/head_body.png">

## Abdomen 
Working off of Houdini Playground techniques, I used a for-loop to create the bee abdomen. 

First, I created the shape of one section of the abdomen by modifying a torus. 

I then used Houdini's loop nodes to duplicate the shape and stack them on top of each other, creating the full abdomen. The overall structure was created by bending and tapering the duplicated toruses. 

<img height="400" alt="butt" src="/bee_butt.png">

**Jellyfish Parallel**: I used Elyssa's bell technique to create the bee head and body, including bend and mountain nodes. 

## Legs
The legs were created using a combination of VEX and geometric modeling (oops). To get the shape of the first two segments of the legs, I ended up modifying the vertices of a tube. 

However, I did use VEX to create the more jagged shape of the legs' bottom section. I tried replicating a sawtooth function in VEX to create the shape of the leg, before revolving it to make it three-dimensional. I don't think this is super observable because I ended up subdividing the entirety of the legs to make them smoother, so retrospectively, I would have separated the bottom part of the leg and merged at the end. 

The legs were then mirrored and duplicated, with slight variations between the front, middle, and hind legs. 

**Jellyfish Parallel**: The VEX code used in the leg's attribute wrangle node is similar to Elyssa's code to create ruffles in the jellyfish arms. 

<img width="500" alt="legs" src="/legs.png">

## Wings
I first created the base wing by bending a primitive circle. After remeshing it, I worked on creating the details using shortest paths. The wing was slightly extruded and the details were converted to meshes using polywire. 

**Jellyfish Parallel**: The wings follow the technique of the veins, as I used remesh, shortest path, and smooth nodes to create the sprawling details on the wing. 

<img width="400" alt="wings" src="/wings.png">

## Hair
The bee has hair on its head, body, abdomen, and legs. The general method for generating each is the same: calculate normals for the mesh, scatter points on the mesh, copy a hair mesh (bent, polywired line) to each of the points. 

The bee's abdomen hair has a slight detail: the bee's abdomen has more hair closer to the body, and fewer hairs on the stinger side. This was done using a distance to geometry node, in which points are more likely to be scattered on the parts of the mesh that are closer to the bee's body. If I circle back on this project, I'll try to delete the points that scatter inside the abdomen, since it's currently creating hairs that are never seen. 

**Jellyfish Parallel**: The jellyfish tentacles similarly use lines that copy to points on the mesh.  

<img width="400" alt="HairRender" src="/hairpoints.png">
<img width="400" alt="HairRender1" src="/hair.png">

## Animation (just the wings-for now) 
I added a simple animation for the flapping of the wings. 

My method is slightly different from Elyssa's. 

Instead of creating a controller that changes parameter values by keyframe, I specified the animation for the wings directly in a bend node. That is, for the wing's bend angle, I added $F (the current frame number) as a function of cosine. This makes the wing's position change sinusoidally with the frames. Since the animation displaces the wing angle, I also added a switch node that allows the user to toggle the animation on and off, returning the bee's wings to the original position. 

I was too lazy to render the animation oops. 

**Jellyfish Parallel**: Like the jellyfish, my bee moves yay. 

<img width="600" alt="beegif" src="/bee.gif">


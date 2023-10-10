# Procedural Jellyfish

## Project Overview
In this homework, I made a procedural jellyfish using Houdini. This utilized various procedural modeling and simulation techniques to create a bell, arms, organs, veins, and tentacles. 

### Final Animated Videos/GIFs
<img width="800" alt="ColoredWithBGGif" src="/colored-env-light.gif">
<img width="800" alt="ColoredGif" src="/colored-v2.gif">
<img width="800" alt="UncoloredGif" src="/uncolored.gif">

### Final Rendered Images
<img width="800" alt="ColoredRender" src="/Colored_render.jpg"> 
<img width="800" alt="LowShotRender1" src="/low_shot_render.jpg"> 
<img width="800" alt="LowShotRender2" src="/low_shot_2.jpg"> 
<img width="800" alt="TopShotRender1" src="/top_view_render.jpg"> 

### Unshaded Versions
<img width="800" alt="FullUnshaded" src="/full-view-unshaded.jpg"> 
<img width="800" alt="MoveShotUnshaded" src="/move-shot-unshaded.jpg"> 

## Bell 
<img width="400" alt="Bell" src="/bell.jpg"> 
I created the bell using line geometry that I bent to form a cuve. 
I then revolved the curve to form a bell shape and added mountain noise to make the bell shape look more organic.

## Arms
<img width="400" alt="Arms" src="/arms.jpg"> 
I created the arms using grid geometry that I ruffled using a VEXpression. I then duplicated the arm to form a ring of 5 arms using a Copy node. 
I applied Cloth and Hair simulation via Vellum Constraints and Vellum Solver nodes to create general movement for the arms. 
I also pinned the tops of the arms and used a Deform node so that the arms would move with the bell.

## Veins
<img width="400" alt="Veins" src="/veins.jpg"> 
I first remeshed the jellyfish into triangles. 
I then created the veins for the jellyfish using a "Find Shortest Path" node. The starting and ending points for the node were selected from the top and bottom points respectively of the surface of the bell.
I then smoothed out the paths using a combination of Smooth, Fuse, and Resample nodes to make the veins look more organic before giving the veins volume using a Sweep node. 
Like the Arms, I used a Deform node so that the deformation and movement of the veins would match the bell. 

## Organs
<img width="400" alt="Organs" src="/organs.jpg">
I created the organs by taking line geometry and bending it into a curve, just as I did with the bell.
I then used Sweep to give volume to the lines and then Mountain noise to make the shape look more organic.
I then created 4 copies of the base organ using a Copy node and then used a Deform node so that the movement of the organs would match the bell. 


## Tentacles
<img width="400" alt="Tentacles" src="/tentacles.jpg">
I created the tentacles using line geometry as the base strand. 
I then took a scattering of points along the bottom edge of the bell using a Scatter node and copied the base strand onto the scattered points using a CopyToPoints node. 
I applied a Deform node so that the movement of the tentacles would follow the bell. 
I applied a Hair simulation to the tentacles using Vellum Hair and Vellum Solver nodes.
Within the Vellum Solver node, I used Pop Attract and Pop Force to influence the movement of the tentacles. 
Lastly I applied a Sweep node to give volume to the tentacles. 

## Extra Credit 
I created 3 shaders, one for the bell, one for the veins/tentacles, and one for the arms/organs, each with varying traits like color, emission, and transparency.
I added various lights to the scene, including a Geometry Light attached to the organs so that they could glow.
In order to allow for the glow of the organs to show througuh the bell, I made the bell shader somewhat transparent. 


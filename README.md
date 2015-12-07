# GPU robot vision simulation full AI

Super fast GPU-based simulation of simple intelligent robots with vision to develop full AI.

This is currently just a crazy project idea, and does not have an implementation yet.

The final goal is to make it easier to develop vision-based artificial general intelligence https://en.wikipedia.org/wiki/Artificial_general_intelligence.

The key (hopefully) innovative idea that would make things faster than ever before is that everything will run inside the GPU without ever going back to the CPU, which is costly.

The loop is:

1. render (with OpenGL GPU, duh)
1. do computer vision (e.g. OpenCV supports CUDA)
1. take decisions with custom OpenCL and make simulated motors act
1. update the physics engine world state (e.g. Bullet Physics supports AMD)
1. to back to step 1

The idea is that the GPU is the most promising computational breakthrough of our time, and might be the first thing that allows us to reach the critical speed / cost point needed for full AI.

One important part of the project is the choice of the game world. Good game concepts should mimic key aspects of simple real robots / animals:

- first person with perspective
- goals similar to those of simple animals: eat, don't get eaten, find resources

## Mixing stuff

The key technical challenge of this project is keeping all calculations inside the GPU:

- http://stackoverflow.com/questions/18086519/is-it-possible-to-bind-a-opencv-gpumat-as-an-opengl-texture
- http://stackoverflow.com/questions/4005935/mix-opencl-with-opengl

## Literature

Existing research in the area.

-   <http://www.doc.ic.ac.uk/teaching/distinguished-projects/2011/p.lipka.pdf>
    - <https://www.linkedin.com/in/peter-lipka-763aba5b>
    - <http://improbable.io/> Saw this on TechCrunch before. Hot stuff.
        - <https://www.linkedin.com/company/3011959?trk=prof-exp-company-name>
-   <https://www.quora.com/Artificial-Intelligence/How-hard-would-it-be-to-create-an-AI-to-successfully-solve-most-FPS-game-campaigns-today>
-   <http://deepmind.com/>
    - <https://github.com/kuz/DeepMind-Atari-Deep-Q-Learner>
    - BroadMind: <https://www.youtube.com/watch?v=wfL4L_l4U9A>
-   MarI/O <https://www.youtube.com/watch?v=qv6UVOQ0F44>
    - <http://pastebin.com/ZZmSNaHX>
-   Playfun Computer program that learns to play classic NES games
    <http://www.cs.cmu.edu/~tom7/mario/>
    - <https://www.youtube.com/watch?v=xOCurBYI_gY>
-   <https://www.youtube.com/watch?v=bBZ7kEphv3s> Mario AI
-   <http://code.tutsplus.com/tutorials/how-to-build-a-python-bot-that-can-play-web-games--active-11117>

## Possible games

### Realistic animal games

Possible games we could use.

-   <http://www.webearthonline.com/>
-   <https://en.wikipedia.org/wiki/Life_simulation_game>
    -   3d first person:
        -   <https://en.wikipedia.org/wiki/WolfQuest> 2011
            -   youtuber playing <https://www.youtube.com/watch?v=ck5BrLh2eqI>
        -   Minecraft?
    -   iHasCupquake <https://www.youtube.com/channel/UCqg2eLFNUu3QN3dttNeOWkw>
        youtubber that reviews tons of games that have some potential.
    -   Third person;
        - <https://en.wikipedia.org/wiki/Lion_%28video_game%29>
        - gameplay <https://www.youtube.com/watch?v=opDch4j8Bt8>
    -   <http://agar.io/>
-   tier 2
    -   https://www.youtube.com/watch?v=gYZyyWwqdiw
    -   http://jobsimulatorgame.com/
    -   baking simulator https://www.youtube.com/watch?v=qqwAnDgsi6Y
    -   Pet simulator <https://www.youtube.com/watch?v=gYZyyWwqdiw>
    -   http://boards.straightdope.com/sdmb/showthread.php?t=614572

### Others

- FPS

## Engines that allow to take the image from games

- <http://code.tutsplus.com/tutorials/how-to-build-a-python-bot-that-can-play-web-games--active-11117>

## Animal intelligence

Understanding animals could give insights into what our OpenCL intelligence should look like.

-   insects
    -   fruit fly
        - fruit fly associate odour to electric shock <https://www.youtube.com/watch?v=-dPfZE5adYg>
        - fly cyborg 2010 http://spectrum.ieee.org/automaton/robotics/artificial-intelligence/cyborg-fly-pilots-robot-through-obstacle-course
-   reptiles:
    - informal <https://www.youtube.com/watch?v=hr1bKVPyqwU>
-   birds
    - crows:
        - drop stones to raise water level, like in a fable, trained: <https://www.youtube.com/watch?v=lrYPm6DD44M>
        - using sticks as tools: <https://www.youtube.com/watch?v=URZ_EciujrE>
        - 3 tools in sequence: <https://www.youtube.com/watch?v=41Z6Mvjd9w0>
-   tier 2
    - bear turns off electric power to eat deer: <https://www.youtube.com/watch?v=8eC9ZmCaIWY&feature=youtu.be>

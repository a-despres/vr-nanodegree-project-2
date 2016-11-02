## VR Nanodegree - Project 2 - *Build an Apartment*
##### Andrew Despres
------
This purpose of this project was to build an apartment scene using supplied assets. It was my job to place the objects in the scene, place lights, assign materials, build animations, and optimize the VR experience for mobile. The user of the app can move through the apartment by using the trigger on the Cardboard headset. The trigger also starts and stops a spinning animation on the globe. Beyond the official project guidelines, I animated the clock hands so that they move in realtime, and I added city sound effects that are clearly heard from the windows closest to the front door.

#### Time to Completion

This project took approximately 8 hours to complete. A majority of this time was spent troubleshooting animation and material issues.

#### Optimized for Mobile

To optimize for mobile, most of materials are setup as either "Mobile/Diffuse" or "Mobile/Unlit", all lights use baked shadows rather than realtime shadows, and all objects except for the globe and the clock hands are set as static.


#### Completing the Project: Challenges and Accomplishments

When I started this project things were moving along very rapidly. Adding prefabs to the empty apartment scene was very straightforward and I experienced zero issues. However when I moved on to assigning materials to the prefabs I began to run into issues. Assigning a material is straightforward enough; however, many of the prefabs had a pre-assigned shader called "Apartment" that was not rendering properly. All of the prefabs with this pre-assigned shader were rendering as either white or dark gray. I ultimately ended up creating several new materials -- some, ironically enough, using the apartment texture and experimenting with the tiling properties.

The most challenging part of the entire project was adding animations to the scene. The project required that the globe spin/stop when the trigger on the Cardboard headset was pressed. Like much of my experience with this project, things started off smoothly enough before running into issues. I created the spinning animation and setup the state machine with ease. Once I added the "TriggerAnimation" to the globe GameObject the camera stopped rendering. Commenting out a line of code in the "TriggerAnimation" script fixed the issue, but I was not satisfied with this solution. A mentor on the Udacity Forums ultimately tipped me off to the real solution, which involved removing the "GvrViewerMain" object from the scene and re-adding the "GvrViewerMain" prefab to the scene. Sure enough, this worked.

I am satisfied with the end result; however, I feel that the real accomplishment was in my ability to overcome the many different issues that I encountered while completing this project, and everything that I learned as part of that process.

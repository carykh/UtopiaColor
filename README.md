## Setup

1. [Download and install Processing](https://processing.org/download)
2. [Download the code](https://github.com/carykh/UtopiaColor/archive/refs/heads/main.zip) and extract it
3. Open Processing
4. In Processing click File > Open and select `UtopiaColor.pde` in the folder you extracted the code in
5. In Processing click Tools > Manage Tools > Libraries and install:
   - Sound (version 2.4.0 or newer)
   - VideoExport (search for `hamoid`). On newer versions, change `import com.hamoid.*;` to `import com.hamoid.processing.videoExport.*;` at line 3 of UtopiaColor.pde

You can now run the project by clicking the run button in Processing

## Controls for this food chain simulator!

| First Header  | Second Header |
| ------------- | ------------- |
| ENTER | Toggle whether the mouse is locked into the screen (mouse movements change camera direction) or is free again |
| 'WASD' | Move around the gray stick figure viewer guy |
| SPACE | Make the viewer guy jump |
| 'C' | Toggle whether you want the camera to follow a nearby creature (cow or carnivore) or the viewer guy |
| Up and Down | Change the playback speed (1x by default, 10+ speed is good for getting to the next day faster) |
| 'T' | If the camera is currently tracking an animal, pressing 'T' will shift the camera focus to that animal's target (e.g. if a carnivore is chasing a cow) |
| 'U' | Hold down U to rotate the camera at a medium speed for cinematic effect |
| SHIFT | Press SHIFT to toggle whether the camera should rotate at a slow speed for cinematic effect |
| Mouse Wheel | Zoom in and out |

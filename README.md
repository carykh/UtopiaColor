## Setup

1. [Download and install Processing](https://processing.org/download)
2. [Download the code](https://github.com/carykh/UtopiaColor/archive/refs/heads/main.zip) and extract it
3. Open Processing
4. In Processing click File > Open and select `UtopiaColor.pde` in the folder you extracted the code in
5. In Processing click Tools > Manage Tools > Libraries and install:
   - Sound (version 2.4.0 or newer)
   - VideoExport (search for `hamoid`). On newer versions, change `import com.hamoid.*;` to `import com.hamoid.processing.videoExport.*;` at line 3 of UtopiaColor.pde

You can now run the project by clicking the run button in Processing

## Useful information

### Changing starting color
UtopiaColor.pde line 98 is of the form `float[]dna = {x, y};` where:
 - `x` is between 0 and 1 the angle of the color
 - `y` is between 0 and 1 the distance to the center (0 is center, 1 is edge)
If you want the exact same dna for all starting species instead of a small spread, replace the mutate(...) on the next line by dna
If you want a color arc, use random(start, end) for x with the starting and ending colors
If you want a wide arc, use random(in_distance, out_distance) with the inner and outer bonds of the arc

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

## Troubleshooting

### The class "SoundFile" does not exist
You didn't do the [Setup step](#setup) properly. Make sure you install the Sound library.

### The class "VideoExport" does not exist
You didn't do the [Setup step](#setup) properly. Mase sure you install the VideoExport library.

### The package "com.hamoid" does not exist. You probably are missing a library
You are on a newer version of the VideoExport package and need to change `import com.hamoid.*;` to `import com.hamoid.processing.videoExport.*;` at line 3 of UtopiaColor.pde

### White Screen
Change `boolean SAVE_VIDEO = true;` to `boolean SAVE_VIDEO = false;` at line 6 of UtopiaColor.pde
⚠️ This will prevent the code from making the video file named at line 5.

### RuntimeException: Waited 5000ms for ...
See [White Screen](#white-screen) just above

### The function "..." does not exist
You didn't do the [Setup step](#setup) properly. Make sure you extract the code in a folder and open the file from there.

### The game is displaying very wrong
Add a `pixelDensity(1);` line between lines 83 and 84 of UtopiaColor.pde
⚠️ This has been reported to not always work. Sometimes only fixing some of the issues

**Before**:
```java
void setup() {
  map = new Map(SIZE);
```
**After**:
```java
void setup() {
  pixelDensity(1);
  map = new Map(SIZE);
```

### The game is spinning
See [The game is displaying very wrong](#the-game-is-displaying-very-wrong) just above

### The game has a weird offset
See [The game is displaying very wrong](#the-game-is-displaying-very-wrong) just above

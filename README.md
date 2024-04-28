<u>Supported o3de versions</u> : **23.10**

# Loherangrin's O3DE Jam 2305

![gameplay](doc/gameplay.gif?raw=true)

In a near-future the space exploration has reached most of the planets in the Universe. Technology has evolved to transform desert wastes into clean urban areas instantly. But new planets can be hostile and new settlements have to be always protected from natural disasters. How long can you last ?

Game developed for the [O3DE Jam - May 5-14, 2023](https://itch.io/jam/o3de-jam).

## Prerequisites

You need to build or [install O3DE engine](https://o3de.org/download/).

## How to run

1. Download (green "Code" button, then "Download ZIP") or clone the github repository (`git clone https://github.com/loherangrin/games.o3de.o3de-jam-2305.git`)
2. Launch O3DE. It will open the Project manager. Click on the **New Project** button then **Open Existing Project** option.
3. Navigate to your download (and make sure it is unzipped). Open this folder. The project should now be registered.

![project](doc/cover.png?raw=true)

4. Click on the **Build Project** button, located on the **Loherangrin_O3DEJam2305** image.
5. Once the project has been built successfully, use the **Open Editor** button.
6. The asset pre-processor will run for a bit. Once it is over you will be welcomed with the **Open a Level** window, simply pick the first one.

## Controls

| Keys | Description |
| :---: | :--- |
| W / S | Move forward / backward |
| A / D | Turn left / right |
| Space | Toggle the beam |
| E | Land on a platform (if any exists) |
| P | Pause the game / Complete the mission (only after landing) |

## Project Highlights

- **C++ scripting**, custom components interacting with each other via event buses
- **UI**, complete UI with start screen, loading screen, HUD, and so on
- **Terrain procedural generation**, tiles are placed randomly at game launch
- **Level loading**, multiple level with loading screen in-between

### Screenshots

![screenshot](doc/screenshot-1.png?raw=true)

![screenshot](doc/screenshot-2.png?raw=true)

![screenshot](doc/screenshot-3.png?raw=true)

## Game Rules

Use the beam to transform more tiles as possible without loosing all the energy of the spaceship.

- The spaceship consumes energy to move forward and backward, but it can rotate freely.
- When the beam is activated, the spaceship transfers its energy to the selected tiles, transforming them from dust to lawn (or just providing additional energy, if they were already transformed).
- Each transformed tile generates 1 point every 5 seconds, but it will slowly decay returning to its initial state (dust) if no more energy is supplied.
- The decay speed of a tile is affected by the number of already transformed neighbors. While all of them are transformed, the tile doesn't decay anymore.
- When the spaceship energy is lower than 20%, the power-saving mode is activated automatically. Move speed is halved not to consume more energy. Moreover, the beam cannot be activated.
- Energy can be recharged landing on a platform. Spaceship can take off at any time, even if the recharge isn't fully completed.
- Storms can emerge at any place in the map and move in a random direction for a limited time. They reduce the energy of the spaceship or any transformed tiles that they hit along their path.
- Tiles are randomly generated at each sesson. Keep playing to discover new planets!

### Power-ups

After transforming a tile, one of the following collectables might be dropped from it:

| Keys | Description |
| :--- | :--- |
| Coins | Add points to final score |
| Gem | Add extra energy to the spaceship |
| Spikes | Reduce energy of the spaceship |
| Heart | Add extra energy to all transformed tiles |
| Bomb | Reduce energy of all transformed tiles |
| Lever | Speed up the spaceship for a limited time |
| Red flag | Slow down the spaceship for a limited time |
| Lock | Block the decay of all transformed tiles for a limited time |

## License

The source code of this project is licensed under the Apache License, version 2.0. Please see LICENSE and NOTICE files for further details.

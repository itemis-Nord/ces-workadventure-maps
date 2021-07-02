# WorkAdventure Map Starter Kit

This is a starter kit to help you build your own map for [WorkAdventure](https://workadventu.re).

To understand how to use this starter kit, follow the tutorial at [https://workadventu.re/map-building](https://workadventu.re/map-building).

## Introduction

- WorkAdventure is a open source virtual office solution
- Offers instant meetings without the hassle of setting a date
- Maps can be designed and structured as pleased

## Submitting a Map-Change

- Open issue with suggetion for change
- No one complains -> submit pull request with changes
  - If only one map affected, prefix the commit message with the map name like "map_nord: add a shark to the lake"
- Important! Concurrently working on the same map is very problematic
  - Therefore, changes should be as small as possible and quickly transition from issue to PR

## Working with Tiled

[Tiled: Intuitive tool for creating tilemaps](https://www.mapeditor.org/)

### Tilesets
  - Sprite atlases used as a register for tiles to draw
  - For workadventure, tiles should be 32 x 32 pixel
  - Add a tileset via import of a png
  - Important! Tilesets have to be embedded into the tilemap JSONs

### Tilemap
  - A map in which tiles from one or more tilesets are placed
  - Multiple layers
  - Important! Has to be exported as JSON

### Advanced
  - Animated Tiles -- make the surroundings more engaging!
  - TerrainSets -- draw intricate floor-transitions effortlessly!

### WorkAdventure Integration

[WorkAdventure Map-Building Tutorial](https://workadventu.re/map-building)

  - "floorLayer" ObjectLayer is needed (rendering of characters happens here)
  - "start" layer used as the default entrypoint
  - Optinally jitsii-meeting layers for conferencing (one layer per meeting)

## Test maps during development

1. Push your changes to a branch on GitHub
2. Navigate to the changed file in the browser and open it (make sure to select the correct branch)
3. Use the "Raw" link to access the map in an existing Work Adventure instance, e.g. `http://workadventure.your.domain/_/jitsiNamespace/raw.githubusercontent.com/.../map.json`

## Deployment

The maps are currently hosted on Github Pages. A merge to master triggers a Github Action which deploys the new maps.

## Ressources

- [WorkAdventure Map-Building Tutorial](https://workadventu.re/map-building)
- [Tiled Editor](https://www.mapeditor.org/)

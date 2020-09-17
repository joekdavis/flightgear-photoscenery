# FlightGear - PhotoScenery Edition

This project brings support for photoscenery to FlightGear, the free and open-source flight simulator.
The photoscenery is an overlay, which overrides the traditional scenery textures when available.
It is fully compatible with Atmospheric Light Scattering, and works with your existing scenery. There is a toggle in the rendering options.

This is a work in progress. Currently, orthophotos need to be provided manually in the PNG format (flipped vertically), placed alongside the tile that they correspond to in the `Terrain/` subdirectory of your scenery. For example, tile 991000 already has the files `991000.stg` and `991000.btg.gz`, and you would put `991000.png` alongside them.

## Getting it

I plan to release prebuilt binaries for Linux, MacOS, and Windows to coincide with the upcoming release of FlightGear 2020.2. Currently, you need to build from source.

## Building from source

1. Clone the official FlightGear base data package at the release/2020.2 branch. (`git clone -b release/2020.2 https://git.code.sf.net/p/flightgear/fgdata`). Apply my patch. ([simgear.patch](simgear.patch) in this repository)
1. Clone my patched [SimGear repository](https://github.com/nathanielwarner/simgear) (`git clone https://github.com/nathanielwarner/simgear`), and follow the normal build and install instructions. You may want to set the install prefix so as not to conflict with an existing installation of simgear.
2. Clone the official FlightGear repository, at the release/2020.2 branch. (`git clone -b release/2020.2 https://git.code.sf.net/p/flightgear/flightgear`). No patch needs to be applied. Follow the normal build instructions, making sure that the base data package and simgear location is set to the patched ones you installed.

## Screenshots

All screenshots are with ALS renderer at max quality, and OpenStreetMap buildings enabled.

KSBA area, with photoscenery:

![KSBA photoscenery](screenshots/ksba-photoscenery.png)

Same location, with traditional scenery:

![KSBA traditional scenery](screenshots/ksba-traditional.png)

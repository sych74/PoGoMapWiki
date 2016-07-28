# Pokemon Go Map Wiki

## About Pokemon Go Map

[PoGoMap](https://jz6.github.io/PoGoMap/) is aiming to bring a live visualization map of nearby Pokémon, Pokéstops and gyms in a form of a web-app as well as native phone applications. It can be self hosted and [installed](installation.md) on Windows, Mac, and Linux, with [Android](https://github.com/omkarmoghe/Pokemap) and [iOS](https://github.com/istornz/iPokeGo) ports currently in development.

**[Demo](http://pkmgomap.com/)**

**Video Setups:**  
[Video Walkthrough](https://www.youtube.com/watch?v=RJKAulPCkRI)  
[German Amazon EC2 Tutorial](https://www.youtube.com/watch?v=FxcVGrszl3I)

## Releases

The current state of releases can be found on the official [GitHub Repo](https://github.com/AHAAAAAAA/PokemonGo-Map/releases).

### v2.1.0
  * Vastly improved the search pattern for maximum speed
  * Added China transformations
  * Added option to notify with sound
  * Stopped hardcoding URL root in JS
  * Added a `config.ini` file
  * Started clearing selection when opening an infoWindow
  * Added a current location indicator
  * Added exclude and notify links to Pokémon info popup
  * Added MySQL as an database alternative
  * Added flags to disable Pokémon, Pokéstop, and/or gym parsing
  * Added option to disable search bar
  * Center map on Pokemon on notification click
  * Added a sprite for the Pokémon on the map
  * Added directions div to gym marker
  * Added many multi-threading improvements
  * Added 3 custom map styles that remove labels
  * Added `--only-server` mode
  * Added various lure improvements
  * Added bounce animation to markers for notified Pokémon
  * Added latitude and longitude to location markers
  * Added webhook integration
  * Added the ability to display only lured Pokéstops
  * Improved step misalignment after huge numbers of steps
  * Cleaned up the code

**[Download](https://github.com/AHAAAAAAA/PokemonGo-Map/archive/v2.1.0.zip)**

### v2.0.0

  * Completely reformatted code
  * Added multithreading capability
  * Added an enhanced user interface
  * Introduced map styles
  * Added the ability to easily track scans
  * Improved searching
  * Added database storage
  * Added cookies
  * Added a mobile/reduced data mode

**[Download](https://github.com/AHAAAAAAA/PokemonGo-Map/archive/v2.0.0.zip)**

### v1.0.0

This is the original build before the major rewrite. Will forever be home to the infamous `example.py`.

**[Download](https://github.com/AHAAAAAAA/PokemonGo-Map/archive/v1.0.0.zip)**

## Contributing

### Contributing to this Wiki

Follow the instructions at *[WikiContribs](WikiContribs.md)* to learn how to edit and add new pages to this wiki.

Contributions are via GitHub Pull Requests and are moderated and approved by [Jonah Aragon](https://github.com/JonahAragon) and other PoGoMap Developers.

### Contributing to the project

*See [Development](Development.md)*

## Other Information

### Project refactor
As of 2016-07-20, support for the first implementation 'example.py' was dropped.<br/>
Please use the refactored version present in the branch `develop`. <br/>
Periodic tagged releases will be made

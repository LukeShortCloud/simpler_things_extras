# Simpler Things RPG Extras

Additional resources for the [Simpler Things RPG](https://github.com/ekultails/simpler_things_rpg). Reference guides, character sheets, and examples are provided. PDF releases of these documents are available as assets [here](https://github.com/ekultails/simpler_things_extras/releases).

## Documents

### Character Sheet

The [stre_character_sheet.fods](stre_character_sheet.fods) character sheet is in the Flat OpenDocument Spreadsheet (FODS) document format. This provides advanced formatting, a condensed size to reduce paper waste, the ability to add equations, and the flat (uncompressed) format helps to better provide a git revision history of the changes.

Instructions on how to create a PDF:

- LibreOffice Calc
    - File > Print Preview > Format Page > Sheet > Print > (check the box for “Grid”) > OK
    - File > Export as PDF... > Export

### Genres

The [stre_genres.md](stre_genres.md) guide explains how to adapt Simpler Things RPG to specific genres. Currently, this only contains Star Wars.

### Player Character Guide

The [stre_pc_guide.md](stre_pc_guide.md) document is an introduction to TTRPG and how to use skills in the game.

## Versioning

Both Simpler Things RPG and Extras follow semantic versioning of: `X.Y.Z`. Extras mirrors the major (X) and minor (Y) version of RPG. The bugfix release (Z) is independent/separate between the two repositories.

For example, RPG version 0.1.0 is compatible with Extras 0.1.1.

## Build Releases

Each tagged release on GitHub has a related release that provides PDF files.

```sh
for guide in $(ls -1 *.md | cut -d\. -f1); do pandoc --toc --variable urlcolor=cyan -f markdown -t latex -o ${guide}.pdf ${guide}.md; done
```

## License

[WTFPL](http://www.wtfpl.net/about/)

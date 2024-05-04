Kelly Hill Therion template.  This is a boilerplate repo designed to help those learning to use Therion for the
Kelly Hill Cave Project.  It is configured in a manner that should render the caves using the ASF Cave Map symbols,
with a few UIS ones used occasionally because it looks a little nicer.

This repo is a work in progress, so expect changes.  Feel free to suggest changes too!

## How to use
This is pre-configured to use the sample cave k90.  The following instructions should build a map

1. Install Therion https://therion.speleo.sk - see also "Setting up Therion"
2. Open COMPILE.thconfig using xTherion
3. Create a directory called `output`
4. click the Compile button
5. check in the `output` folder for PDFs for the example cave

## How to set this up for a new cave

This is both easy (copying the example), and hard (the manual work required to draw your new cave).  

1. Collect your survey data, and place it in a folder within the `data` folder.  Being as we're working on Kangaroo Island, this will probably be `k<something>`.
2. Place in this folder any relevant survey data you've collected:
    1. Any scans of cave sketches.
    2. Survey data from Survex - either in svx or .3d form (I haven't tested .3d yet, so stay tuned).
    3. You'll need two Therion files - on .th (the survey data) and the other .th2 (the drawing you will eventually do).
3. Inside the kXX.th file, you will place your data from Survex.  `data/k90` has a reasonably straight forward example.  You can mostly copy/paste from an svx file, removing the * at the beginning of the lines.
4. The .th2 file is created in xTherion using it's _Map Editor_ mode.  Open up the app, click _New_ and then _Save As_.
5. (the hard bit begins) - using the Map Editor, load into it the scanned cave sketch, and then use a bunch of clunky controls to "draw" the map.  This is too hard to describe in words, I strongly recommend watching one of the videos in the Credits section.
6. Inside the COMPILE.thconfig file on line 4 change the `source` value to be the path to your new .th file.
7. Inside the .th file, make sure the `input` value on line 4 points to your newly created .th2 file.
8. Click on the Compile button, and possibly some kind of ritual sacrifice.
9. Assuming it doesn't show an error, inside the `output` folder will be several PDF files that may or may not look like a cave map.

## Setting up Therion

Depending on your operating system you have a few options:

1. Download the installer via Windows [https://therion.speleo.sk/download.php]
2. Install via your Linux package manager
    1. For Ubuntu `sudo apt install therion`

Note: the package manager appears to be either out of date (Ubuntu), or not working at all (Fedora) in my experience.  For the brave, [Github](https://github.com/therion/therion) allows you to clone and build the code yourself.


## Credits
Thanks to Greenman126 for his excellent template and video tutorial:

- https://github.com/Greenman126/Therion-Template-and-builder/blob/main/caveSketch.th2
- https://www.youtube.com/watch?v=nBhx0gRTJb0

## Useful resources

- [ASF Cave Map Symbols](https://caves.org.au/resources/)
- [UIS Cave Map Symbols](https://www.carto.net/neumann/caving/cave-symbols/uis_signatures_english.pdf)

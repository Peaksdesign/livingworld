# Conway's Game of life PHP implementation

A simple test application using Symfony 3.x components and using PHP 7.x features.

## How to use

First, generate a new world into a xml file in order to have something to process.
Then run the data import that will draw the life on the screen and save the 
last frame into another xml file.

### Generate your world

World generation is simple and is done by following console command:

``php app/console.php generate:world targetFile.xml 10 10 15``

The first argument is a file that will describe the world and its occupants.
The other parameters are a number of organisms to life in the world, number of cells
of which the world consists and number of life cycles.

### Import and process the life

Then, you can start the life cycles:

``php app/console.php import:xml sourceFile.xml targetFile.xml 2``

The cycle reads initial state from ``sourceFile.xml`` and executes the logic.
The last frame is saved into target file ``targetFile.xml`` in a format of source files
 so that they can be further processed as source files. The last argument is FPS for the writer.

## Contribute

[![Build Status](https://travis-ci.org/tuscanicz/livingworld.svg?branch=master)](https://travis-ci.org/tuscanicz/livingworld)

Feel free to contribute!

Please, run the tests via ``composer ci`` and keep the code quality.

Enjoy.
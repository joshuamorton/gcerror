gcerror
=======
To reproduce the error:

1. Clone this repo onto your computer
2. open the index.html page in google chrome

The error seems to stem from Chrome not correctly using custom fonts defined via the @font-face in a css file if the font is being used by a canvas with `context.font=''stuff';` and then `context.fillText(stuff);` or `context.strokeText(stuff);`

The index.html page shows that built in fonts do work correctly, yet even if a font renders correctly in browser.  This is true on both Windows 8.1 and ubuntu 13.10.  I also included a the same file rendered in Internet explorer (at 90% zoom) for comparison, where the images do render correctly.  The final example using jQuery `$(document).ready` was included to make certain that the error was not because of a missing or not loaded file.

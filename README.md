# Unofficial Documentation for Shadowrun Returns Editor

## Main folders
There are three major folders you would be interested in:
- (Content pack folder)\art
- (Content pack folder)\misc
- (Content pack folder)\chars\templates

The first holds the artwork you can use in your quest items and portraits for characters. File format must be PNG. I haven't tested the maximum resolution but I think it should be less than 1024x1024px.

The second folder can contain files for your epilogue (they must be `.txt` format -- no RTF text! e.g. `ending_good.txt`) and credit text to be prepended to the credits roll (must be named `credits.txt`)

The third folder contains the template for your characters. If you need a specific character to be the main character, put the templates here.

## Editor notes
The "End game with epilogue and credits" option takes file names (text files in the `misc` folder), **not** raw text! This puzzled me for a long time.

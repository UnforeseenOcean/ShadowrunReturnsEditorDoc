# Unofficial Documentation for Shadowrun Returns Editor

## Main folders
There are three major folders you would be interested in:
- `(Content pack folder)\art`
- `(Content pack folder)\misc`
- `(Content pack folder)\chars\templates`

The first holds the artwork you can use in your quest items and portraits for characters. File format must be PNG. I haven't tested the maximum resolution but I think it should be less than 1024x1024px just to be safe.

The second folder can contain files for your epilogue (they must be `.txt` format -- no RTF text! e.g. `ending_good.txt`) and credit text to be prepended to the credits roll (must be named `credits.txt`)

The third folder contains the template for your characters. If you need a specific character to be the main character, put the templates here.

## Editor notes
The "End game with epilogue and credits" option takes file names (text files in the `misc` folder), **not** raw text! This puzzled me for a long time.

## Improvements
- Add "Load external resources" option
  - Example syntax: `Load (things\00_placeholder.wav) as (sound)`
- Allow streaming of audio files from folders
  - This makes adding custom sounds and music very very significantly easier than using UABE and hacking one in
- Make `art` folder by default
- Formatting for the epilogue text or Rich Text Editor integration through Sciltilla, perhaps
- More documentation

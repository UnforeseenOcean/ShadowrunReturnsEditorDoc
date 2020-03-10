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
- The "End game with epilogue and credits" option takes file names (text files in the `misc` folder), **not** raw text! This puzzled me for a long time.
- The scene, quest item or conversation name cannot contain the word "meta". This also means `ch1-sc1-Item-Metal` is also invalid since it contains "meta" in the name. 
- If the Test Scene or compilation fails with blank error report, run "Validate Content Pack Dependencies". It will usually show what went wrong.
- Weirdly, the editor *does* read all files in the directory, regardless of its usability; You have to make sure you aren't putting any weird files into the folders, even if it's your own folder. Else, it will cause errors.

## credits.txt
Put this file in `misc` folder. The formatting is as follows:
- `(text)`: Unformatted text, centered
- `t1#(text)`: Title text
- `h1#(text)`: Header text (bigger version of `h2#`)
- `h2#(text)`: Subtitle text (yellow font for SRR)
- `nd#(text)|(text)`: Name list text, where the text after `|` is treated as job title

![Demo](https://raw.githubusercontent.com/UnforeseenOcean/ShadowrunReturnsEditorDoc/master/img/IMG1583860720.png "Formatting demo")

The text data in the credits.txt in this example is as follows:
```
t1#Escape Velocity 

h1#by Blackbeard Gameworks

h2#Project Leads

nd#Torbjorn Lindholm|Director

Lead Artist
Torbjorn Lindholm
```

## Improvements
- Add "Load external resources" option
  - Example syntax: `Load (things\00_placeholder.wav) as (sound)`
- Allow streaming of audio files from folders
  - This makes adding custom sounds and music very very significantly easier than using UABE and hacking one in
- Make `art` folder by default
- Formatting for the epilogue text or Rich Text Editor integration through Scintilla, perhaps
- More documentation

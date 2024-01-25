# big-funk
Mod Of PenguinFunk.



OG SHIT HERE :

It's basically Friday Night Funkin but rewritten in PenguinMod.
Probably the cleanest Friday Night Funkin framework ever. Like seriously. It's like 1.6MB by itself.

What it can do
Reads charts made with the Friday Night Funkin chart editor
Group multiple songs into weeks
Has (limited) support for Psych Engine events. You can add more using JavaScript!
Can load mods from the "Mods" folder
Characters with configs and icons
Stages with configs and animated elements
Songs with charts
Customizable list to display the mods
What it can't do
Access your bank account
Why does this exist
Because it's very small compared to other Friday Night Funkin engines.
It's light and fast, making it run really well on lower-end devices. Also, JavaScript is the best programming language to ever get created.

How to use
While you read this, I would recommend looking at the example mods that I have ported in the "Mods" folder.

Folder structure
The folder structure is pretty easy to understand.

Mods
Mod-name
Characters
Player
Enemy
Stage
Song
Character folders
The characters folder contains 2 sub-folders. "Enemy" and "Player". The "Enemy" folder will contain the assets for the character you play against, and the "Player" folder will contain the assets for the character that you play as. I use this tool to get the individual frames from a spritesheet.
The 2 folders will both contain:

A "character.json" file
The poses as separate frames, followed by their name and frame number
The icon of the character, named "icon.png"
Look in the "Mods" folder for examples.
character.json
The "character.json" file will contain the configuration of the character.
This is its structure:

"size": size of the character
"cameraX": where the cameraX goes when this character sings
"cameraY": where the cameraY goes when this character sings
"x": y position
"animations"
"idle"
"frames": number of frames for that pose
"up"
"frames": number of frames for that pose
"down"
"frames": number of frames for that pose
"left"
"frames": number of frames for that pose
"right"
"frames": number of frames for that pose
"seconds per frame"
"offsets"
"idle"
"x"
"y"
"up"
"x"
"y"
"down"
"x"
"y"
"left"
"x"
"y"
"right"
"x"
"y"
"healthColor": color in HEX
Stage folder
The stage folder contains all the images in the stage and a stage.json file. Pretty simple.

stage.json
The "stage.json" file is a JSON array. Every item in that array is a background object.

A basic background item looks like this:

{"fileName":"nameOfImage.png","x": X position,"y": Y position,"size": size of object}


An animated background item looks like this:

{"fileName":"fileNamePrefix.png","x": X position,"y": Y position,"size": size of object,"isAnimated":true,"frames":number of frames,"seconds per frame": seconds per frame}


There also are special properties that you can add:
"canBop" will make that element bop on the beat. You can look at the "stage.json" file of the "fuss-erect" and "soda-pop" examples to see it.
"inFront" will render the element in front of everything else.

Song folder
It contains "song.json" and "song.mp3".
Unlike other Friday Night Funkin engines, this one doesn't use 2 separate tracks for the instrumental and the vocals. They are merged into an MP3 file. It's also worth noting that nothing besides MP3 works.
The "song.json" file is just the chart of the song. Nothing special.



























































































cantaloupe

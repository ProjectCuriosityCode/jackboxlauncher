Jackbox Game Launcher
=============

Version 1.0

The Jackbox Game Laucher shows all the games in each Jackbox pack in one spot.
Using this you can view basic information from each game and launch the pack of the game
you are viewing. There is even a random game button for when your friends are too lazy
to pick a game. It will not launch the specific game in the pack but it's purpose is
mainly to view all the games in a nice way similar to the main menus of the packs.



Using the Launcher
---------------

Step 1: Launch the include exe

It is as simple as that but the launcher by default should have all the packs enabled 
but no file paths for them. This means they will be viewable but not launchable through
the launcher.

To Be Able To Launch Games Through the Launcher Follow These Steps
Step 1: Click the setting button at the top right of the program
Step 2: In the entry box for each paste the file path to the exe for that pack or press the button
            to the right of the entry box to open a file explorere to select the exe for the pack
Step 3: Press the save buttton at the bottom right of the program
Step 4: Press the home button at the top right of the program
Step 5: The play button for the pack should now be enabled if the file path is a valid exe


Adding/Removing/Editing Games
---------------

In the settings menu for the launcher you can enable/disable packs but if you want to 
add/remove/edit games completely you can edit the games.json file.

If there is no games in a pack that pack will not be loaded into the program.

This is an example of what the games.json file looks like with one entry.
```json
[
    {
        "name": "Drawful 2",
        "bg_color": "white",
        "text_color": "deep pink",
        "description_color": "black",
        "highlight_color": "deep pink",
        "title_color": "deep pink",
        "button_text_color": "deep pink",
        "picturesPath": "Pictures/Drawful 2/",
        "enabled": true,
        "gamePath": "F:\\Program Files (x86)\\Steam\\steamapps\\common\\Drawful 2\\Drawful 2.exe",
        "games": [
            {
                "name": "Drawful 2",
                "pictureName": "drawful2.png",
                "description": "For 3-8 players and an audience of thousands! Your phones or tablets are your controllers! The game of terrible drawings and hilariously wrong answers."
            }
        ]
    }
] ```

I did not hard code in a max amount of packs or games for each pack but GUI is not yet designed to infinitly scale.
This means you can put as mony games/packs as you want but they appear as a list they might go off the screen.



Variables and What They Mean
---------------

These are the variables in the game.json file and what they are used for.

For the color variables you can use valid python color names like "white" or hex codes like "#ffffff"

"name"                  -Stores the pack/game name that is displayed on the top of the GUI
"bg_color"              -This is the background color of the GUI and all the widgets when the pack is being viewed
"text_color"            -This is the default text color of the games in the pack when the pack is being viewed
"description_color"     -This is the color of the decription text for the games in that pack
"highlight_color"       -This is the color of the game that is being viewed in the pack
"title_color"           -Color of the text for the title of the pack being viewed
"button_text_color"     -This is the text color of all the buttons in the GUI when viewing the pack
"picturesPath"          -File path for the folder that stores the pictures for the pack
"enabled"               -This is a boolean tells the program if the program should be viewable
"gamePath"              -This is the file path of the exe used to launch the pack

"games"                 -This is an array of all the games in the pack
    "name"              -This is the name for the game in the pack
    "pictureName"       -Name of the picture in the folder path given by "picturesPath"
    "description"       -Text description of the game



Changing The Pictures
---------------

The resolution for the game preview pictures is 640x360.
The resolution for the GUI button pictures is 120x120.



More Pointless information on Me and the Project
---------------

Programmer Name:   ProjectCuriosity
Version Number :   1.0
Python Version :   3.9 (64 Bit)
OS             :   Windows

I am a college student who just likes speading days making projects to automate problems I run into 
that take a minute to do manually.
This is the first thing I have made in python so it is far from perfect but I hope it solves
a small problem I ran into when playing jackbox with my friends.

I have been working on this project in my free time for about a couple weeks now but got it too
the point I can call it a version 1.0.
If I decide to continue to work on this project I have a few updates in mind. Some features I would like
to add next are
    1.Linux and Mac Support
    2. Ability to Like/Dislike Games
        -Disliked games would not be chosen when pressing the random game button.
    3. Genre tags for games
        -Simple tags like drawing, trivia, etc.
    4. More information for the games
        -I would like information like player amount, family friendly, etc to be viewable in the Launcher
I have a few more ideas i'm unsure if I want to do but these three would make the launcher ten times better.
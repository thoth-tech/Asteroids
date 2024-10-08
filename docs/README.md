# Asteroids1.0

## Game intro

Asteroids is a top-down single player or co-op shooter that has you, the player, flying around and
surviving an onslaught of rocks, and if you survive long enough, even bosses! Aim for a high score,
don't lose your hearts before your friend, and maneuver around dangers and rack up that score!

## Running the game

Assuming you are CD'd into the correct directory, the game can be run with a simple `skm dotnet run`
command via the MSYS2 terminal. If you aren't CD'd into the directory, or don't know what that
means, open MSYS2, find the folder path for Asteroids, and copy it into a

```
cd '{path}'
```

command, where {path} is your copied explorer path, apostrophes included to account for file path
spaces.

## Basic Controls

Main menu controls assume player 1 controls for movement, selections, and actions unless otherwise
stated. At any time an ESC key input will quit the game.

Player 1 controls:

    Up arrow:       Move Forward
    Left arrow:     Rotate Left
    Right Arrow:    Rotate Right
    Ctrl:           Fire

Player 2 controls:

    S/R Key:            Move Forward
    D Key:              Rotate Left
    G Key:              Rotate Right
    A Key:              Fire

## Game Config

From the main Asteroids folder, navigating to /Resources/json will yield the `Controls.json` and the
`Game_Config.json` files. `Controls.json` houses the key mappings that Asteroids has defined (but
not necessarily ones that are in use, those are above and up-to-date as of writing).
`Game_Config.json` houses a few editable parameters for Asteroids:

    "fullscreen": true,
    "gameScale": 0.6,
    "no_boarder": false,
    "screen_height": 540,
    "screen_width": 960

`fullscreen` will, as the name suggests, determine whether or not on launch the game sets itself to
fullscreen.

`gameScale` refers to some visual elements of Asteroids, adjusts the position and movement of
everything in the game, and should not be edited without proper editing of `screen_height` and
`screen_width` as well to ensure visual communication and fidelity. Example of base game scale and
calculations for 80% and 60% scaled versions:

    Full res:                   1600 x 900,   game scale:     1
    80% res:                    1280 x 720,   game scale:     0.8  →   1600*0.8 || 900*0.7
    60% res: (current setting)  960 x 540,    game scale:     0.6  →   1600*0.6 || 900*0.6

`no_boarder` will determine, if `fullscreen` is false, whether or not the standard Windows / OS
program border (that houses minimize, maximize, and close buttons) will be visible on the
application. This removes movement and minimization functionality of the game window, but the
application can still be quit via the escape key if necessary.

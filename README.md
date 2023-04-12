# Bab-be-u-modding-guide
I hope this will help you create your own bab be u mod.
## How to add your sprite
Put your sprite in `assets/sprites`. You can put it in any folder, i for guide will new one, and call it `dzhake`.

![Image here](pictures/FolderExample.PNG)

Then open `assets/tiles/objects`. You can see some `.json` files, you can change any of them, but i prefer to create my own, and copy text from characters.json to it. But there are so many text! I will leave only text about bab.

```json
[
  {
    "name": "bab",
    "sprite": ["bab"],
    "layer": 11,
    "color": [[0, 3]],
    "rotate": true,
    "features": {
      "sans": {"x": 22, "y": 10, "w": 2, "h": 2}
    },
    "voice": "s_doo",
    "desc": "its bab bruh",
    "tags": ["chars", "baba"],
    "pronouns": ["she", "her"]
  },
  {
    "name": "txt_bab",
    "sprite": ["txt/bab"],
    "metasprite": ["txt/bab meta"],
    "types": ["object"],
    "color": [[4, 1]],
    "desc": "\"BAB\". thats what it says",
    "tags": ["chars", "baba"]
  }
]
```

My sprite called `discord` so i need to replace some things.

```json
[
  {
    "name": "discord",
    "sprite": ["dzhake/discord"], (i made my folder called dzhake and put sprite called discord there. So path is `dzhake/discord`.)
    "layer": 11, (z layer of sprite. Bg things should be below 10 and characters from 11-25. You can add any number above 0 but if you will make char with layer 1 it will be below all deco.)
    "color": [[0, 3]], (bab uses paletts from baba! You can find them in `assets/paletts` and you can change palette for level in level settings.)
    "rotate": true, (true if object can rotate when moves. Don't you think, rotating wall looks strange but rotating bab isn't.)
    "features": {
      "sans": {"x": 0, "y": 0, "w": 0, "h": 0} ( when `x is sans` formed `x` gets light-blue thing. You can change it here.)
    },
    "voice": "s_doo", (you can sing! Changes voice, from `assets/audio/sfx`)
    "desc": "its bab bruh", (Description. You see it when hover above object in selector)
    "tags": ["chars", "baba"], (Todo: understand what for tags exists.)
    "pronouns": ["she", "her"] (Todo: understand what for pronouns exists.)
  }, (don't forget comma if this is not last object in your `.json` file!)
  {
    "name": "txt_bab",
    "sprite": ["txt/bab"],
    "metasprite": ["txt/bab meta"],
    "types": ["object"],
    "color": [[4, 1]],
    "desc": "\"BAB\". thats what it says",
    "tags": ["chars", "baba"]
  }
]
```
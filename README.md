# Bab-be-u-modding-guide
I hope this will help you create your own bab be u mod.
## How to add your sprite
### Basics
Put your sprite in `assets/sprites`. You can put it in any folder, i for guide will new one, and call it `dzhake`.
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
    "sprite": ["dzhake/discord"],
    "layer": 11,
    "color": [[0, 3]],
    "rotate": true,
    "features": {
      "sans": {"x": 0, "y": 0, "w": 0, "h": 0}
    },
    "voice": "s_doo",
    "desc": "its bab bruh",
    "tags": ["chars", "baba"],
    "pronouns": ["she", "her"]
  },
  {
    "name": "txt_bab", (txt_..object name)
    "sprite": ["dzhake/txt/discord"], (in my folder i created `txt` folder and put my text there with name `discord`. So path is `dzhake/txt/discord`)
    "metasprite": ["dzhake/txt/discord meta"], (just add space meta, but you can change this if you want custom meta sprite)
    "types": ["object"], (What does this text mean? Is it prefix? Infix? Prop? No! It refences to object!)
    "color": [[4, 1]], (color from palette)
    "desc": "\"BAB\". thats what it says", (in game this looks `"BAB" thats what it says`. You need to put `\` because this is part of string)
    "tags": ["chars", "baba"]
  } ,
  {
    "name": "txt_babn't", (just `n't` sprite. It's optional, two sprites is enogh. Why do you want this? To change: sprite (like won't), discription (like bab), or something else)
    "display": "bab n't", (Just name without `txt_`+` n't` (something about order of display maybe?))
    "sprite": ["txt/bab meta", "n't"], (todo: write todo here)
    "types": ["object"],
    "color": [[4, 1], [2, 2]],
    "painted": [true, false], (can sprite be painted? Sprite can, but `n't` can't. In `sprite` we can see that we have two sprites!)
    "desc": "BAB N'T: The same as having these two text tiles in a row."
  } (No comma here because this is last object in file!!!)
]
```
 - `object thing`:
	 - `sprite`: i made my folder called dzhake and put sprite called discord there. So path is `dzhake/discord`.
	 - `layer`: z layer of sprite. Bg things should be below 10 and characters from 11-25. You can add any number above 0 but if you will make char with layer 1 it will be below all deco.
	 - `color`: bab uses paletts from baba! You can find them in `assets/paletts` and you can change palette for level in level settings.
	 - `rotate`: true if object can rotate when moves. Don't you think, rotating wall looks strange but rotating bab isn't.
	 - `featurues`:
	   - `sans`: when `x is sans` formed `x` gets light-blue thing. You can change it here.
	 - `voice`: objects can sing! Changes voice, from `assets/audio/sfx`
	 - `desc`: Description. You see it when hover above object in selector
	 - `tags`: uhh idk
	 - `pronous`: used in `x is self`. Example: `bab is herself`.
 - `text things`:
	- blablbalba
 
 
 
 
I added my sprite to game, but i can't find it in selector!
Of course i can't! Because i need to add it to selector!
Open `values.lua` in root game folder and scroll to bottom.
You can see 9 pages, you can create another one, or add your sprite to existing one.
I will add my sprite to `unfinished` tab (it's last)
Instead of 0 somewhere i write `"discord"`, and next to it `"txt_discord"`.
Now i can open game and find my sprites!

[README.md](https://github.com/user-attachments/files/33106748/README.md)
# Ocarina of Time: 2-Player Splitscreen (v0.2)

This mod adds a second, playable Link on controller 2, with the screen split in two. It's a fan mod built on the zeldaret/oot decompilation.

- **Game version:** The Legend of Zelda: Ocarina of Time, USA v1.2 (Rev 2)
- **Clean ROM MD5:** `57a9719ad547c516342e1a15d5c28c3d`
- **Runs on:** N64 emulators only. It doesn't run on original hardware.

---

## Installing

1. Start with a clean, unmodified **USA v1.2** ROM in `.z64` format.
2. Apply `OoT-Splitscreen-v0.2.bps` to it with **Floating IPS** or **Rom Patcher JS**.
3. Load the patched ROM in your emulator.

## Emulator settings

| Setting | Why |
|---|---|
| **Controller 2 plugged in** | Player 2 only appears if controller 2 is connected when an area loads. |
| **Expansion Pak / 8 MB RAM on** | The extra memory is needed to draw the second view. Mupen64Plus-based emulators have it on by default. In Project64, set the game's memory size to 8 MB. |
| **CPU overclock (if it's slow)** | The game draws every area twice, so it's heavier than the original. Turn on an option like "Overclock VR4300" or "Counter Factor 1". |

---

## Features

### Splitscreen
- Player 1 is on the **top half** of the screen and player 2 is on the **bottom half**.
- Each player has their own camera, including Z-targeting, first-person aiming (C-up, slingshot, bow, hookshot) and the camera turning to follow them.
- In areas with **fixed camera angles** (the Market, shops, houses), both players share **one full screen** and play on it together.

### Shared and separate stats
- **Shared:** sword, shield, tunic, boots, C-button items, ammo, rupees and keys.
- **Separate:** each player has their own **hearts** and **magic meter**. Player 2's hearts and magic are shown in the bottom half of the screen.
- Recovery hearts, magic jars, rupees, sticks, nuts and seeds can be picked up by **either player**. Hearts and magic go to whoever picks them up.
- A potion or fairy that player 2 uses heals player 2.

### Combat
- Each enemy goes after **whichever player is closer**.
- **Damage only hits the player who was struck.** The other player doesn't take damage or play the hurt animation. This was fixed in v0.2.
- Player 2's **Z button** locks on to the nearest enemy in front of them. Pressing it again releases the lock.
- Player 2 can use the sword, spin attack (which uses player 2's own magic), shield, slingshot, bow, magic arrows, bombs, bombchus, Deku nuts, sticks, the boomerang, the hookshot, the Megaton Hammer, masks and potions.

### Cutscenes
- During cutscenes, text boxes, conversations, item-get scenes and area transitions, **player 2 is hidden and frozen**, and player 1 gets the full screen.
- When the cutscene ends, player 2 reappears next to player 1.

### Player 2 can't get stuck or end the game
- **Player 2 can't die.** At 0 hearts, player 2 reappears next to player 1 with 3 hearts. Only player 1 can get a game over.
- **Player 2 can't trigger loading zones or void-outs.** If they walk into an exit or fall into a pit, they're moved back to player 1 instead. Only player 1 can change areas.
- Player 2 is also moved back to player 1 after falling out of the level, getting very far away, or being left behind when player 1 goes through a door.
- Player 2 reappears **beside** player 1, away from walls, exits and pits. That spot is checked before player 2 is placed there (also fixed in v0.2).

### Pausing
- Only player 1 can pause, with START. The pause menu fills the whole screen.

---

## Limitations

### Things only player 1 can do
These affect the whole game world, so they stay with player 1:

- Talk to people, read signs, open doors and chests
- Get big items: keys, heart pieces, heart containers, new equipment
- Play the **Ocarina** and its songs
- Cast **Din's Fire**, **Farore's Wind** or **Nayru's Love**, or use the **Lens of Truth**
- Use **trade-sequence items** (egg, chicken, letters, and the adult trade items)
- Use **empty bottles** to catch things, or bottles holding a fish, bug, poe, Blue Fire or Ruto's letter
- Use the **fishing rod**
- Talk to **Navi** (player 2 has no fairy)

If player 2 presses a C button that has one of these items on it, nothing happens.

### Enemies and objects that only notice player 1
Some parts of the game still only check for player 1:

- **Grabbing enemies** such as Like Likes, Wallmasters and Dead Hands always grab player 1.
- **Floor switches** and other "stand here" triggers may only react to player 1.
- The **boomerang** returns to player 1.
- A few hazards that hurt by touch, rather than with an attack, may only notice player 1.
- Puzzles that need two players in two places at once don't exist in the original game, so the mod adds none.

### Screen and display
- Player 1's **rupee counter** stays in the bottom-left corner, over player 2's view.
- The **minimap** is hidden while the screen is split.
- The black **cutscene bars** at the top and bottom of the screen are turned off while the screen is split.
- Each view is wide and short (320×120), so the picture looks more zoomed out horizontally than normal.
- Sword trails and other effects are drawn twice per frame, so a few effects may flicker slightly.

### Saving and progress
- The save file is player 1's normal save. **Player 2's hearts and magic aren't saved.** Player 2 starts each session with full hearts.
- Story progress, items and flags are shared because they live in the one save file.

### Performance
- The game draws everything twice, so busy areas such as Hyrule Field and large rooms can slow down without a CPU overclock.
- The mod needs the Expansion Pak setting. Without it the game may run out of memory.

### Compatibility
- It only works with the **USA v1.2** ROM. Other versions (1.0, 1.1, PAL, GameCube, Master Quest) aren't supported.
- It doesn't support **original N64 hardware** or flash carts.
- It isn't compatible with randomizers or other ROM hacks.

---

## Version history

**v0.2**
- Fixed both players taking damage and playing the hurt animation when only one was hit.
- Fixed player 2 getting stuck being teleported back over and over next to a loading zone.
- Player 2 now reappears beside player 1 instead of behind them.

**v0.1**
- First release: splitscreen, player 2 on controller 2, shared equipment, separate hearts and magic, and player 2 hidden during cutscenes.

---

## Reporting problems
If you find a bug, write down where it happened (area or room), what each player was doing, and what you expected to happen.

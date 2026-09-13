# Reliqui Studio — build Pokémon fangames without ever opening RPG Maker XP

All-in-one editor for Pokémon Essentials, available in 6 languages.

Hi everyone! Reliqui Studio is a free desktop tool for creating Pokémon fangames on top of Pokémon Essentials (using the BES base — a Spanish edition with content up to Gen 9). I started my own fangame over 10 years ago in RPG Maker XP, picked it back up recently, and got frustrated going back to the same old tools (Notepad for the PBS files, a map editor from 2004, Editor.exe for trainers…). So I built my own: an all-in-one editor where you never touch RPG Maker XP at all — not even for battle animations anymore. Here's what it does.

## Download

➡ Get the latest installer from the [Releases page](../../releases)

Windows 10/11 (64-bit). No admin rights needed — it installs per-user.
The installer includes the tool, a clean copy of the base engine and an overworld sprite pack. Create your project from the Home tab and press ▶ Play.

📖 Guides and reference live in the [Wiki](../../wiki).

Interface available in **English, Spanish, German, French, Portuguese and Italian** (language selector right in the sidebar; adding another language is just a translation file, no recompiling).

## What's new

**🥊 Battle animation editor — the last RPG Maker XP holdout is gone.** Full visual editor for `Animations.rxdata`: frame-by-frame timeline, cell placement over the sprite sheet (position, zoom, angle, opacity, blend mode), live preview at RGSS-normal speed, duplicate/insert/delete frames and cells. This was the one thing that still forced you back into RPG Maker XP — not anymore.

**🗒 Quest/mission editor.** A dedicated tab to build the pause-menu quest log: create quests with ordered stages, give each one an ID to reference from your events, and hide the whole log behind a switch until you're ready to ship it. No more juggling switches and variables by hand to track "is this quest active."

**🌐 In-game content translator.** Scans every dialogue box and event text in the whole game and lists it in one searchable table where you edit the translation directly — separate from the tool's own interface language. This is the piece that was missing before: translating your *game's* content used to be entirely on you; now there's a built-in tool for it.

**🐾 Follower Pokémon.** The first Pokémon in your party walks behind the player — on foot, on bike, across surf and dive, through teleports — with options for what happens if it's fainted, whether it can be talked to, and a switch to hide it. Sprites are copied into the project automatically when you turn it on.

**👀 Visible overworld encounters.** Wild Pokémon roam the map before you battle them, à la Let's Go / Legends Arceus: pick which maps have them (coexisting with random encounters or replacing them), how many spawn at once, how often, how far they wander, how long they linger, and whether they show up on water too.

**💀 Nuzlocke mode.** A full ruleset toggle: one capture per zone (by map or by region), fainted Pokémon are gone for good, mandatory nicknames, mandatory shiny captures, a graveyard/memorial list — all wired into your events through `pbNuzlocke?`, `pbNuzlockeBurnZone`, `pbNuzlockeFreeZone` and `pbNuzlockeGraveList`.

**📋 Pokédex tasks (Legends Arceus-style).** "See, catch or evolve species X, Y times" research objectives with optional rewards, toggled from the same settings screen.

**🛠 Quality-of-life toggles.** Let players forget HM-only moves like any other move, and add a "Show EVs" button to the Pokémon summary screen (with a one-click reset to 0) — the two things every Essentials community asks for.

**🌍 Regional forms, per map.** New in the alternate-forms system: assign which maps spawn wild Pokémon already wearing their Alolan/Galarian/Hisuian/Paldean form, by map ID, no scripting required.

## How is it different from the usual RPG Maker XP + Essentials?

Essentials is a fantastic engine, but working with it means editing PBS files by hand in Notepad, using RPG Maker XP's map editor (three layers, no reliable undo), wrestling with Editor.exe for trainers and animations, and praying nothing gets corrupted. Reliqui Studio edits the exact same project files (PBS, maps, scripts), but:

| Before (RMXP + Essentials) | With Reliqui Studio |
|---|---|
| PBS files by hand in Notepad | Visual editors: Pokédex with sprites, clickable type chart, encounters, items, moves, trainers |
| RMXP map editor: 3 layers, no reliable Ctrl+Z | Up to 8 layers, undo, paint bucket, copy/paste regions, autotiles with automatic borders |
| Map connections by typing coordinates into `connections.txt` | Visual canvas: drag dozens of maps around, snap them edge to edge, and the connections write themselves |
| Events through the RMXP editor | Full event editor + 1-click recipes: NPC, sign, shop, nurse, trainer, teleport with auto-return, harbor |
| Battle animations through Editor.exe | Full visual animation editor: frame timeline, cell placement, live preview |
| Quest/flag tracking by hand with switches | Dedicated quest editor with ordered stages and a pause-menu log |
| Translating your game's content | Built-in scanner + editor for every dialogue and event text in the game |
| Forms and regional variants by writing Ruby handlers | Visual forms editor with sprite slots and per-map regional spawning |
| No version control | Built-in Git: a "Save version" button plus automatic backups before every save |
| Sharing your game = copying the folder with everything exposed | Encrypted export (RGSSAD) + installer generator |

## Standout features

**Multiple shiny variants.** Every species can have several alternative shinies with conditions: custom rarity, weather, time of day, season, specific maps, a game switch, level range… or manual activation for gifts/bosses. The palette editor lets you pick new colors right on top of the original sprite, and the recolor applies at once to the front, back, icon and walking sprites — no drawing required.

**Alternate forms & regional variants.** Give any species extra forms from the Pokédex tab — different types, stats, abilities, movesets, size and Pokédex entry, each with its own sprites. Any field you leave empty is inherited from the base form. Mark which maps spawn wild Pokémon already wearing the form and you have your own regional variants, exactly like the engine's Alolan or Galarian ones.

**Level scaling by progress.** For long or multi-region adventures: wild Pokémon and trainer teams adjust to your party's average level (trainers keep their internal level spread and their custom movesets). Toggle it on and off with a switch from your own events.

**Gen 5 seasons + inter-region travel.** Real seasons (with Deerling/Sawsbuck forms), forceable for testing content; plus a travel system with destinations you unlock via switches, all managed visually.

**Battle mechanics toggles.** Turn Mega Evolution, Z-Moves, Dynamax or Terastallization off for your whole game with a checkbox — the button disappears from battle (for you and for rivals) and the interruptor locks them out story-side too.

**Fakemon wizard.** Create a complete species in one step: data, sprites automatically renamed into place, and an auto-generated shiny with a hue shift you tune live.

**Move effect picker.** All 457 engine effects, searchable in plain language ("burn", "drain", "raises Attack"…) with examples of which moves already use each one. Goodbye hex function codes.

**Damage/balance calculator, project notes & to-dos, common events with named switches, safe autosave, PC boxes from the pause menu, project health check** (finds broken references across the whole game) **, and a Play button that compiles and launches your game instantly** (mkxp-z runtime: resizable window, vsync, Alt+Enter fullscreen).

## How does it work under the hood?

A desktop app that edits the real files of your Essentials project — no weird proprietary formats. If you ever want to go back to RMXP, your project stays 100% compatible.

- Byte-for-byte verified writing of `.rxdata` files, and automatic rotating backups before every save.
- Multi-project: import any Essentials v9–v18 project (and it reads modern v19–v21 ones too).
- When you export your game, the data is encrypted into a `Game.rgssad` — nobody can casually open your maps or scripts.

ℹ **Note on languages:** the tool's interface is fully translated (6 languages). The game content that ships with the BES base engine (moves, items, dialogue) is in Spanish — the built-in translator tab is there to help you localize your own project's content.

Credits: Pokémon Essentials (Maruno and contributors), BES Spanish edition, mkxp-z runtime.

https://buymeacoffee.com/andyu19

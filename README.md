# Reliqui Studio 1.0.1 — build Pokémon fangames without ever opening RPG Maker XP

*All-in-one editor for Pokémon Essentials, English/Spanish.*

Hi everyone! I'd like to introduce **Reliqui Studio**, an application I've been building for my own fangame and decided to polish up to share. I started my project over 10 years ago in RPG Maker XP, picked it back up this year, and got so frustrated going back to the same old tools (Notepad for the PBS files, a map editor from 2004…) that I ended up building my own: an all-in-one editor for Pokémon Essentials where you never touch RPG Maker at all. Here's what it does — I'd love to hear what you think.

Reliqui Studio is a free desktop tool for creating Pokémon fangames on top of Pokémon Essentials (using the BES base — a Spanish edition with content up to Gen 9). The idea is simple: everything that used to force you to juggle RPG Maker XP, Notepad and a dozen tutorials now lives in a single application with a modern interface — available in **Spanish and English** out of the box (language selector right in the sidebar; adding another language is just a config file, no recompiling).

<!-- SCREENSHOT 1: Home Screen -->
<img width="1486" height="943" alt="image" src="https://github.com/user-attachments/assets/1976753b-2608-4cf5-932d-3f59b1e2be27" />

## How is it different from the usual RPG Maker XP + Essentials?

Essentials is a fantastic engine, but working with it means: editing PBS files by hand in Notepad, using RPG Maker XP's map editor (from 2004, 3 layers, no reliable undo), wrestling with `Editor.exe` for trainers, and praying nothing gets corrupted. Reliqui Studio edits the **exact same project files** (PBS, maps, scripts), but:

| Before (RMXP + Essentials) | With Reliqui Studio |
|---|---|
| PBS files by hand in Notepad | Visual editors: Pokédex with sprites, clickable type chart, encounters, items, moves, trainers |
| RMXP map editor: 3 layers, no reliable Ctrl+Z | Up to 8 layers, undo, paint bucket, copy/paste regions, autotiles with automatic borders |
| Map connections by typing coordinates into `connections.txt` | Visual canvas: drag dozens of maps around, snap them edge to edge, and the connections write themselves |
| Events through the RMXP editor | Full event editor + 1-click recipes: NPC, sign, shop, nurse, trainer, teleport with auto-return, harbor |
| No version control | Built-in Git: a "Save version" button plus automatic backups before every save |
| Sharing your game = copying the folder with everything exposed | Encrypted export (RGSSAD) + installer generator |

<!-- SCREENSHOT 2: Map editor -->
<img width="1486" height="943" alt="image" src="https://github.com/user-attachments/assets/0294db4f-e133-40fa-8eea-b4ed179c2ff8" />

<!-- SCREENSHOT 3: World editor -->
<img width="1486" height="943" alt="image" src="https://github.com/user-attachments/assets/40802747-f2ac-4e4c-96b3-761402795cae" />


**Multiple shiny variants.** Every species can have several alternative shinies with conditions: custom rarity, weather, time of day, season, specific maps, a game switch, level range… or manual activation for gifts/bosses. And the best part: the palette editor — you pick new colors right on top of the original sprite, and the recolor applies at once to the front, back, icon and walking sprites. No drawing required.

<!-- SCREENSHOT 4: Shiny variant editor -->
<img width="1486" height="943" alt="image" src="https://github.com/user-attachments/assets/c8df52f6-ab09-461d-8768-929e1d314544" />


**Level scaling by progress.** For long or multi-region adventures: wild Pokémon and trainer teams adjust to your party's average level (trainers keep their internal level spread and their custom movesets). Toggle it on and off with a switch from your own events.

**Gen 5 seasons + inter-region travel.** Real seasons (with Deerling/Sawsbuck forms), forceable for testing content; plus a travel system with destinations you unlock via switches, all managed visually.

**Fakemon wizard.** Create a complete species in one step: data, sprites automatically renamed into place, and an auto-generated shiny with a hue shift you tune live. *(Icons and sprites in the screenshot were taken from the internet as examples.)*

<!-- SCREENSHOT 5: Fakemon editor -->
<img width="1486" height="943" alt="image" src="https://github.com/user-attachments/assets/9050f0f2-0860-4e05-bcd5-3c3958eea88e" />


**Move effect picker.** All 457 engine effects, searchable in plain language ("burn", "drain", "raises Attack"…) with examples of which moves already use each one. Goodbye hex function codes.

<!-- SCREENSHOT 6: Effect picker -->
<img width="1486" height="943" alt="image" src="https://github.com/user-attachments/assets/8261df80-8fad-448a-9c93-bacd04a2bb6a" />


Damage/balance calculator, project notes & to-dos, common events with named switches, safe autosave, PC boxes from the pause menu, project health check (finds broken references across the whole game)… plus a **Play** button that compiles and launches your game instantly (mkxp-z runtime: resizable window, vsync, Alt+Enter fullscreen).

## How does it work under the hood?

A desktop app that edits the real files of your Essentials project — no weird proprietary formats. If you ever want to go back to RMXP, your project stays 100% compatible.

- Byte-for-byte verified writing of `.rxdata` files, and automatic rotating backups before every save. In months of development I haven't lost a single file.
- Multi-project: import any Essentials v9–v18 project (and it reads modern v19–v21 ones too).
- When you export your game, the data is encrypted into a `Game.rgssad` — nobody can casually open your maps or scripts.

**Credits:** Pokémon Essentials (Maruno and contributors), BES Spanish edition, mkxp-z runtime.

https://buymeacoffee.com/andyu19

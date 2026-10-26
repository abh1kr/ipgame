# Origin

A single-file, browser-playable 16-bit pixel-art action RPG.

## Run

Open `index.html` in any modern browser. No build step and no dependencies.
If your browser restricts local file access, serve the directory:

    python3 -m http.server 8000

Then visit http://localhost:8000.

## Controls

| Action | Key |
| --- | --- |
| Move | WASD / Arrow keys / left touch joystick |
| Skill slot 1 | Left mouse button |
| Skill slot 2 | Right mouse button |
| Skill slot 3 | Q |
| Skill slot 4 | E |
| Dash | Space (invulnerable during dash) |
| Health potion | 1 |
| Mana potion | 2 |
| Interact | F |
| Return to town | T |
| Inventory | I |
| Character panel | C |
| Skill tree | K |
| Toggle music | M |
| Help | H |
| Pause | Esc |

## Features

- Three classes (Warrior, Mage, Ranger), each with three skill branches
- Ten zones with distinct environments and a boss per zone
- Procedural pixel art and chiptune music, no external asset files
- Real-time combat, loot, affixes, reforging, bounties, shared vault, multi-character accounts
- Day/night cycle and local save via `window.storage` when available

## Developer / Tester Tools

Enabled by default in the shipped file. Four ways to access:

1. **Pause menu** -- Esc, then click **Dev Tools**.
2. **Keyboard shortcuts** (while in-game):
   - `Ctrl+Shift+U` -- Unlock Everything
   - `Ctrl+Shift+R` -- Reset Test Unlocks
   - `Ctrl+Shift+D` -- Open the Dev Tools panel directly
3. **URL parameter** -- append to the page URL:
   - `?cheat=unlock` -- apply Unlock Everything as soon as a character loads
   - `?cheat=reset` -- apply Reset Test Unlocks as soon as a character loads
4. **Browser console**:
   ```js
   originCheat.unlock()          // Unlock Everything
   originCheat.unlockLevels()    // Levels only
   originCheat.unlockAbilities() // Abilities only
   originCheat.reset()           // Reset test unlocks
   originCheat.info()            // Print current unlock state

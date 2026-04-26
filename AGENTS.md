# DDP (Dia Del Petardo)

Wintermute Engine adventure game.

## Dev Tools

- **ProjectMan** - Compile project → outputs to `packages/`
- **SceneEdit** - Edit scenes (`.scene` files)
- Run `packages/ddp.exe` to test

## Structure

- `data/` - Game content (scenes, actors, scripts, sprites, items, music, UI)
- `data/default.game` - Game definition (entry point)
- `data/scenes/` - Scene folders (each has `.scene` file + `scr/` subfolder)
- `data/scripts/` - Global scripts (`game.script`, `game_loop.script`, `*.inc`)
- `packages/` - Compiled output (`ddp.exe`, `data.dcp`)

## Scripts

- Wintermute scripting language (`.script` files)
- `#include` pulls in `.inc` header files
- Entry: `default.game` → `scripts\game.script`
- Actor: `actors\marcelo\marcelo.actor`

## Notes

- Spanish-language game (verbs: "Ir a", "Agarrar", "Mirar", "Usar", etc.)
- Line endings: CRLF (Windows) - don't change git autocrlf
- Remote: `git@github.com:morhook/ddp.git`
- Published: https://morhook.itch.io/dia-del-petardo

# DDP (Dia Del Petardo)

Wintermute Engine 1.x adventure game. Windows-only toolchain.

## Dev

- **ProjectMan** -- compile project, outputs to `packages/` (Windows GUI only, no CLI)
- **SceneEdit** -- edit `.scene` files (Windows GUI only)
- Run `packages/ddp.exe` to test
- No lint/test/typecheck pipeline exists

## Repo Layout

- `data/default.game` -- game definition / entry point
- `data/scripts/` -- global scripts: `game.script` (entry), `game_loop.script`, `scene.script` (shared per-scene), `base.inc`, `const.inc`, `keys.inc`
- `data/scenes/<name>/` -- scenes with `.scene` file + `scr/` subfolder for per-scene scripts
- `data/actors/marcelo/` -- main actor; `data/actors/chancho/`
- `data/items/`, `data/interface/`, `data/fonts/`, `data/sprites/`, `data/music/`, `data/ui_elements/`
- `packages/` -- compiled output (`ddp.exe`, `data.dcp`); gitignored
- `*.xcf` -- GIMP source files, excluded from compiled package
- Scene scripts under `data/scenes/<name>/scr/`

## Scripting

- Wintermute scripting language (`.script` files)
- `#include` pulls in `.inc` header files at source level; `.inc` files are excluded from the compiled `data.dcp` (see `ddp.wpr` filter)
- Entry chain: `default.game` → `scripts\game.script` → attaches `game_loop.script`

## Conventions

- Spanish-language game -- verbs: "Ir a", "Agarrar", "Mirar", "Usar", "Dar", "Abrir", "Cerrar", "Empujar", "Tirar", "Hablar"
- CRLF line endings enforced via `.gitattributes` -- do not change

# Project Naming Conventions

## Whole project

The whole project should follow the [Snake Case](https://en.wikipedia.org/wiki/Snake_case) naming system. This means that folder names and file names should both be in lowercase and separated by underscores.

## Asset organization

Assets live in the `/assets` directory, and are sorted based on their parent project. All assets for a project should be contained in `/assets/proj/<project_name>`, known as the **Project Asset Root** (PAR). The PAR may be used in file paths in this document as `$PAR`.

| Asset Type            | Production Asset Path |
|-----------------------|-----------------------|
| Characters & Entities | `$PAR/prod/chr`       |
| Scene Objects         | `$PAR/prod/obj`       |
| World Maps            | `$PAR/prod/wld`       |
| Audio                 | `$PAR/prod/aud`       |


## Example asset paths

Imagine an example game with:

- A character named "Henry"
  - Has `default` variant
  - Has `powerup` variant
- A world called `world_0`
  - Has a single tileset for the world

The file structure *might* look something like this:

```text
$PAR
└── prod
    ├── chr
    │   └── henry
    │       ├── default
    │       │   ├── harmony
    │       │   │    └── <harmony-21 files>
    │       │   ├── renders
    │       │   │    ├── run_sprites.png
    │       │   │    ├── run_sprites.json
    │       │   │    ├── walk_sprites.png
    │       │   │    ├── walk_sprites.json
    │       │   │    ├── jump_sprites.png
    │       │   │    ├── jump_sprites.json
    │       │   │    ├── sit_sprites.png
    │       │   │    └── sit_sprites.json
    │       │   └── henry_default.procreate
    │       └── powerup
    │           └── <like above>
    └── wld
        └── world_0
            ├── tileset
            │   ├── tiles.ase
            │   ├── tiles.tsx
            │   └── tiles.png
            ├── world_0_layer_0.png
            ├── world_0_layer_1.png
            └── world_0.tmx
```

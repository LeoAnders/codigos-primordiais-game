# Estrutura do projeto (pasta → responsabilidade)

Este documento define **onde colocar cada tipo de coisa**. A ideia é evitar “cada um faz de um jeito” e facilitar colaboração.

## Árvore (visão geral)

Esta árvore representa a **estrutura-alvo da fase 0**. Pode haver pastas adicionais enquanto o projeto evolui, mas a organização base deve seguir este padrão.

```
projeto_codigos_primordiais/
├── addons/
├── assets/
│   ├── audio/
│   │   ├── music/
│   │   │   ├── arithma/
│   │   │   ├── geometra/
│   │   │   ├── probabilis/
│   │   │   ├── algebrax/
│   │   │   ├── cosmara/
│   │   │   └── main_theme/
│   │   └── sfx/
│   │       ├── ui/
│   │       ├── ambiente/
│   │       └── combate/
│   ├── fonts/
│   ├── sprites/
│   │   ├── personagens/
│   │   ├── planetas/
│   │   ├── ui/
│   │   └── tilesets/
│   └── vfx/
│       ├── particulas/
│       └── shaders/
├── data/
│   ├── enigmas/
│   │   ├── arithma.json
│   │   ├── geometra.json
│   │   ├── probabilis.json
│   │   ├── algebrax.json
│   │   └── cosmara.json
│   ├── dialogos/
│   └── progressao/
│       └── configuracao_niveis.json
├── resources/
│   ├── materials/
│   ├── shaders/
│   ├── fonts/
│   └── tilesets/
├── scenes/
│   ├── main/
│   │   └── main.tscn
│   ├── gameplay/
│   │   ├── calculon/
│   │   └── planets/
│   │       ├── arithma/
│   │       ├── geometra/
│   │       ├── probabilis/
│   │       ├── algebrax/
│   │       └── cosmara/
│   ├── entities/
│   │   ├── player/
│   │   ├── npcs/
│   │   └── enemies/
│   ├── ui/
│   │   ├── menus/
│   │   ├── hud/
│   │   └── dialogos/
│   └── systems/
├── scripts/
│   ├── autoload/
│   ├── systems/
│   ├── entities/
│   │   ├── player/
│   │   ├── npc/
│   │   └── enemy/
│   ├── ui/
│   └── utils/
├── docs/
├── tests/
├── project.godot
└── README.md
```

## Root

- `addons/` — plugins e ferramentas externas (ex.: GUT no futuro)
- `assets/` — arquivos brutos (imagens, áudio, fontes) — veja [`ASSET_GUIDE.md`](./ASSET_GUIDE.md)
- `data/` — dados do jogo (JSON/CSV): enigmas, diálogos, progressão
- `resources/` — recursos do Godot (`.tres`, `.res`, `.gdshader`)
- `scenes/` — cenas (`.tscn`)
- `scripts/` — scripts (`.gd`) — padrões em [`CODING_STANDARDS_GDSCRIPT.md`](./CODING_STANDARDS_GDSCRIPT.md)
- `docs/` — documentação do projeto (como este arquivo) — índice em [`README.md`](./README.md)
- `tests/` — testes (opcional; se/quando adotarmos)

## `assets/` (brutos)

- `assets/audio/music/<planeta>/` — músicas por planeta (`arithma`, `geometra`, `probabilis`, `algebrax`, `cosmara`)
- `assets/audio/music/main_theme/` — música tema geral
- `assets/audio/sfx/{ui,ambiente,combate}/` — efeitos sonoros
- `assets/sprites/{personagens,planetas,ui,tilesets}/` — sprites organizados
- `assets/fonts/` — fontes
- `assets/vfx/{particulas,shaders}/` — vfx brutos (shaders finais preferimos em `resources/shaders/`)

## `data/` (JSON/CSV)

- `data/enigmas/<planeta>.json` — enigmas por planeta
- `data/dialogos/` — diálogos (por personagem ou planeta)
- `data/progressao/configuracao_niveis.json` — progressão/níveis

## `scenes/` (Godot)

- `scenes/main/main.tscn` — cena de entrada/launcher
- `scenes/gameplay/calculon/` — hub (nave Calculon)
- `scenes/gameplay/planets/<planeta>/` — cenas por planeta
- `scenes/entities/{player,npcs,enemies}/` — entidades
- `scenes/ui/{menus,hud,dialogos}/` — UI
- `scenes/systems/` — suporte (se necessário)

## `scripts/` (GDScript)

- `scripts/autoload/` — singletons (autoloads)
- `scripts/systems/` — sistemas (enigma, diálogo, progressão, etc.)
- `scripts/entities/` — comportamento de entidades
- `scripts/ui/` — lógica de UI
- `scripts/utils/` — utilitários

## Onde coloco X?

- “Nova música do planeta Arithma” → `assets/audio/music/arithma/`
- “Sprite do player” → `assets/sprites/personagens/`
- “Novo enigma (com randomização)” → `data/enigmas/<planeta>.json`
- “Cena de menu” → `scenes/ui/menus/`
- “Script do sistema de enigmas” → `scripts/systems/`
- “Shader final do jogo” → `resources/shaders/`

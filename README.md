# Códigos Primordiais

[![Godot](https://img.shields.io/badge/Godot-4.6-478CBF?logo=godot-engine&logoColor=white)](https://godotengine.org)
[![GDScript](https://img.shields.io/badge/Language-GDScript-355570)](https://docs.godotengine.org/en/stable/getting_started/scripting/gdscript/index.html)
[![License](https://img.shields.io/badge/License-Private-lightgrey)](./LICENSE)

## Sumário

- [Visão geral](#visão-geral)
- [Objetivo do Projeto](#objetivo-do-projeto)
- [Requisitos](#requisitos)
- [Como rodar](#como-rodar)
- [Documentação](#documentação)
- [Como contribuir](#como-contribuir)
- [Estrutura do repositório](#estrutura-do-repositório)
- [Licença](#licença)

## Visão geral

Códigos Primordiais é um RPG educativo de narrativa espacial. Cada planeta representa um eixo matemático, e a matemática aparece como **enigmas integrados à história**, não como combate.

- **Planetas:** Arithma, Geometra, Probabilis, Algebrax, Cosmara
- **Hub:** a nave **Calculon**
- **Antagonista:** Entropy (corrupção dos Códigos Primordiais)

O jogador viaja entre mundos para restaurar os Códigos Primordiais e reverter o colapso de cada planeta.

## Objetivo do Projeto

- **Pedagógico:** apoiar a aprendizagem de matemática com problemas contextualizados e progressivos.
- **Narrativo:** conectar conteúdo matemático à identidade de cada planeta, dando sentido às tarefas.
- **Acadêmico:** estruturar um projeto colaborativo com padrões claros para o time.

## Requisitos

- **Godot 4.6** (conforme `project.godot`)
- Git (para colaboração)

## Como rodar

1. Clone o repositório:

```bash
git clone https://github.com/LeoAnders/codigos-primordiais-game.git
cd codigos-primordiais-game
```

2. Abra a Godot e selecione **Import** (ou **Open**).
3. Escolha a pasta do repositório (onde está o `project.godot`).
4. Rode o projeto (Play).

> Nota: se aparecer um alerta de “main scene not defined”, selecione `scenes/main/main.tscn` como cena principal.

## Documentação

A porta de entrada da documentação é [`docs/README.md`](./docs/README.md).

## Como contribuir

Leia o guia em [`CONTRIBUTING.md`](./CONTRIBUTING.md).

## Estrutura do repositório

Estrutura detalhada em [`docs/STRUCTURE.md`](./docs/STRUCTURE.md). Abaixo um resumo mais completo:

```text
codigos-primordiais-game/
├── addons/               # Plugins externos
├── assets/               # Recursos visuais e áudio
│   ├── audio/
│   │   ├── music/        # Músicas por planeta + tema
│   │   └── sfx/          # UI, ambiente, combate
│   ├── sprites/          # Personagens, planetas, UI, tilesets
│   ├── fonts/            # Fontes
│   └── vfx/              # Partículas e shaders brutos
├── data/                 # Dados do jogo (JSON, CSV)
│   ├── enigmas/          # Enigmas por planeta
│   ├── dialogos/         # Diálogos
│   └── progressao/       # Configuração de níveis
├── docs/                 # Documentação versionada
├── resources/            # Resources do Godot (.tres, .res, .gdshader)
│   ├── materials/
│   ├── shaders/
│   ├── fonts/
│   └── tilesets/
├── scenes/               # Cenas do jogo
│   ├── main/             # Cena inicial
│   ├── gameplay/         # Calculon + planetas
│   ├── entities/         # Player, NPCs, inimigos
│   ├── ui/               # Menus, HUD, diálogos
│   └── systems/          # Cenas de suporte
├── scripts/              # Código GDScript
│   ├── autoload/         # Singletons
│   ├── systems/          # Sistemas (enigma, diálogo, progressão)
│   ├── entities/         # Player, NPC, enemy
│   ├── ui/               # Lógica de UI
│   └── utils/            # Utilitários
├── tests/                # Testes (quando aplicável)
└── project.godot         # Configuração do projeto
```

## Licença

Este repositório é privado para fins acadêmicos.

Veja [`LICENSE`](./LICENSE) para mais detalhes.

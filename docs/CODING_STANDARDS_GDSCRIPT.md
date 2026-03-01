# Padrões de código (Godot / GDScript)

Objetivo: manter o projeto **legível e colaborativo**, mesmo com pessoas em níveis diferentes.

## Nomes (arquivos e pastas)

- Use `snake_case` para pastas e arquivos.
- Cenas: `snake_case.tscn`
- Scripts: `snake_case.gd`
- Recursos: `snake_case.tres`, `snake_case.gdshader`

Planetas (slugs fixos):

- `arithma`, `geometra`, `probabilis`, `algebrax`, `cosmara`

## Organização (onde criar coisas)

Use [`STRUCTURE.md`](./STRUCTURE.md) como “mapa do projeto”. Regra prática:

- **feature por planeta** fica agrupada em `scenes/gameplay/planets/<planeta>/` e `data/enigmas/<planeta>.json`
- **sistemas gerais** ficam em `scripts/systems/`

## Estilo (GDScript)

- Indentação: **4 espaços**
- Uma responsabilidade por script (evite scripts “faz tudo”)
- Funções curtas e nomes claros (`verb_objeto` quando possível)

## Tipagem (gradual)

Use tipagem gradualmente, principalmente em sistemas centrais:

- Parâmetros e retornos tipados em funções públicas
- Variáveis tipadas quando ficar ambíguo

Não é para travar prototipagem; é para reduzir bugs e facilitar leitura.

## `class_name` (quando usar)

Use `class_name` quando:

- for um tipo reutilizável (ex.: `DialogueLine`, `Enigma`, `GameManager`)
- você quiser autocompletar e padronizar uso no editor

Evite `class_name` em scripts extremamente locais/temporários.

## Autoloads (singletons)

- Só criar autoload quando for realmente global
- Coloque em `scripts/autoload/`
- Mantenha API pequena e estável (para não virar “Deus-objeto”)

## Assets e imports

- Não renomeie/mova assets sem avisar o time (pode quebrar referências)
- Não apague `.import` sem entender o impacto

Guia: [`ASSET_GUIDE.md`](./ASSET_GUIDE.md).

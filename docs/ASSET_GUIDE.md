# Guia de assets (arte/áudio/fontes)

Este guia ajuda a manter `assets/` organizado e evita que o projeto vire uma “pasta downloads”.

## Regras rápidas

1. Coloque arquivos em `assets/` no lugar certo (ver [`STRUCTURE.md`](./STRUCTURE.md)).
2. Use `snake_case` em nomes de arquivo.
3. Evite mover/renomear assets já usados em cenas sem combinar com o time.

## Nomenclatura sugerida

- Sprites: `nome_variacao_tamanho.png` (ex.: `eco_idle_64.png`)
- UI: `ui_nome_estado.png` (ex.: `ui_botao_confirm_hover.png`)
- SFX: `sfx_contexto_acao.wav` (ex.: `sfx_ui_click.wav`)
- Música: `music_planeta_tema.ogg` (ex.: `music_arithma_market.ogg`)

## Importação (Godot)

- Ao adicionar assets, abra o projeto no editor para a Godot gerar/importar metadados.
- Não apague arquivos `*.import` sem motivo (eles guardam configurações de importação).

## Créditos e licenças de terceiros

Se você adicionar qualquer asset de terceiros:

1. Salve o texto da licença em `licences/` (ou um arquivo `licences/<nome_do_pacote>.txt`; veja [`LICENSE`](../LICENSE) para contexto).
2. Anote a fonte e as condições de uso (link, autor, licença).

Mesmo em repositório privado, isso evita problemas e ajuda a organizar o projeto.

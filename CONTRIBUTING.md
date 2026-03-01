# Contribuindo para Códigos Primordiais

Este documento define como contribuir de forma organizada e segura para o projeto.

## 1) Setup rápido

1. Clone o repositório.
2. Abra a Godot (**4.6**) e importe/abra o projeto pelo `project.godot` (veja também [`README.md`](./README.md)).
3. Rode o projeto pelo Play.

> Se a Godot pedir "main scene", selecione `scenes/main/main.tscn` (detalhes em [`README.md`](./README.md)).

## 2) Convenção de branches (PT-BR)

Use o padrão e **nomes em PT-BR**:

```
tipo/descricao-curta
```

Tipos permitidos:

- `feat/` → nova funcionalidade
- `fix/` → correção de bug
- `chore/` → organização, limpeza ou manutenção
- `refactor/` → melhoria interna sem alterar comportamento
- `docs/` → alterações apenas na documentação
- `data/` → alterações em arquivos de dados (JSON/CSV)

Exemplos (em PT-BR):

- `feat/sistema-enigmas`
- `fix/erro-progressao`
- `chore/organiza-assets`
- `docs/atualiza-roadmap`

## 3) Fluxo de trabalho (feature branch)

1. **Antes de começar:** sincronize a `main`

```bash
git checkout main
git pull
```

2. **Crie sua branch**

```bash
git checkout -b tipo/nome-curto
```

3. Trabalhe em mudanças pequenas e focadas.

4. Antes de dar push:
   - Abra o projeto na Godot.
   - Rode o Play pelo menos uma vez.

5. Envie sua branch:

```bash
git push -u origin tipo/nome-curto
```

6. Abra um Pull Request (PR) para `main` e solicite revisão.

## 4) Resolvendo conflitos

Se houver conflito no PR:

1. Atualize sua branch:

```bash
git checkout main
git pull
git checkout sua-branch
git merge main
```

2. Resolva os conflitos.

3. Rode o projeto novamente.

4. Faça commit da resolução.

5. Dê push.

Conflitos são normais em trabalho em equipe. Resolva com cuidado.

## 5) Organização do projeto

Mapa completo em [`docs/STRUCTURE.md`](./docs/STRUCTURE.md).

Atalhos rápidos:

- **Sprites/arte/áudio:** `assets/` (ver [`docs/ASSET_GUIDE.md`](./docs/ASSET_GUIDE.md))
- **Dados (JSON/CSV):** `data/`
- **Cenas Godot (.tscn):** `scenes/`
- **Scripts (.gd):** `scripts/`
- **Resources (.tres/.res/.gdshader):** `resources/`
- **Documentação:** `docs/` (entrada em [`docs/README.md`](./docs/README.md))

## 6) Convenções de nomes

Use **snake_case** para arquivos e pastas:

- `minha_cena.tscn`
- `player_controller.gd`
- `configuracao_niveis.json`

Planetas usam slugs fixos:

- `arithma`
- `geometra`
- `probabilis`
- `algebrax`
- `cosmara`

## 7) Padrões de código (GDScript)

Guia completo em [`docs/CODING_STANDARDS_GDSCRIPT.md`](./docs/CODING_STANDARDS_GDSCRIPT.md).

Resumo:

- Prefira scripts pequenos e com responsabilidade clara.
- Use tipagem gradual, especialmente em sistemas centrais.
- Elementos globais devem ficar em `scripts/autoload/` e ser documentados.

## 8) Adicionando assets

1. Coloque o arquivo em `assets/` no local correto.
2. Abra o projeto na Godot para que o import aconteça.
3. Não apague arquivos `.import` sem motivo.

Se alterar configurações de importação, mencione no PR.

Guia completo: [`docs/ASSET_GUIDE.md`](./docs/ASSET_GUIDE.md).

## 9) Cuidados específicos do Godot

- Evite editar a mesma cena que outra pessoa esteja modificando.
- Não remova arquivos `.import`.
- Se alterar `project.godot`, explique claramente o motivo no PR.
- Sempre teste a cena modificada antes de enviar.

## 10) Padrão de commits (PT-BR)

Formato (descrição em PT-BR):

```
tipo: descrição curta no imperativo
```

Exemplos (PT-BR):

- `feat: adiciona sistema base de enigmas`
- `fix: corrige cálculo de pontuação`
- `docs: atualiza guia de assets`
- `chore: reorganiza estrutura de pastas`

### Conventional Commits

Usamos o padrão de tipos do **Conventional Commits**. Leia o guia oficial:

[https://www.conventionalcommits.org/pt-br/v1.0.0/](https://www.conventionalcommits.org/pt-br/v1.0.0/)

## 11) Checklist antes do push

- [ ] Rodei o projeto na Godot (Play) pelo menos uma vez
- [ ] Coloquei arquivos nas pastas corretas
- [ ] Usei nomes em `snake_case`
- [ ] Minha mudança é pequena e focada
- [ ] Expliquei claramente o que foi feito no PR

Contribuições que não seguirem este guia podem ser solicitadas para ajuste antes do merge.

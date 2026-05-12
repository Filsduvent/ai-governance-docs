# Politica e Governanca de IA

Documentacao estrategica para apoiar a construcao de uma politica corporativa de uso de Inteligencia Artificial, com foco em governanca, seguranca, padronizacao, rastreabilidade e inovacao controlada.

## Objetivo da documentacao

Este projeto organiza a narrativa executiva sobre a evolucao da empresa:

1. Em 2024, surgiu um desafio **data-driven** relacionado a organizacao, integracao e governanca de dados.
2. Como resposta, foi construido um **datalake** para centralizar informacoes e apoiar decisoes.
3. Entre 2024 e 2026, a area de tecnologia evoluiu de uma atuacao predominantemente operacional para uma logica mais orientada a dados, inteligencia e automacao.
4. Em 2026, o crescimento do uso de **IA generativa**, **vibe coding** e ferramentas de produtividade cria um novo desafio institucional.
5. A documentacao compara dois cenarios:
   - uso de IA sem governanca;
   - uso de IA com governanca.
6. O resultado esperado e apoiar a definicao de uma politica clara de IA para a empresa.

## Estrutura do projeto

```text
.
|-- .github/workflows/deploy.yml
|-- assets/
|   |-- images/
|   `-- slides/
|-- docs/
|   |-- assets/images/
|   |-- stylesheets/extra.css
|   |-- index.md
|   |-- contexto.md
|   |-- evolucao-tecnologia.md
|   |-- uso-sem-governanca.md
|   |-- uso-com-governanca.md
|   |-- politica-ia.md
|   `-- referencias.md
|-- mkdocs.yml
`-- README.md
```

### Componentes principais

- `docs/`: paginas da documentacao publicavel.
- `docs/assets/images/`: imagens utilizadas no site MkDocs.
- `docs/stylesheets/extra.css`: customizacoes visuais para aparencia executiva.
- `assets/images/`: arquivos fonte das imagens da apresentacao.
- `assets/slides/`: materiais complementares em formato de apresentacao.
- `mkdocs.yml`: configuracao do MkDocs Material.
- `.github/workflows/deploy.yml`: automacao de publicacao no GitHub Pages.

## Como instalar dependencias

Recomenda-se o uso de ambiente virtual Python.

```bash
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install mkdocs mkdocs-material
```

## Como rodar localmente

Com as dependencias instaladas:

```bash
mkdocs serve
```

Depois, acesse o endereco local indicado pelo MkDocs no terminal, normalmente:

```text
http://127.0.0.1:8000/
```

## Como gerar o site estatico

Para validar a compilacao da documentacao:

```bash
mkdocs build
```

O resultado sera gerado no diretorio `site/`.

## Como publicar no GitHub Pages

A publicacao e feita por GitHub Actions usando o workflow:

```text
.github/workflows/deploy.yml
```

O fluxo executa automaticamente quando houver push na branch `main` e realiza:

1. checkout do repositorio;
2. configuracao do Python;
3. instalacao de `mkdocs` e `mkdocs-material`;
4. deploy com:

```bash
mkdocs gh-deploy --force
```

O workflow utiliza a permissao:

```yaml
permissions:
  contents: write
```

Essa permissao permite atualizar a branch usada pelo GitHub Pages durante o deploy.

## Fluxo de trabalho do projeto

Este projeto foi estruturado com o seguinte fluxo:

```text
Codex
  + MCP_DOCKER
  + GitHub MCP
  + MkDocs Material
  + GitHub Pages
```

### Como esse fluxo funciona

| Etapa | Papel |
| --- | --- |
| Codex | Apoio na criacao, revisao e organizacao da documentacao |
| MCP_DOCKER | Camada de acesso a ferramentas MCP usadas no processo |
| GitHub MCP | Criacao e atualizacao remota de repositorios, branches e arquivos |
| MkDocs Material | Geracao do site de documentacao com navegacao e identidade visual |
| GitHub Pages | Publicacao automatizada do conteudo estatico |

## Proximos passos

- Revisar a narrativa executiva com as areas responsaveis.
- Validar linguagem, exemplos e imagens com stakeholders.
- Consolidar a primeira versao da politica corporativa de IA.
- Evoluir a pagina de referencias com normas, frameworks e documentos internos.
- Ajustar o workflow de publicacao conforme a estrategia final de Pages.
- Avaliar inclusao de novas secoes, como:
  - papeis e responsabilidades;
  - processo de avaliacao de risco;
  - catalogo de casos de uso;
  - ferramentas aprovadas;
  - perguntas frequentes.

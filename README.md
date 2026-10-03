# deep

Página da disciplina de Deep Learning — Engenharia Elétrica, UFMT.
Publicada pelo GitHub Pages a partir de `index.html`.

## Organização

- `index.html`, `estilo.css` — página da disciplina (layout herdado de Microcontroladores).
- `notebooks/aulaNN_alunos.ipynb` — notas de aula publicadas, com as células `# AO VIVO` vazias.
- `notebooks/aulaNN_professor.ipynb` — versão completa, **fora do git** (ver `.gitignore`).
- `planejamento-deep-learning.md` — planejamento da disciplina.

## Publicar uma nova aula

1. Salve `aulaNN_professor.ipynb` e `aulaNN_alunos.ipynb` em `notebooks/`.
2. No cronograma do `index.html`, troque "Notebook em breve." pelos links da semana:
   `https://colab.research.google.com/github/raoni-teixeira/deep/blob/main/notebooks/aulaNN_alunos.ipynb`
3. `git add notebooks/aulaNN_alunos.ipynb index.html && git commit && git push`.

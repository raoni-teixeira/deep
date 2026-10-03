# Deep Learning — Planejamento da disciplina

**Professor:** Raoni Teixeira (UFMT, Instituto de Engenharia)
**Público:** Engenharia Elétrica
**Duração:** 7 semanas, 1 encontro semanal de 2h30 a 3h
**Período / dias / sala:** _a definir_
**Avaliação:** _a definir_

## Formato

Não há slides. Cada aula é uma nota de aula em forma de notebook Colab: texto corrido com código entremeado, parte dele escrita ao vivo durante o encontro. Os alunos recebem uma versão do notebook com as células "ao vivo" vazias e acompanham digitando junto. Toda aula tem pelo menos um exercício, feito em parte no papel e em parte no notebook.

O fio condutor do curso são os grandes modelos de linguagem (LLMs). Na primeira aula, eles servem para apresentar os tipos de aprendizado e a predição do próximo token. Na última, voltamos a eles para construir um pequeno transformer. A ideia central que atravessa o curso é a de que uma rede profunda aprende, automaticamente, transformações que levam os dados a um espaço latente onde o problema fica mais simples.

## Livro-texto

Simon J. D. Prince. *Understanding Deep Learning*. MIT Press, 2023.

- Página do livro (PDF gratuito e figuras): https://udlbook.github.io/udlbook/
- Repositório com os notebooks oficiais por capítulo: https://github.com/udlbook/udlbook
- Errata e comentários: https://github.com/udlbook/udlbook/issues

## Material de apoio

- Material próprio de introdução ao PyTorch: tensores, grafo computacional, `autograd`, uso de GPU. _(link a definir)_
- Google Colab: https://colab.research.google.com

## Cronograma

### Semana 1 — O que significa uma máquina aprender?
**Leitura:** caps. 1 (Introdução) e 2 (Aprendizado supervisionado)

**Objetivos:** distinguir aprendizado supervisionado, auto-supervisionado, não supervisionado e por reforço, usando o pipeline de um LLM como exemplo (pré-treino, ajuste por instruções, ajuste por preferências); entender a predição do próximo token como um problema de classificação supervisionada; ter uma primeira intuição de espaço latente; escrever modelo, perda, gradiente e mínimo da regressão linear.

**Ao vivo:** modelo de bigramas de caracteres em *Dom Casmurro*, com geração de texto e log-verossimilhança negativa; analogias com embeddings GloVe (rei − homem + mulher) e projeção por PCA; calibração de sensor de temperatura, com superfície de perda e gradiente descendente usando gradiente numérico.

**Exercício:** problemas 2.1 e 2.2 do livro, conferidos no notebook contra o gradiente numérico e o gradiente descendente.

**Para casa:** apostar e justificar, em duas linhas, se a regressão generativa invertida produz a mesma reta que a discriminativa.

**Notebooks:** `notebooks/aula01_professor.ipynb` (fora do git), `notebooks/aula01_alunos.ipynb`

### Semana 2 — Redes neurais rasas
**Leitura:** cap. 3 (Redes neurais rasas)

**Abertura:** resolução do problema 2.3 (regressão generativa × discriminativa) no Colab.

**Objetivos:** entender a rede rasa como soma de funções lineares por partes; relacionar unidades ocultas e regiões lineares; conhecer o teorema da aproximação universal.

**Exercício:** _a definir_

### Semana 3 — Redes neurais profundas
**Leitura:** cap. 4 (Redes neurais profundas)

**Objetivos:** entender a composição de redes como "dobra" do espaço de entrada; comparar profundidade e largura; escrever uma rede profunda em notação matricial e em PyTorch.

**Exercício:** _a definir_

### Semana 4 — Funções de perda
**Leitura:** cap. 5 (Funções de perda)

**Objetivos:** derivar funções de perda pelo princípio da máxima verossimilhança; reconhecer o erro quadrático como caso gaussiano; construir a entropia cruzada para classificação e ligá-la à log-verossimilhança negativa dos bigramas da semana 1.

**Exercício:** _a definir_

### Semana 5 — Ajuste de modelos
**Leitura:** cap. 6 (Ajuste de modelos); cap. 7 (Gradientes e inicialização) _proposta_

**Objetivos:** gradiente descendente, SGD, momento e Adam; retropropagação como percurso no grafo computacional; inicialização. Usa o material próprio de PyTorch (grafo, `autograd`, GPU).

**Exercício:** _a definir_

### Semana 6 — Desempenho e regularização
**Leitura:** caps. 8 (Medindo desempenho) e 9 (Regularização)

**Objetivos:** separar treino, validação e teste; entender viés e variância e o *double descent*; aplicar regularização L2, *early stopping*, *dropout* e aumento de dados.

**Exercício:** _a definir_

### Semana 7 — Transformers _(proposta)_
**Leitura:** cap. 12 (Transformers)

**Objetivos:** fechar o fio condutor do curso; entender atenção e o transformer decodificador; treinar um mini-GPT de caracteres em *Dom Casmurro* e compará-lo com o modelo de bigramas da semana 1.

**Alternativa:** cap. 10 (Redes convolucionais), aproveitando a familiaridade da turma com convolução.

**Exercício:** _a definir_

## Notas para a geração da página

- Usar o layout da página da disciplina de Microcontroladores (`/home/raoni/Documents/micro`).
- Cada semana deve ter os links "Abrir no Colab" para a versão do aluno e, se desejado, a do professor. Formato do link: `https://colab.research.google.com/github/<usuario>/<repositorio>/blob/main/notebooks/<arquivo>.ipynb`
- Notebooks ficam em `notebooks/`. Os da semana 1 já existem: `aula01_professor.ipynb` e `aula01_alunos.ipynb`.
- A versão do professor não é publicada (`.gitignore`), seguindo a convenção de Microcontroladores para gabaritos; a página só linka a versão dos alunos.
- Campos marcados como _a definir_ ou _proposta_ devem aparecer na página de forma discreta ou ser omitidos, até serem confirmados.

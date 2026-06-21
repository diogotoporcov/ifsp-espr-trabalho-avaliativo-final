# Estatística e Probabilidade — Trabalho Avaliativo Final

[![Python](https://img.shields.io/badge/Python-3.11-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)](https://numpy.org/)
[![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?logo=scipy&logoColor=white)](https://scipy.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)

Projeto desenvolvido para o trabalho final de **Estatística e Probabilidade**, com o objetivo de analisar como os participantes distribuem seu tempo entre **obrigações**, **lazer**, **descanso** e **sono**.

A pesquisa foi construída a partir de um formulário com perguntas sobre idade, trabalho, estudo, tarefas domésticas, cuidado de terceiros, deslocamento, lazer, uso de telas, sono e desejo de mais tempo livre.

A análise utiliza Python para aplicar estatística descritiva, probabilidades empíricas, intervalos de confiança, testes de hipótese, regressão linear simples e visualizações gráficas.

---

## Sumário

1. [Visão geral](#visão-geral)
2. [Perguntas analisadas](#perguntas-analisadas)
3. [Dados](#dados)
4. [Metodologia](#metodologia)
5. [Visualizações](#visualizações)
6. [Execução](#execução)

---

## Visão geral

O projeto investiga a relação entre a carga semanal de obrigações e variáveis associadas ao equilíbrio da rotina, como tempo de lazer e descanso, sono por noite, uso de telas no lazer e desejo de mais horas livres.

A principal hipótese analisada é se pessoas com mais horas semanais de obrigações tendem a desejar mais horas adicionais de lazer ou descanso.

---

## Perguntas analisadas

O formulário coleta informações sobre:

* Data e hora da resposta
* Data de nascimento
* Horas semanais de trabalho remunerado
* Horas semanais de estudo
* Horas semanais com tarefas domésticas ou administrativas
* Horas semanais cuidando de outras pessoas sem remuneração
* Horas semanais em deslocamento ou espera
* Horas semanais de lazer e descanso
* Horas semanais de lazer com telas
* Horas de sono por noite
* Horas adicionais desejadas de lazer ou descanso

A partir dessas respostas, o notebook cria variáveis derivadas, como idade, total semanal de obrigações, sono semanal, percentual do lazer feito com telas e proporção entre lazer e obrigações.

---

## Dados

O arquivo de respostas não é incluído diretamente no repositório.

Durante a execução, o notebook usa a variável de ambiente `RESPONSES_SPREADSHEET_URL`, que deve conter o link de download das respostas em formato TSV. Esse arquivo é baixado automaticamente, lido com Pandas e convertido para CSV.

Após o download, os dados são salvos localmente em:

```bash
data/responses.csv
```

Caso esse arquivo já exista, o notebook utiliza a versão local e não realiza um novo download.

---

## Metodologia

A análise realiza as seguintes etapas:

* Carregamento e padronização das colunas
* Conversão de datas e variáveis numéricas
* Inspeção inicial dos dados
* Tratamento de valores impossíveis e inconsistentes
* Criação de variáveis derivadas
* Estatísticas descritivas
* Cálculo de probabilidades empíricas
* Construção de intervalos de confiança
* Aplicação de testes de hipótese
* Ajuste de regressão linear simples

Valores impossíveis pela unidade da pergunta ou inconsistentes entre respostas relacionadas são desconsiderados apenas nas análises afetadas. Valores extremos, mas ainda possíveis, são mantidos na análise principal.

---

## Visualizações

O notebook gera gráficos para apoiar a interpretação dos dados, incluindo:

* Gráficos de barras para médias e probabilidades
* Boxplots para comparar obrigações, lazer e sono
* Histogramas para visualizar distribuições
* Gráficos de dispersão com reta de regressão
* Matriz de correlação entre variáveis quantitativas

Essas visualizações ajudam a observar padrões gerais da amostra e a complementar os resultados dos testes estatísticos.

---

## Execução

Instale as dependências principais:

```bash
pip install pandas numpy scipy matplotlib rich
```

Defina a variável de ambiente com o link TSV das respostas:

```bash
export RESPONSES_SPREADSHEET_URL="URL_DE_DOWNLOAD_TSV"
```

Em seguida, abra o notebook no Jupyter Notebook, Google Colab ou em outra plataforma compatível para visualizar tabelas, gráficos e conclusões.

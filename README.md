# Trabalho de mineração de dados

Este projeto implementa classificação de textos para artigos de notícias usando técnicas de aprendizado de máquina, especificamente Support Vector Machines (SVM). O projeto processa dados de notícias de diferentes categorias e treina modelos para classificar artigos com base em seus títulos e descrições.

## Pré-requisitos

- Python 3.x
- Jupyter Notebook

## Instalação

1. Clone este repositório ou baixe os arquivos
2. Crie e ative um ambiente virtual (recomendado):
```bash
python -m venv venv
source venv/bin/activate  # No Windows use: venv\Scripts\activate
```

3. Instale os pacotes necessários:
```bash
pip install pandas numpy scikit-learn matplotlib nltk tqdm jupyter
## ou
pip install -r requirements.txt
```

## Arquivos Necessários

Certifique-se de ter os seguintes arquivos em seu diretório do projeto:
- `processamento.ipynb`: O notebook Jupyter principal contendo o código de análise
- `datasetNews.json`: O arquivo do dataset contendo as notícias

## Executando o Projeto

1. Abra o VS Code e instale a extensão "Jupyter" se ainda não estiver instalada
   - Procure por "Jupyter"
   - Instale a extensão da Microsoft

2. Abra o projeto no VS Code:
   - Vá em File > Open Folder
   - Selecione a pasta do projeto

3. Abra o arquivo `processamento.ipynb`:
   - O VS Code irá reconhecer automaticamente o arquivo como um Jupyter Notebook
   - Se solicitado, selecione o kernel Python (preferencialmente do ambiente virtual criado anteriormente)

4. Execute o notebook:
   - Você pode executar célula por célula clicando no botão ▶️ ao lado de cada célula
   - Ou use o atalho `Shift+Enter` para executar a célula atual e mover para a próxima
   - Ou, use o menu "Run" no topo do notebook para executar todas as células

O notebook irá:
   - Carregar e pré-processar o dataset de notícias
   - Criar três subconjuntos diferentes dos dados:
     - Três categorias principais (Política, Bem-estar, Entretenimento)
     - Todas as categorias exceto as três principais
     - Nove categorias mais frequentes após remover as três principais
   - Aplicar pré-processamento de texto incluindo:
     - Remoção de stopwords
     - Lematização
     - Vetorização TF-IDF
   - Treinar e avaliar modelos SVM em diferentes combinações de títulos e descrições

## Estrutura do Projeto

A análise está dividida em três partes principais:
1. Pré-processamento e limpeza dos dados
2. Extração de características usando TF-IDF
3. Treinamento do modelo e avaliação usando SVM

## Dependências

- pandas: Manipulação e análise de dados
- scikit-learn: Algoritmos e ferramentas de aprendizado de máquina
- nltk: Ferramentas de Processamento de Linguagem Natural
- matplotlib: Visualização de dados
- tqdm: Barras de progresso para operações de longa duração

## Observações

- A implementação do Naive Bayes foi tentada mas não pôde ser completada devido a restrições de tamanho do dataset
- O projeto usa tanto os títulos quanto as descrições dos artigos para classificação
- Os resultados são avaliados usando métricas de acurácia

Dataset original: [Kaggle](https://www.kaggle.com/datasets/rmisra/news-category-dataset/data)

Referências usadas na codificação: [Grupo Turing USP](https://github.com/turing-usp/fernando-pessoa), [Análise do dataset](https://www.kaggle.com/code/avikumart/nlp-news-articles-classif-wordembeddings-rnn#1.3-Text-data-Preprocessing)

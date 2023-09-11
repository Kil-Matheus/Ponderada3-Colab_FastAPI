# Documentação do Projeto

Este projeto utiliza a biblioteca FastAPI para criar uma API de previsão com base em um modelo de regressão treinado com PyCaret. A API é usada para fazer previsões com base nos recursos fornecidos pelo usuário.

## Pré-requisitos

Antes de executar o projeto, certifique-se de que você tenha as seguintes bibliotecas e ferramentas instaladas:

- Python 3.x
- Pandas
- PyCaret
- FastAPI
- Uvicorn
- Pydantic
- Unidecode

Você pode instalar as bibliotecas usando o `pip`. Por exemplo:


## Estrutura do Projeto

O projeto é dividido em dois componentes principais: o script Python e o Colab Notebook.

### Colab Notebook (`Ponderada _3_Programacao.ipynb`)

- O Colab Notebook contém o código utilizado para pré-processar os dados e treinar o modelo PyCaret.
- Ele também realiza a normalização dos dados e explora a correlação entre as variáveis.
- O modelo treinado é salvo e carregado posteriormente pelo script Python.

link: https://colab.research.google.com/drive/1e1aKMYGFzCI1GfSeQKWBT_rmxtwRe1H4?usp=sharing

### Script Python (`minha_api.py`)

- `minha_api.py` é o arquivo principal que contém a definição da API FastAPI.
- Ele carrega um modelo PyCaret previamente treinado e o utiliza para fazer previsões com base nos dados de entrada fornecidos pelo usuário.
- As colunas do DataFrame de entrada são renomeadas para substituir espaços por underscores e acentos são removidos das colunas.
- O resultado da previsão é retornado como uma resposta da API.


## Executando a API

Para executar a API, siga estas etapas:

1. Abra um terminal e navegue até o diretório onde o arquivo `minha_api.py` está localizado.

2. Execute o seguinte comando para iniciar o servidor FastAPI:

```bash
uvicorn minha_api:app --reload
```
A API estará disponível em `http://localhost:8000/docs`.

## Acessando a Documentação Interativa

1. Abra seu navegador e vá para `http://localhost:8000/docs`.

2. Você verá uma interface interativa que lista todos os endpoints disponíveis, bem como informações sobre os dados esperados para cada um.

3. Para testar a API, clique em um endpoint específico, insira os dados de entrada e clique no botão "Execute" para ver a resposta da API.

A documentação interativa do FastAPI é uma ferramenta valiosa para explorar e testar os endpoints da API de forma interativa.

## Baixar e Rodar do Docker Hub

1. Baixe a imagem do Docker Hub:

```bash
docker pull kilmatheus/ponderada-colab-fastapi:1.0.0
```

2. Execute o seguinte comando para iniciar o servidor FastAPI:

```bash
docker run -p 8000:8000 kilmatheus/ponderada-colab-fastapi:1.0.0
```

A API estará disponível em `http://localhost:8000/docs`.


## Vídeo do Projeto

Link do vídeo: https://drive.google.com/file/d/1Guy2oBOhWIdcqBdO37mpt1nkApRjwYFv/view?usp=sharing

## Autores

- Kil Matheus Gomes Teixeira - Engenharia da Computação - Instituto de Tecnologia e Liderança (INTELI)
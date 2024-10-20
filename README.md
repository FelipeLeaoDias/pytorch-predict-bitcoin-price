# Bitcoin Price Prediction using PyTorch

## Alunos:
- Felipe Leão
- Rafael Santos
- Danilo Scheltes
- Henrique Lyrio

## Objetivo
Este projeto tem como objetivo criar uma IA usando PyTorch para prever o preço do Bitcoin em USD. O dataset foi dividido em duas partes:

- **dataset.csv**: Utilizado para o treinamento e teste inicial, com o salvamento dos pesos da rede neural.
- **datasetteste.csv**: Contém menos dados e é usado para fazer predições e testes usando os pesos salvos.

## Passos do Projeto

### 1. Download dos Datasets
Utilizamos a biblioteca `gdown` para baixar os arquivos do Google Drive.

### 2. Carregar o Dataset e Ajustar Features
Carregamos o dataset usando o `pandas`, e dividimos as colunas entre features e labels.

### 3. Definição do Modelo
Criamos a arquitetura da rede neural com várias camadas densas, ativação `ReLU` e `Dropout` para evitar overfitting.

### 4. Treinamento do Modelo
Utilizamos a função de perda `MSELoss` e o otimizador `Adam`. O treinamento ocorre por 500 épocas com avaliação periódica do erro no conjunto de teste.

### 5. Salvando os Pesos do Modelo
Após o treinamento, salvamos os pesos da rede neural em um arquivo para futuras previsões.

### 6. Avaliação e Plotagem dos Resultados
Utilizamos métricas como `MAE` e `R²` para avaliar o desempenho do modelo e plotamos as predições.

### 7. Avaliar o Modelo com Novos Dados
Carregamos um novo dataset de teste e utilizamos os pesos salvos para realizar predições com novos dados.
# Analise_de_dados_com_Python_e_Pandas
Desafio da Formação Python Developer pela Digital Innovation One, neste Labs será apresentada a biblioteca Pandas, uma biblioteca Python de código aberto para análise de dados, tendo capacidade de trabalhar com dados do tipo planilha, permitindo carregar, manipular e combinar dados rapidamente, entre outras funções.

import pandas as pd

# Criar um DataFrame a partir de um arquivo CSV
data = pd.read_csv('seuarquivo.csv')

# Visualizar as primeiras linhas do DataFrame
print(data.head())

# Verificar informações básicas sobre o DataFrame
print(data.info())

# Calcular estatísticas descritivas
print(data.describe())

# Selecionar colunas específicas
print(data['nome_da_coluna'])

# Filtrar dados com base em condições
filtered_data = data[data['idade'] > 30]

# Ordenar os dados
sorted_data = data.sort_values(by='idade', ascending=False)

# Agregar dados
grouped_data = data.groupby('categoria').mean()

# Exportar dados para um novo arquivo CSV
grouped_data.to_csv('dados_agregados.csv', index=False)

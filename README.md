#### 📈 MANIPULAÇÃO DE DADOS E CRIAÇÃO DE GRÁFICOS COM BIBLIOTECAS PYTHON

Projeto desenvolvido para manipulação de dados de uma base da Bolsa de Valores e criação de gráficos com bibliotecas Pandas e Plotly Express do Python no Google Colab.  
É uma proposta de trabalho feita na <i>Imersão Python: Do Excel à Análise de Dados</i>, promovida pela Alura.    

<img src='https://github.com/rosacarla/Manipulacao-de-dados-e-graficos-com-bibliotecas-python/blob/main/images/aula03.png'>  

---

#### 💬 PROMPTS USADOS NO CHATGPT PARA CRIAR PLANILHAS NO GOOGLE COLAB  

- prompt 1
<img src='https://github.com/rosacarla/Manipulacao-de-dados-e-graficos-com-bibliotecas-python/blob/main/images/aula03-chatgpt.png'>

- código para inclusão da coluna `resultado`
  
```python
# Aplica a lógica da fórmula (da planilha Principal) utilizando uma expressão lambda e a função apply
# Expressao lambda é usada para fazer operações linha a linha
# Função apply é chamada para aplicar outra função
df_principal['resultado'] = df_principal['variacao_rs'].apply(lambda x: 'Subiu' if x > 0 else ('Desceu' if x < 0 else 'Estável'))
df_principal
```

- prompt 2
<img src='https://github.com/rosacarla/Manipulacao-de-dados-e-graficos-com-bibliotecas-python/blob/main/images/aula03-chatgpt2.png'>

- código para inclusão da coluna `cat_idade`
  
```python
# Cria a coluna 'cat_idade' (= planilha Principal) no dataframe 
# Aplica a lógica da fórmula para criar a coluna utilizando expressão lambda e função apply
df_principal['cat_idade'] = df_principal['idade'].apply(lambda x: 'Mais de 100' if x > 100 else ('Menos de 50' if x < 50 else 'Entre 50 e 100'))
df_principal
```

---  

### 💹 ANÁLISE EXPLORATÓRIA DE DADOS 
<img src='https://github.com/rosacarla/Manipulacao-de-dados-e-graficos-com-bibliotecas-python/blob/main/images/aula03-analises.png'>

- prompt 3
<img src='https://github.com/rosacarla/Manipulacao-de-dados-e-graficos-com-bibliotecas-python/blob/main/images/aula03-chatgpt3.png'>

- código para criação de planilha com métricas da coluna `variacao_rs`
  
```python
# Análise de dados com métricas
# Calcula o maior valor
maior = df_principal['variacao_rs'].max()

# Calcula o menor valor
menor = df_principal['variacao_rs'].min()

# Calcula a média
media = df_principal['variacao_rs'].mean()

# Calcula a média de quem subiu
media_subiu = df_principal[df_principal['resultado'] == 'Subiu']['variacao_rs'].mean()

# Calcula a média de quem desceu
media_desceu = df_principal[df_principal['resultado'] == 'Desceu']['variacao_rs'].mean()
(...)
```

---  

### 📊 CRIAÇÃO DE GRÁFICOS COM PLOTLY EXPRESS
<img src='https://github.com/rosacarla/Manipulacao-de-dados-e-graficos-com-bibliotecas-python/blob/main/images/aula03-graficos.png'>

- código para criar gráfico de barras da Variação em R$ por Resultado

```python
# Gera gráfico de barras com biblioteca Plotly Express
fig = px.bar(df_analise_saldo, x='resultado', y='variacao_rs', text='variacao_rs', title='Variação em Reais por Resultado')
# Exibe o gráfico na tela
fig.show()  
```

---  

### 🧠 DESAFIOS DA AULA 3  

- Pesquise com a documentação da biblioteca Plotly ou GPT como mudar a formatação dos números do gráfico de barras;
- Fazer o gráfico de pizza no df_análise_segmentos com a mesma biblioteca Potly;
- Fazer o `groupby` da categoria de idades e gerar o gráfico de barras.

☑️ RESOLUÇÃO DOS DESAFIOS  
- prompt 4
<img src='https://github.com/rosacarla/Manipulacao-de-dados-e-graficos-com-bibliotecas-python/blob/main/images/aula03-chatgpt4.png'>

- código para formatação dos números nas barras do gráfico das categorias por idade
  
```python
# Gera gráfico de barras com formatação dos números (separador de milhar no texto das barras)
fig = px.bar(df_analise_saldo, x='resultado', y='variacao_rs', text=df_analise_saldo['variacao_rs'].apply(lambda x: '{:,.2f}'.format(x)), title='<b>VARIAÇÃO EM REAIS POR RESULTADO</b>')

# Exibe o gráfico na tela
fig.show()
```

- prompt 5
<img src='https://github.com/rosacarla/Manipulacao-de-dados-e-graficos-com-bibliotecas-python/blob/main/images/aula03-chatgpt5.png'>

- código para criar gráfico em formato de pizza com Variação em R$ por Segmento de quem subiu

```python
# Cria o gráfico de pizza do df_analise_segmento
# Filtra os dados para remover os segmentos 'Petróleo', 'Mineração' e 'Banco'
df_analise_segmento_filtrado = df_analise_segmento[~df_analise_segmento['segmento'].isin(['Petróleo', 'Mineração', 'Banco'])]

# Ajusta o tamanho da pizza
fig = px.pie(df_analise_segmento_filtrado, values='variacao_rs', names='segmento', title='<b>VARIAÇÃO EM R$ POR SEGMENTO COM ALTA NO RESULTADO</b>', width=1024, height=1024)

# Exibe o gráfico
fig.show()
```

- prompt 6
<img src='https://github.com/rosacarla/Manipulacao-de-dados-e-graficos-com-bibliotecas-python/blob/main/images/aula03-chatgpt6.png'>

- código para criar gráfico de barras da Variação em R$ a partir do agrupamento das categorias de idade das empresas

```python
# Cria gráfico de barras com dados de df_analise_cat_idade usando Plotly Express
fig = px.bar(df_analise_cat_idade, x='cat_idade', y='variacao_rs', text='variacao_rs', title='<b>VARIAÇÃO EM R$ versus IDADE</b>')

# Formata números em textos das barras para terem separadores de milhar e 3 casas decimais após a vírgula
fig.update_traces(texttemplate='%{text:,.2f}')

# Atualiza os nomes dos eixos
fig.update_xaxes(title_text='Idade')
fig.update_yaxes(title_text='Variação em R$')

# Exibe o gráfico
fig.show()
```

---  

#### ✍️ AUTORA  
Carla Edila Silveira  
Contato: rosa.carla@pucpr.edu.br  

---

#### ©️ LICENÇA

[MIT](https://choosealicense.com/licenses/mit/)  

---  

#### 🔗 LINKS ÚTEIS  

[Conheça as bibliotecas do Python de Data Visualization](https://www.alura.com.br/artigos/data-visualization-conhecendo-bibliotecas-python?_gl=1*m01qr6*_ga*MTkyMTEwNTQ2Ni4xNzA5NTk0NTU0*_ga_1EPWSW3PCS*MTcxMTU3MDQ0Ny4yOS4xLjE3MTE1NzA1MTUuMC4wLjA.*_fplc*b1ZHNnVRMXRZRkJhY0NFRTQlMkZiT0U3Y3o2bkVHOWcwOXphbHJjdktaY1dSOVgzM3FOc2xFam16SCUyRjlMRVpwNyUyQjhOclRIZTBUMiUyQkNONzhnWlU0VjlwTHI2WE5HUTloJTJGMXRwTDI5WU44NWN3UnpGcDZRSmRsME54WWtibEtHQSUzRCUzRA..)  
[O que é DataFrame](https://www.alura.com.br/artigos/pandas-o-que-e-para-que-serve-como-instalar?_gl=1*10lewlx*_ga*MTkyMTEwNTQ2Ni4xNzA5NTk0NTU0*_ga_1EPWSW3PCS*MTcxMTU3MDQ0Ny4yOS4xLjE3MTE1NzExMzAuMC4wLjA.*_fplc*b1ZHNnVRMXRZRkJhY0NFRTQlMkZiT0U3Y3o2bkVHOWcwOXphbHJjdktaY1dSOVgzM3FOc2xFam16SCUyRjlMRVpwNyUyQjhOclRIZTBUMiUyQkNONzhnWlU0VjlwTHI2WE5HUTloJTJGMXRwTDI5WU44NWN3UnpGcDZRSmRsME54WWtibEtHQSUzRCUzRA..#:~:text=DataFrame,Series%20sob%20um%20mesmo%20index.)  
[ChatGPT e a análise de dados avançada](https://www.youtube.com/watch?v=u-JoDQ58Dv0)  
[Documentação do Pandas GroupBy](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.groupby.html)  
[Documentação da biblioteca Plotly](https://plotly.com/python/bar-charts/)  

---

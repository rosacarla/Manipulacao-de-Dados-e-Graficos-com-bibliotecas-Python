#### 📈 MANIPULAÇÃO DE DADOS E CRIAÇÃO DE GRÁFICOS COM BIBLIOTECAS PYTHON

Projeto desenvolvido para manipulação de dados de uma base da Bolsa de Valores e criação de gráficos com bibliotecas Python no Google Colab.  
É uma proposta de trabalho feita na <i>Imersão Python: Do Excel à Análise de Dados</i>, promovida pela Alura.    

<img src=''>  

---

#### 📄 FÓRMULAS DO GOOGLE SHEETS PARA ANÁLISE DE DADOS E GRÁFICOS  

<img src=''>  

1) Criação de tabela com Métricas da coluna Variação R$
- maior variação: `=MAIOR(Principal!O:O;1)`
- menor variação: `=MENOR(Principal!O:O; 1)`
- média da variação: `=MÉDIA(Principal!O:O)`
- média de quem subiu: `=MÉDIASE(Principal!P:P;"Subiu";Principal!O:O)`
- média de quem desceu: `=MÉDIASE(Principal!P:P;"Desceu";Principal!O:O)`
- nome da empresa de maior variação: `=PROCV(B2;Principal!O:R;3;0)`
- nome da empresa de menor variação: `=PROCV(B3;Principal!O:R;3;0)`

2) Criação de tabela com colunas "SEGMENTO, VARIAÇÃO R$, VARIAÇÃO DE QUEM SUBIU"
- coluna SEGMENTO: `=UNIQUE(Principal!R2:R82)`
- coluna  VARIAÇÃO R$: `=SOMASE(Principal!R:R;A13;Principal!O:O)`
- coluna VARIAÇÃO DE QUEM SUBIU: `=SOMASES(Principal!O:O;Principal!R:R;A13;Principal!P:P;"Subiu")`

3) Criação de tabela com colunas "RESULTADO, VARIAÇÃO R$"
- coluna RESULTADO: `=UNIQUE(Principal!P2:P82)`
- coluna VARIAÇÃO R$: `=SOMASE(Principal!P:P;A61;Principal!O:O)`

4) Criação de tabela com colunas "ANÁLISE POR IDADE, VARIAÇÃO R$, QUANTIDADE DE EMPRESAS"
- coluna ANÁLISE POR IDADE: `=UNIQUE(Principal!T2:T82)`
- coluna VARIAÇÃO R$: `=SOMASE(Principal!T:T;A71;Principal!O:O)`
- coluna QUANTIDADE DE EMPRESAS: `=CONT.SE(Principal!T:T;A71)`

☑️ Ver [resolução no Google Sheets]().

---  

#### 🧠 DESAFIO DA AULA 3

- Pesquise com a documentação da biblioteca Plotly ou GPT como mudar a formatação dos números do gráfico de barras;
- Fazer o gráfico de pizza no df_análise_segmentos com a mesma biblioteca Potly;
- Fazer o GroupBy da categoria de idades e gerar o gráfico de barras.

<img src=''>  

---  

#### 💻 ANÁLISE DE DADOS COM BIBLIOTECA PANDAS DO PYTHON  
<img src=''>   

☑️ Ver [NOTEBOOK no Google Colab]().  

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

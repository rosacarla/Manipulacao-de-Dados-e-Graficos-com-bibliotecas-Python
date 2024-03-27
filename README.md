#### 📈 GRÁFICOS E ANÁLISES COM GOOGLE COLAB E PYTHON PANDAS

Projeto desenvolvido para criação gráficos e tabelas no Google Sheets, manipulação de dados com Python Pandas pelo Google Colab.  
É uma proposta de trabalho feita na <i>Imersão Python: Do Excel à Análise de Dados</i>, promovida pela Alura.    

<img src='https://github.com/rosacarla/graficos-e-analises-com-Google-Colab-e-Python-Pandas/blob/main/images/aula02.png'>  

---

#### 📄 FÓRMULAS DO GOOGLE SHEETS PARA ANÁLISE DE DADOS E GRÁFICOS  

<img src='https://github.com/rosacarla/graficos-e-analises-com-Google-Colab-e-Python-Pandas/blob/main/images/aula02-graficos.png'>  

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

☑️ Ver [resolução no Google Sheets](https://docs.google.com/spreadsheets/d/1ybYb4sdnHts2VyavBV9TroK_gfeClFuMbYQWbCi4rGg/edit?usp=sharing).

---  

#### 🧠 DESAFIO DA AULA 2

- Crie um gráfico de barras olhando a faixa etária e o valor da variação;
- Faça outro gráfico de barras com a faixa etária e a quantidade de empresas que estão em cada faixa etária;
- Explore os tipos de gráficos com os dados já feitos.

<img src='https://github.com/rosacarla/graficos-e-analises-com-Google-Colab-e-Python-Pandas/blob/main/images/aula02-graficos-desafio.png'>  

---  

#### 💻 ANÁLISE DE DADOS COM BIBLIOTECA PANDAS DO PYTHON  
<img src='https://github.com/rosacarla/graficos-e-analises-com-Google-Colab-e-Python-Pandas/blob/main/images/aula02-python.png'>   

☑️ Ver [NOTEBOOK no Google Colab](https://github.com/rosacarla/graficos-e-analises-com-Google-Colab-e-Python-Pandas/blob/main/Imersao_Python_Aula02.ipynb).  

---  

#### ✍️ AUTORA  
Carla Edila Silveira  
Contato: rosa.carla@pucpr.edu.br  

---

#### ©️ LICENÇA

[MIT](https://choosealicense.com/licenses/mit/)  

---  

#### 🔗 LINKS ÚTEIS  

[O que é Google Colab?](https://www.alura.com.br/artigos/google-colab-o-que-e-e-como-usar?_gl=1*1obtdxk*_ga*MTkyMTEwNTQ2Ni4xNzA5NTk0NTU0*_ga_1EPWSW3PCS*MTcxMTQ3Nzc3OS4yNi4xLjE3MTE0Nzk0NDQuMC4wLjA.*_fplc*TmtySU9mMkZvOXRhNkJFTnpuTHRsSDFMdU5lM0YzcyUyRlNjaDFOQ3pqOWU3Tk1QZFJvZWJXMyUyQkRTYnElMkZEJTJCMlA5bjZ4ZTFvUnZQSzhzcEt0ZCUyQjhaUlM4NjZyRkloNGxFUHN5VXB6dWtFOHhJeGRJTXVBTTdBelo0dUk4M0FuQSUzRCUzRA..)  
[Pandas Python: o que é, para que serve e como instalar](https://www.alura.com.br/artigos/pandas-o-que-e-para-que-serve-como-instalar?_gl=1*j4i1dh*_ga*MTkyMTEwNTQ2Ni4xNzA5NTk0NTU0*_ga_1EPWSW3PCS*MTcxMTQ3Nzc3OS4yNi4xLjE3MTE0Nzk4MjguMC4wLjA.*_fplc*TmtySU9mMkZvOXRhNkJFTnpuTHRsSDFMdU5lM0YzcyUyRlNjaDFOQ3pqOWU3Tk1QZFJvZWJXMyUyQkRTYnElMkZEJTJCMlA5bjZ4ZTFvUnZQSzhzcEt0ZCUyQjhaUlM4NjZyRkloNGxFUHN5VXB6dWtFOHhJeGRJTXVBTTdBelo0dUk4M0FuQSUzRCUzRA..)  
[Ecossistema Python | Hipsters Ponto Tech](https://www.alura.com.br/podcast/hipsterstech-ecossistema-python-hipsters-ponto-tech-387-a9175?_gl=1*1r8pa05*_ga*MTkyMTEwNTQ2Ni4xNzA5NTk0NTU0*_ga_1EPWSW3PCS*MTcxMTQ3Nzc3OS4yNi4xLjE3MTE0Nzk5MjMuMC4wLjA.*_fplc*TmtySU9mMkZvOXRhNkJFTnpuTHRsSDFMdU5lM0YzcyUyRlNjaDFOQ3pqOWU3Tk1QZFJvZWJXMyUyQkRTYnElMkZEJTJCMlA5bjZ4ZTFvUnZQSzhzcEt0ZCUyQjhaUlM4NjZyRkloNGxFUHN5VXB6dWtFOHhJeGRJTXVBTTdBelo0dUk4M0FuQSUzRCUzRA..)  
[IA dentro de empresas | Hipsters Ponto Tech](https://www.alura.com.br/podcast/hipsterstech-openai-sora-google-gemini-pro-1-5-ia-no-picpay-hipsters-fora-de-controle-45-a9238?_gl=1*5rrlev*_ga*MTkyMTEwNTQ2Ni4xNzA5NTk0NTU0*_ga_1EPWSW3PCS*MTcxMTQ3Nzc3OS4yNi4xLjE3MTE0Nzk5NzcuMC4wLjA.*_fplc*TmtySU9mMkZvOXRhNkJFTnpuTHRsSDFMdU5lM0YzcyUyRlNjaDFOQ3pqOWU3Tk1QZFJvZWJXMyUyQkRTYnElMkZEJTJCMlA5bjZ4ZTFvUnZQSzhzcEt0ZCUyQjhaUlM4NjZyRkloNGxFUHN5VXB6dWtFOHhJeGRJTXVBTTdBelo0dUk4M0FuQSUzRCUzRA..)  

---

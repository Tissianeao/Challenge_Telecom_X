# Challenge_Telecom_X
Este projeto realiza uma análise exploratória de dados para identificar os fatores que contribuem para a evasão de clientes (churn) em uma empresa de telecomunicações, a Telecom X. O objetivo é fornecer insights para desenvolver estratégias de retenção mais eficazes.

Etapas do Projeto:

1. Carregamento e Desestruturação dos Dados:
* Os dados foram carregados de um arquivo JSON para um DataFrame Pandas.
* Colunas aninhadas como 'customer', 'phone', 'internet' e 'account' foram desmembradas em novas colunas de nível superior para facilitar o acesso e a análise dos dados.

2. Tratamento da Coluna 'Charges':
* A coluna 'Charges' foi dividida para extrair 'MonthlyCharges' (cobranças mensais) e 'TotalCharges' (cobranças totais).
* A coluna 'TotalCharges' foi convertida para tipo numérico, com valores não numéricos tratados como NaN.

3.Codificação de Variáveis Categóricas:
* Colunas binárias (como 'Churn', 'Partner', 'PhoneService', etc.) foram convertidas para 0 e 1 ('Yes' para 1, 'No' ou 'No service' para 0).
* A coluna 'gender' foi mapeada para 0 (Feminino) e 1 (Masculino).

4. Foi criada a coluna 'Contas_Diarias', calculada dividindo 'MonthlyCharges' por 30, para ter uma medida diária de cobrança.

5. Foi realizada uma verificação de valores ausentes (NaN) e linhas duplicadas para garantir a integridade do dataset. (Identificados 11 valores ausentes em 'TotalCharges').

6. Estatísticas Descritivas:
* Foram calculadas e exibidas estatísticas descritivas (média, mediana, desvio padrão, etc.) para as colunas numéricas (e.g., 'tenure', 'MonthlyCharges', 'TotalCharges', 'Contas_Diarias').
* As distribuições de frequência e proporções foram analisadas para as colunas categóricas.

7. Foram gerados histogramas com kde (Kernel Density Estimate) para 'tenure', 'MonthlyCharges', 'TotalCharges' e 'Contas_Diarias' para visualizar suas distribuições.

8.  Foram criados count plots para 'Churn', 'InternetService', 'Contract' e 'PaymentMethod' para mostrar a contagem e proporção de cada categoria.

9.  Foram gerados count plots comparando a distribuição de 'Churn' com diversas variáveis categóricas ('gender', 'Partner', 'Dependents', 'InternetService', 'Contract', 'PaymentMethod', 'SeniorCitizen', 'PaperlessBilling'). Isso permitiu identificar quais categorias têm maior ou menor taxa de churn.

10.  Foram criados box plots para comparar a distribuição de 'tenure', 'MonthlyCharges', 'TotalCharges' e 'Contas_Diarias' entre clientes que evadiram (Churn=1) e não evadiram (Churn=0). Isso ajudou a visualizar diferenças nas medianas e dispersões.

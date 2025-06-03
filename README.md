"# Telecom-X" 

eiros passos no projeto Telecom X

Extração:
A extração é a primeira etapa do processo ETL (Extract, Transform, Load). Ela consiste em obter os dados a partir da sua fonte de origem. No nosso caso, importamos os dados do GitHub usando o seguinte endereço:
https://raw.githubusercontent.com/alura-cursos/challenge2-data-science/refs/heads/main/TelecomX_Data.json

Para entender melhor os dados, utilizei funções como head(), info() e describe(). Essas funções ajudaram a identificar possíveis erros ou valores ausentes, entender a distribuição das variáveis e detectar relações interessantes entre as colunas.

Transformação:
Na etapa de transformação, utilizei funções para tratar o arquivo JSON, como:

df.isnull().sum() para verificar valores nulos em cada coluna.
df.duplicated().sum() para identificar registros duplicados.
Como havia poucos valores em branco, decidi deixar esses registros inicialmente sem alteração. Caso seja necessário, posso preencher esses valores usando a função df.replace().

Carga e Análise (Load):
Na fase de carga, gerei diversos gráficos para analisar os dados. Notei que as informações relacionadas à evasão (Churn) são um pouco inconclusivas. Isso porque a variável indica apenas se o cliente ainda mantém sua assinatura ou serviço em uso, o que limita a análise sobre a saída real dos clientes.

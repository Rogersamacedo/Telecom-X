"# Telecom-X" 

eiros passos no projeto Telecom X

Extra��o:
A extra��o � a primeira etapa do processo ETL (Extract, Transform, Load). Ela consiste em obter os dados a partir da sua fonte de origem. No nosso caso, importamos os dados do GitHub usando o seguinte endere�o:
https://raw.githubusercontent.com/alura-cursos/challenge2-data-science/refs/heads/main/TelecomX_Data.json

Para entender melhor os dados, utilizei fun��es como head(), info() e describe(). Essas fun��es ajudaram a identificar poss�veis erros ou valores ausentes, entender a distribui��o das vari�veis e detectar rela��es interessantes entre as colunas.

Transforma��o:
Na etapa de transforma��o, utilizei fun��es para tratar o arquivo JSON, como:

df.isnull().sum() para verificar valores nulos em cada coluna.
df.duplicated().sum() para identificar registros duplicados.
Como havia poucos valores em branco, decidi deixar esses registros inicialmente sem altera��o. Caso seja necess�rio, posso preencher esses valores usando a fun��o df.replace().

Carga e An�lise (Load):
Na fase de carga, gerei diversos gr�ficos para analisar os dados. Notei que as informa��es relacionadas � evas�o (Churn) s�o um pouco inconclusivas. Isso porque a vari�vel indica apenas se o cliente ainda mant�m sua assinatura ou servi�o em uso, o que limita a an�lise sobre a sa�da real dos clientes.

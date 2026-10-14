```markdown

# Uber data analysis


Esse trabalho tem como objetivo colocar em prática os conhecimentos obtidos na disciplina de ciencias dos dados e inteligencia empresarial. para o desenvolvimento desse trabalho, estou usando um dataset disponivel no kaggle, intitulado "Uber Data Analytics Dashboard", disponível em: https://www.kaggle.com/datasets/yashdevladdha/uber-ride-analytics-dashboard. a motivação desse trabalho surgiu com o objetivo de identificar padrões de demanda, cancelamentos e características das viagens. A análise dessas informações pode apoiar a identificação de dificuldades operacionais e de oportunidades para melhorar a experiência dos usuários. Nesse contexto, este projeto, utiliza uma base pública sobre solicitações de corridas para aplicar técnicas de análise estatística e explorar como os resultados podem contribuir para decisões de negócio.

## Descrição do dataset
O projeto utiliza o dataset [Uber Data Analytics Dashboard](https://www.kaggle.com/datasets/yashdevladdha/uber-ride-analytics-dashboard), disponibilizado por Yash Dev Laddha no Kaggle. O arquivo analisado contém **150.000 registros e 21 colunas**, com datas entre **1º de janeiro e 30 de dezembro de 2024**.

Cada linha representa uma solicitação de corrida, com informações sobre data, horário, identificadores da reserva e do cliente, tipo de veículo, locais de origem e destino, status, indicadores de tempo, valor, distância, avaliações e método de pagamento. A base também apresenta motivos de cancelamento e de viagens incompletas.

A origem operacional dos registros e sua eventual geração sintética não foram confirmadas. Por isso, o conjunto será utilizado como estudo acadêmico, sem atribuir os resultados ao desempenho real da Uber ou generalizá-los para o mercado de transporte por aplicativo.

## Perguntas de negócio

1. Como as solicitações se distribuem entre meses, dias da semana e horários?
2. A proporção de cancelamentos varia entre os tipos de veículo?
3. Quais locais de embarque apresentam maior proporção de solicitações sem motorista disponível?
4. Qual é a relação entre distância e valor nas corridas concluídas?
5. O valor médio das corridas concluídas difere entre dias úteis e fins de semana?

## Análises planejadas

### Preparação e qualidade dos dados
Serão verificados os tipos das variáveis, a consistência das datas e horários, a repetição de identificadores, os valores ausentes e os valores extremos. Os campos de tempo terão suas definições e unidades conferidas antes da interpretação. Também serão criadas variáveis de calendário, como mês, dia da semana, hora e classificação entre dia útil e fim de semana.

Os dados ausentes serão avaliados conforme o status da solicitação. A ausência de avaliação em uma corrida cancelada, por exemplo, não será automaticamente tratada como um erro ou substituída por uma média. Valores extremos serão investigados antes de qualquer exclusão.

### Análise descritiva
Serão calculadas frequências e proporções das variáveis categóricas e medidas de tendência central, dispersão e distribuição das variáveis quantitativas. Serão utilizados gráficos de barras, histogramas, boxplots, gráficos de dispersão e mapas de calor para apresentar:

- A distribuição das solicitações por mês, dia da semana e horário.
- A participação dos tipos de veículo e dos diferentes status.
- As proporções de cancelamento pelo cliente e pelo motorista.
- A proporção de solicitações sem motorista por local de embarque, acompanhada do volume de solicitações.
- Os motivos registrados para cancelamentos e viagens incompletas.
- A distribuição de valores, distâncias, tempos e avaliações nos registros em que essas informações se aplicam.
- As correlações entre medidas quantitativas, com atenção a valores extremos e relações matemáticas entre variáveis derivadas.
Cancelamentos, viagens incompletas e solicitações sem motorista serão apresentados separadamente. As análises de valores, distâncias e avaliações terão como recorte principal as corridas concluídas.

### Análise inferencial
Serão realizados os seguintes procedimentos, após a verificação dos pressupostos:

- **Intervalo de confiança de 95% para a proporção de cancelamentos:** considerando como cancelamentos os registros classificados como cancelados pelo cliente ou pelo motorista, em relação ao total de solicitações.
- **Teste qui-quadrado de independência:** para avaliar a associação entre tipo de veículo e ocorrência de cancelamento.
- **Teste t de Welch:** para comparar o valor médio das corridas concluídas entre dias úteis e fins de semana, caso seja adequado às características dos dados.
Os testes adotarão nível de significância de 5%, com apresentação das hipóteses, estatísticas e p-valores. A interpretação também considerará a magnitude das diferenças e associações, evitando confundir significância estatística com relevância prática. A aplicação dos procedimentos levará em conta possíveis dependências entre registros e a ausência de informações sobre o processo de amostragem.

### Interpretação e comunicação dos resultados
Os achados serão organizados em um relatório executivo que conectará as análises às perguntas de negócio. As recomendações serão apresentadas como oportunidades de investigação ou ações a serem testadas, sem atribuir causalidade às associações observadas. O relatório também documentará as decisões de tratamento e as limitações da base, permitindo a compreensão e a reprodução da análise.
```

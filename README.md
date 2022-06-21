#Teste Engenheiro de dados ROX

## 1. Objetivo 

O processo de ingestão de dados utilizando ferramentas para o  armazenamento e automatização dos processos de Extração, Transformação e Carga dos dados. Também, efetuar análises através da visualização dos dados processados.

## 2. Tecnologías utilizadas

### 2.1. Azure
Uma das plataformas mais utilizadas quando falamos em execução de aplicativos e serviços, baseados em computação em nuvem. Utilizei por entender que esta ferramenta tem funcionalidades incríveis para execução de processos de ETL e armazenamento dos dados. A seguir as ferramentas da Azure utilizadas.

#### 2.1.1. Data Lake
Para armazenar os dados, aplicamos o conceito de camadas de um data lake, para facilitar a organização e direcionamento rápido para extrações e análises.

#### 2.1.2. Data Factory
Para executar o processo e ETL utilizamos a ferramenta Data Factory. Orquestramos todo os pipelines de dados de forma automatizada com os gatilhos programados.

#### 2.1.3. Banco de Dados SQL
Para armazenar os dados após o processo de transformação. Mantemos na mesma plataforma na Nuvem

#### 2.1.4. Azure Data Studio


### 2.2. Power BI



## 3. Arquitetura

Pensando no cenário onde a empresa de Produção de Bicicletas, diariamente, salve  arquivos brutos oriundos do sistema de vendas, sobre os pedidos executados no dia anterior em. Para ingestão desses dados e tratamento para análise passamos pelas seguintes etapas:

### 3.1. Armazenamento no Data Lake

O Data Lake está subdividido em duas camas Raw e Trusted. A camada Raw é utilizada para armazenar os dados brutos. Por sua vez, a camada Trusted é utilizada para armazenar os dados que passaram pelo processo de transformação e que estão aptos para serem consumidos pelos analistas e cientistas de dados.

### 3.2. Orquestração 

Os dados brutos são direcionados para transformação através de consultas com Power Query, onde limpamos os dados, excluímos colunas que não utilizaremos para análise e carregamos para outro arquivo csv na camada Trusted. Agora os dados estão disponíveis para análise, mas incluímos mais uma etapa nesse pipeline que é carregar os dados para um banco de dados SQL, ambiente ideal para os analistas efetuarem suas consultas ou até conectarem-se com ferramentas de visualização de dados. 

## Conclusão
Apresentamos neste repositório, todas as etapas da ingestão de dados principalmente com ferramentas Azure. Temos também o arquivo com a visualização no Power BI, as consultas e a modelagem conceitual.

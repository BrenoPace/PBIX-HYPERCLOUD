# Teste Técnico Business Intelligence Hypercloud

## Perguntas Teóricas: ##

### 1.	Para você, o que significa Business Intelligence? ###
O conceito de BI ou inteligência de negócios, consiste em gerar informações (insights) através de dados coletados pelos setores de uma determinada empresa. Utilizando processos e ferramentas de ETL para subsidiar a tomada de decisão com objetivo de otimizar os resultados.

### 2.	Cite duas ferramentas de ETL: ###

#### Ferramenta de armazenamento de dados: ####
* Google BigQuery – Serviço de armazenamento de dados em várias nuvens, sem a necessidade de um servidor, ágil e estável.

#### Ferramenta de tratamento de dados: ####
* MySQL – Dedicada para padronizar, carregar, tratar e extrair grandes bases de dados, sendo de baixa complexidade e alta aplicação.

### 3.	Cite três ferramentas de apresentação de dados: ###
Power BI, Tableau e Qlik Sense. Sendo o Power BI a ferramenta mais utilizada, com uma arquitetura flexível, integração com soluções da Microsoft e confiabilidade se destaca no mercado.

### 4.	O que é uma tabela Fato e o que é uma tabela Dimensão? ###
O significado de tabelas Fato e Dimensão, são parte de um conceito de ETL, conhecida pela metodologia de ***Kimball***. Esse modelo se baseia na integração entre tabelas no formato ***Star Squema***, onde particiona os dados numéricos transacionais em tabelas fatos, relacionando com informações de referência nas tabelas Dimensão. Exemplo de tabela Fato poderia ser dados de vendas diários, enquanto tabelas Dimensão poderiam ser informações dos produtos vendidos, dos clientes compradores, dos vendedores, dos pontos de vendas.

### 5.	Quais tipos de modelagens são as mais utilizadas em um projeto de BI? ###
Projetos que envolvem bancos de dados multirelacionais (Fatos e Dimensão), utilizam com maior frequência modelagens ***Star Squema*** e ***Snowflake***. Sendo o ***Star Squema*** relacionamento de tabelas dimensões com uma ou mais tabelas Fato, enquanto o ***Snowflake*** pode relacionar tabelas Fato as dimensões e dimensões com outras dimensões auxiliares.

### 6.	O que significa ***Surrogate Key***? ###
***Surrogate Key*** é uma chave, geralmente numérica e composta, criada para identificar registros únicos de uma tabela. Criando assim uma identificação única que não afeta diretamente uma tabela.

### 7.	Explique a diferença entre relacionamento 1 para 1 e 1 para N: ###
Os relacionamentos criados entre tabelas Fato e tabelas Dimensão podem ser denominados como 1 para 1, onde encontramos apenas 1 ocorrência em ambas tabelas, ou, 1 para N (1 para muitos), quando encontramos 1 ocorrência em uma das tabelas e muitas ocorrências em outra tabela.

### 8.	O que significa Drill Down/Drill up? ###
***Drill Down*** e ***Drill Up*** são conceitos de hierarquias de informações. No ***Drill Down*** é possível passar de um nível mais alto, para um nível mais baixo de agregação. Exemplo seria identificar dados agregados em anos e direciona-los para meses. No ***Drill Up*** se faz na direção contrária, onde podemos ter as informações correspondentes a municípios e direciona-los para estados. Gerasse assim um escalonamento de informações.

---

## Teste Técnico ##

### 1. Faça um desenho da modelagem deste DataWarehouse relacionando as tabelas:

![Modelo DW relaciomentos](https://user-images.githubusercontent.com/116115002/196692130-476a1fba-f203-43f8-a2d1-7c49572ba304.png)

### 1.1 Qual a modelagem projetada? ###
O esquema acima representa uma modelagem ***Snowflake***, em virtude das ramificações das tabelas dimensões com dimensões auxiliares.

# Desafio de Projeto - Modelagem e Transformação de dados com DAX com Power BI - DIO


## Descrição e Objeto do projeto
Utilizar a tabela única Financial Sample para criar as tabelas dimensão e fato baseado no modelo star schema.

O processo consiste na criação das tabelas com base na tabela original. A partir da cópia serão selecionadas as colunas que irão compor a visão da nova tabela. Sendo assim, a partir da tabela principal serão criadas as tabelas:

**F_Vendas** (SK_ID , ID_Produto, Produto, Units Sold, Sales Price, Discount Band, Segment, Country, Salers, Profit, Date (campos))

**D_Produtos** (ID_produto, Produto, Média de Unidades Vendidas, Médias do valor de vendas, Mediana do valor de vendas, Valor máximo de Venda, Valor mínimo de Venda)

**D_Produtos_Detalhes** (ID_produtos, Discount Band, Sale Price, Units Sold, Manufactoring Price)

**D_Descontos** (ID_produto, Discount, Discount Band)

**D_Detalhes** (ID_Produto, Gross Sales, COGS)

**D_Calendário** (Date, ID_Produto, Month Name, Quarter, Week Day, Year)

**D_Categoria** (ID_Produto, Segment, Country)

## Processo de Criação das tabelas

O processo envolveu criar uma cópia da tabela financials_origem para cada tabela (fato e dimensão).

Foram renomeadas as tabelas, excluídas as colunas desnecessárias e as colunas restantesforam reoganizadas para melhor visualização.

A coluna ID_produto foi criada utilizando a opção de coluna condicional e criando uma regra para cada produto da coluna produtos, gerando assim o índice de produtos.

Na Tabela D_Produtos, as colunas Média de Unidades Vendidas, Médias do valor de vendas, Mediana do valor de vendas, Valor máximo de Venda, Valor mínimo de Venda, foram criadas utilizando a opção avançada de Agrupar por no menu trasformar.

Na tabela D_Calendário, as colunas Month Name, Quarter, Week Day, Year, foram criadas utilizando fórmulas DAX: 
- Month Name = FORMAT(MONTH([date]), "mmm") 
- Quarter = QUARTER([date])
- Week Day = WEEKDAY([date])
- YEAR = YEAR([Date])

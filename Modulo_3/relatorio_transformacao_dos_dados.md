# Desafio de Projeto - Processando e Transformando Dados com Power BI - DIO

Este relatório descreve as etapas para a transformação de dados com o objetivo de criar uma base de dados limpa e estruturada, preparando-os para análise e relatórios futuros.

## Etapa 1: Verificação dos Cabeçalhos e Tipos de Dados

Verificar a consistência dos cabeçalhos e dos tipos de dados nas tabelas fornecidas.

### Processo
Verificados os cabeçalhos das tabelas garantindo que os nomes das colunas estão corretos e descritivos.
Verificados os tipos de dados em cada coluna para garantir que correspondam ao esperado.

## Etapa 2: Modificação dos Valores Monetários para o Tipo Double Preciso

Garantir que os valores monetários sejam armazenados de forma adequada.

### Processo
Identificadas as colunas que armazenam valores monetários.
Valores monetários convertidos. 

## Etapa 3 e 4: Verificação de Valores Nulos E colaboradores sem Gerente

Detectar e analisar a presença de valores nulos para possível remoção.
Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente

### Processo
Confirmada a existência de valores nulos. 
Os valores foram preenchidos e ou mantidos de acordo com as informações recebidas.
O empregado com nulo em ID gerente é gerente Geral. 
Não foi encontrado empregado sem gerente.

## Etapa 5 e 6 : Verificação de Departamentos Sem Gerente

Identificar se há departamentos sem gerente designado.

### Processo
Todos os Departamentos possuem Gerentes.

## Etapa 7: Verificação do Número de Horas dos Projetos

Garantir que as informações de horas dos projetos estejam corretas.

### Processo
Não foram encontrados erros na Coluna de horas dos projetos.

## Etapa 8: Separação de Colunas Complexas

Separar colunas complexas em colunas mais simples.

### Processo
Foi separada a Coluna que contém o endereço completo.

## Etapa 9 e 10: Mesclagem de Tabelas Empregados e Departmentos e Eliminação de Colunas Desnecessárias

Criar uma tabela de empregados com o nome dos departamentos associados.
Remover colunas que não são necessárias.

### Processo
Realizada a mescla entre a tabela Empregados e departmentos com base na coluna Id Departamento que relaciona as duas tabelas.
Excluídas as colunas que não são relevantes para a análise.

## Etapa 11: Junção de Colaboradores e Nomes dos Gerentes

Realize a junção dos colaboradores e respectivos nomes dos gerentes

### Processo
Realizada um consulta na tabela de Empregados para criar a tabela de Emregados por Gerente.
Excluídas as colunas que não são relevantes para a análise.

## Etapa 12: Mesclagem dos Nomes e Sobrenomes

Combinadas as colunas de nome e sobrenome em uma única coluna.

## Etapa 13: Mesclagem dos Nomes de Departamentos e Localização

Garantir que cada combinação de departamento e local seja única.

### Processo
Criada uma nova consulta mesclando as tabelas departamento e localização.


## Etapa 14: Justificativa para Mesclagem em vez de Atribuição

"Mesclagem" cria uma nova consulta com uma combinação única de valores, facilitando a criação de modelos estrela e outras análises complexas.
"Acresentar" une todas as linhas das tabelas selecionadas resultando em colunas ou linhas redundantes.

## Etapa 15: Agrupamento de Dados por Gerente

Determinar o número de colaboradores por gerente.

### Processo
Utilizado o menu Combinar para acrescentar consultas e exibir o número de Empregados por Gerente.

## Etapa 16: Eliminação de Colunas Desnecessárias

Elimine as colunas desnecessárias, que não serão usadas no relatório

### Processo
Revisada cada tabela para identificar e excluir as colunas que não serão utilizadas.

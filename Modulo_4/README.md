# Desafio de Projeto - Criando um Star Schema para Cenários de Vendas com Power BI - DIO

Este relatório descreve as etapas para a transformação de um diagrama relacional padrão para um diagrama star schema.

## Configuração do diagrama relacional
Configuração das tabelas e relacionamentos:
- Tabela Professor
    idProfessor (PK)
    Departamento_idDepartamento (FK)

- Tabela Departamento
    idDepartamento (PK)
    Nome 
    Campus
    idProfessor_coordenador (FK)

- Tabela curso
    idCurso (PK)
    Departamento_idDepartamento (FK)
 
- Tabela Disciplina
    idDisciplina (PK)
    Professor_idProfessor (FK)

- Tabela Disciplina & curso
    Disciplina_idDisciplina (FK)
    Curso_idCurso (FK)

- Tabela Matriculado
    Aluno_idAluno (FK)
    Disciplina_idDisciplina (FK)

- Tabela Aluno
    idAluno (PK)

- Tabela Pré-requisitos das disciplinas
    Disciplina_idDisciplina (FK)
    Pré-requisitos_idPré-requisitos (FK)

- Tabela Pré-requisitos
    idPré-requisitos (PK)

## Modelagem Star Schema
- Com objetivo de analisar dados sobre os professores, a tabela professor foi escolhida com tabela fato.
- As tabelas Aluno e Matriculado foram excluídas por não serem relevantes para a análise.
- Criadas as tabelas dimensão utilizando as tabelas Departamento, Discplina e Curso.
- Criada a tabela Datas para mensurar as dastas de oferta dos cursos e disciplinas.

## Configuração do diagrama Star Schema

- Tabela: Professor_Fato
ID_Professor (PK);
Departamento_idDepartamento (FK);
Disciplina_idDisciplina (FK);
Curso_idCurso (FK);
Data_idData (FK);
Nome
Sobrenome
Salario


- Tabela: Departamento_Dimensão
IdDepartamento (PK)
Nome_departamento
Campus

- Tabela: Disciplina_Dimensão
idDisciplina (PK)
Nome_disciplina
Créditos

- Tabela: Curso_Dimensão
idCurso (PK)
Nome_curso
Tipo_Curso (Bacharelado, Licenciatura)

- Tabela: Datas_Dimensão
idData (PK)
Data (DATE)
Ano
Trimestre
Mês
Dia_da_Semana
Dia

### Relações
A tabela Professor_Fato se conecta a cada uma das tabelas de dimensão através das foreign keys, permitindo análises por departamento, disciplina, curso e datas.




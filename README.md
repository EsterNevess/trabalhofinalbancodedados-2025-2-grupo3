# Sistema de Gestão para Clínica Odontológica

Foi desenvolvido um **banco de dados** para um sistema de gestão de uma clínica odontológica, realizado por **Ester Neves, Thaís Assumpção, Victor Pinheiro, Pedro Vivarini, Kauê Martins**.

## Funcionalidades do Sistema

O sistema contempla as seguintes funcionalidades principais:

- Agendamento de consultas
- Registro de atendimentos
- Controle de profissionais (dentistas) e pacientes

## Estrutura do Banco de Dados

Foram criadas **4 tabelas** principais no banco de dados:

### 1. Paciente

Contém as seguintes informações:

- `id`
- `nome`
- `cpf`
- `data_nascimento`
- `telefone`
- `email`
- `endereco`
- `historico_consultas`

### 2. Dentista

Contém as seguintes informações:

- `id`
- `nome`
- `cpf`
- `cro`
- `especialidade`
- `horario_atendimento`


### 3. Consulta

Contém as seguintes informações:

- `id_consulta`
-  `id_dentista`
-  `id_paciente`
- `dentista_responsavel` (relacionamento com tabela dentista)
- `paciente` (relacionamento com tabela paciente)
- `data`
- `horario`
- `descricao`
- `prescricao`


### 4. Procedimento

Contém as seguintes informações:

- `id_procedimento`
- `nome`
- `descricao`
- `duracao_media`

> Foram inseridos **10 registros em cada tabela**.

## Modelagem do Banco de Dados

O banco de dados foi modelado em três níveis:

- **Modelo Conceitual**
- **Modelo Lógico**
- **Modelo Físico**

## Comandos SQL Utilizados

### Índices

- Criação de **2 índices** coerentes para otimizar consultas.

### Atualizações de Registros

- **3 comandos de atualização** com condições específicas aplicadas em tabelas do sistema.

### Exclusão de Registros

- **3 comandos de exclusão** com condições específicas aplicadas em tabelas do sistema.

### Contagem de Consultas

- `COUNT` de consultas realizadas por **especialidade**
- `COUNT` de consultas realizadas por **cada dentista**, exibidas em **ordem decrescente**

### Listagem de Pacientes e Consultas

- Consulta que lista os **pacientes** com a **quantidade de consultas realizadas**, ordenada em **ordem decrescente** pelo número de consultas.

### View SQL Criada

Foi criada uma `VIEW` com os seguintes campos:

- `id_consulta`
- `nome_paciente`
- `nome_dentista`
- `data`
- `procedimento_descrito`

> Ordenada em ordem **decrescente pela data da consulta**

### Média de Consultas por Dentista

- Comando SQL que calcula a **média de consultas realizadas por dentista**

# Estudo de Caso – Sistema de RH

### Professora Ellen Martins Lopes da Silva

## 📚 Sobre a Atividade

A atividade consiste em desenvolver um **Diagrama Entidade-Relacionamento (DER)** para o sistema de Recursos Humanos de uma empresa.

O objetivo é identificar as entidades, seus atributos e os relacionamentos, incluindo as cardinalidades necessárias para representar as regras de negócio.

## 🎯 Objetivos

- Identificar as entidades do sistema de RH.
- Definir os atributos de cada entidade.
- Identificar os relacionamentos entre as entidades.
- Determinar as cardinalidades.
- Elaborar um Diagrama Entidade-Relacionamento.

## 🗂️ Entidades do Sistema

### 1. Área de Lotação

Representa a área onde o empregado trabalha.

**Atributos:**
- Código da área
- Nome da área
- Endereço
- Código do centro de custo

**Regra:** cada área deve possuir pelo menos um empregado e pode possuir vários.

### 2. Empregado

Armazena as informações dos funcionários da empresa.

**Atributos:**
- Código do empregado
- Nome do empregado
- Endereço do empregado
- Número do RG
- Número do CPF
- Código da lotação
- Código do nível salarial
- Código do cargo

**Regras:**
- Todo empregado está vinculado obrigatoriamente a uma área de lotação.
- Todo empregado está vinculado a um cargo.
- Um empregado pode possuir nenhum, um ou vários dependentes.

### 3. Dependente

Armazena as informações dos dependentes dos empregados.

**Atributos:**
- Código do empregado
- Número do dependente
- Nome do dependente
- Data de nascimento
- Tipo de parentesco
- Número do documento de identidade
- Tipo de documento de identidade

**Regras:**
- Um empregado pode possuir zero ou vários dependentes.
- Todo dependente deve estar vinculado a um empregado.
- A identificação do dependente é composta pelo código do empregado e pelo número do dependente.

### 4. Cargo

Representa os cargos existentes na estrutura hierárquica da empresa.

**Atributos:**
- Código do cargo
- Nome do cargo
- Nível hierárquico
- Código no I.R.
- Indicador de nível gerencial
- Código da referência salarial mínima
- Código da referência salarial máxima

**Regras:**
- Todo empregado está vinculado a um cargo.
- Um cargo pode não possuir empregados ou possuir vários.

### 5. Referência Salarial

Armazena as informações dos níveis salariais.

**Atributos:**
- Código da referência salarial
- Data de início de vigência
- Data de final de vigência
- Valor do salário

**Regras:**
- Todo cargo está vinculado a uma referência salarial.
- Uma referência salarial pode estar relacionada a nenhum ou vários empregados.

## 🔗 Relacionamentos

| Entidades | Relacionamento |
|---|---|
| Área de Lotação e Empregado | Uma área possui um ou vários empregados. |
| Empregado e Dependente | Um empregado pode possuir zero ou vários dependentes. |
| Cargo e Empregado | Um cargo pode estar relacionado a zero ou vários empregados. |
| Cargo e Referência Salarial | Todo cargo está vinculado a uma referência salarial. |
| Referência Salarial e Empregado | Uma referência pode estar relacionada a zero ou vários empregados. |

## 📌 Regras de Identificação

- **Área de Lotação:** código alfanumérico único de seis posições.
- **Empregado:** código alfanumérico único de quatro posições.
- **Dependente:** código do empregado + número do dependente, com duas posições.
- **Cargo:** código alfanumérico de três posições.
- **Referência Salarial:** código alfanumérico único de três posições.

## 📝 Entrega da Atividade

A atividade solicita a elaboração de um **Diagrama Entidade-Relacionamento (DER)** contendo:

- Todas as entidades do sistema.
- Os atributos de cada entidade.
- Os relacionamentos entre as entidades.
- As cardinalidades correspondentes às regras de negócio.

## ✅ Conclusão

A modelagem do sistema de RH permite organizar as informações dos empregados, seus dependentes, suas áreas de lotação, seus cargos e suas referências salariais.

O DER será utilizado para representar visualmente essas informações e seus relacionamentos, servindo como base para a estruturação do banco de dados.

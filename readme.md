# Documentação do Modelo MVC

## Introdução

Este documento detalha a implementação do padrão MVC (Model-View-Controller) para um projeto desenvolvido no framework Sails.js. Ele apresenta uma visão clara da organização das entidades de dados (models), das interfaces de usuário (views) e da lógica de controle (controllers), demonstrando como cada componente contribui para a funcionalidade geral do sistema.

## Estrutura MVC

### Models

Representam a camada de dados e contêm a lógica de acesso a estes, sendo a representação das informações com as quais o sistema opera.

#### Modelo: Usuário
- **Atributos:**
  - `Id`: INTEGER (PK)
  - `Nome`: VARCHAR
  - `Data de Nascimento`: DATE
  - `CPF`: VARCHAR
  - `CEP`: VARCHAR
  - `Email`: VARCHAR
  - `Senha`: VARCHAR
  - `Bio`: TEXT
  - `Horas Voluntariadas`: INTEGER

#### Modelo: Ação
- **Atributos:**
  - `Id`: INTEGER (PK)
  - `Id Criador`: INTEGER (FK)
  - `Nome`: VARCHAR
  - `Bio`: TEXT
  - `Foto`: VARCHAR
  - `Vagas`: INTEGER
  - `Aberta`: BOOLEAN
  - `Data de Abertura`: DATE

### Views

Responsáveis pela apresentação dos dados ao usuário, definindo como os usuários interagem visualmente com a aplicação.

#### View: Landing Page
- **Componentes:**
  - Dados de Horas Totais
  - Imagens

#### View: Cadastro
- **Formulário de Registro:**
  - Nome
  - Data de Nascimento
  - CPF
  - CEP
  - Email
  - Senha

#### View: Login
- **Formulário de Login:**
  - Email
  - Senha

#### View: Home Page
- **Componentes:**
  - Ações Disponíveis
  - Voluntários

#### View: Perfil
- **Detalhes do Perfil:**
  - Nome
  - Bio
  - Foto

### Controllers

Definem a lógica de negócio e a interação entre o modelo e a view, gerenciando o fluxo de dados dentro da aplicação e respondendo a eventos, geralmente ações do usuário.

#### Controller: Usuário
- **Operações:**
  - Cadastro
  - Login
  - Candidatar a Ações
  - Criar Ações
  - Receber Convites
  - Consultar
  - Atualizar Perfil

#### Controller: Ação
- **Operações:**
  - Contar Horas Totais
  - Criar
  - Atualizar
  - Procurar
  - Deletar

## Diagrama MVC

A arquitetura deve ser esquematizada usando a ferramenta draw.io para refletir a organização das entidades, interfaces e lógicas de controle conforme descrito. Este diagrama facilitará a compreensão das inter-relações entre as diferentes partes do sistema.

---

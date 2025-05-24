
# 💡 Gerenciamento Bancário

Este projeto implementa um **sistema de gerenciamento bancário em Java**, estruturado com boas práticas de separação em camadas e uso do padrão DAO. Seu objetivo é simular as principais operações realizadas em uma conta bancária, como cadastro, movimentações financeiras e consultas, por meio de uma aplicação de linha de comando.

## 🎯 Objetivo

A aplicação permite:
- Cadastrar, alterar e remover contas bancárias
- Listar todas as contas cadastradas
- Realizar operações de débito, crédito e transferência entre contas
- Listar todos os movimentos financeiros registrados

## 🧱 Arquitetura

O projeto segue uma arquitetura em camadas, com destaque para os seguintes componentes:

- **Camada de Serviço de Aplicação (`AppService`)**: contém a lógica de negócio de alto nível e orquestra as operações entre os DAOs e os modelos.
- **Camada de Persistência (`DAO`)**: abstrai o acesso a dados por meio de interfaces e implementações concretas.
- **Camada de Domínio (`modelo`)**: contém as entidades centrais do sistema (`Conta`, `Movimento`).
- **Tratamento de Exceções**: classes dedicadas para tratar falhas de infraestrutura ou regras de negócio.
- **Utilitários**: como leitura via console e configuração com arquivos `.properties`.

## ⚙️ Tecnologias e Dependências

- **Java 17+**
- **Maven** (gerenciador de dependências)
- **Log4j** (logging)
- **Arquivos `.properties`** para configuração de DAO e log
- **Execução via Terminal (CLI)**

## ▶️ Como Executar

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   ```

2. **Compile o projeto com Maven**:
   ```bash
   mvn clean install
   ```

3. **Execute a aplicação**:
   - Localize a classe `Principal` (com método `main`) no diretório `src`.
   - Execute via terminal ou através de uma IDE como Eclipse ou IntelliJ.

## 📂 Estrutura do Projeto

```
├── src/
│   ├── modelo/               # Entidades do domínio
│   ├── dao/                  # Interfaces DAO
│   ├── dao/impl/             # Implementações concretas
│   ├── servico/              # Serviços de aplicação
│   ├── excecao/              # Exceções customizadas
│   └── Principal.java        # Classe principal (ponto de entrada)
├── resources/
│   ├── dao.properties        # Configuração de persistência
│   └── log4j.properties      # Configuração de logging
├── pom.xml                   # Gerenciador de dependências Maven
```

## 🧑‍💻 Consuderações

Projeto desenvolvido por mim (Matheus Belato) como parte de atividade acadêmica da disciplina de Projetos de Software, com contribuição do código do Professor Carlos Drummond da Universidade Federal Fluminense.

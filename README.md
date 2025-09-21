# 💸 FinanZen - Sistema de Gerenciamento de Despesas Pessoais

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-green.svg)
![Licença](https://img.shields.io/badge/license-todos%20os%20direitos%20reservados-green.svg)

*FinanZen* é uma plataforma robusta para gerenciamento de despesas, projetada para atender tanto usuários individuais quanto grupos (famílias, equipes). Oferece ferramentas avançadas para controle financeiro, incluindo orçamentos, suporte a múltiplas moedas e análises com inteligência artificial para insights valiosos.

## ✨ Principais Funcionalidades

### 👤 *Gestão de Contas e Segurança*
- *Autenticação Segura:* Cadastro com verificação por e-mail e login protegido por tokens JWT.
- *Segurança de Senhas:* Armazenamento seguro com hashing e salt.
- *Perfil de Usuário:* Edição de dados pessoais e avatar customizável.

### 💰 *Controle Financeiro Completo*
- *Gestão de Transações (CRUD):* Registro fácil de receitas e despesas.
- *Categorias Personalizadas:* Crie, edite e exclua categorias para organizar suas finanças.
- *Filtros Avançados:* Encontre transações por período, tipo, categoria ou grupo.
- *Suporte a Múltiplas Moedas:* Defina uma moeda principal e registre gastos em moedas estrangeiras com conversão automática baseada em taxas de câmbio atualizadas.

### 📊 *Dashboards e Relatórios*
- *Dashboard Intuitivo:* Resumo financeiro mensal (receitas, despesas e saldo).
- *Acompanhamento de Orçamentos:* Gráficos visuais para monitorar o progresso dos seus orçamentos por categoria.
- *Exportação Assíncrona:* Gere e baixe relatórios mensais em PDF e Excel sem travar a interface.

### 🤖 *Inteligência Artificial*
- *Categorização Automática:* Novas despesas são categorizadas automaticamente com base no seu histórico.
- *Análise de Padrões:* Detecção de anomalias (gastos duplicados, despesas acima da média) e insights proativos para melhorar sua saúde financeira.

### 👨‍👩‍👧‍👦 *Grupos e Despesas Compartilhadas*
- *Criação de Grupos:* Organize despesas em conjunto (Família, Viagem, Apartamento).
- *Visão Compartilhada:* Membros do grupo podem visualizar e adicionar transações.
- *Permissões:* Papéis de Administrador e Membro para gerenciar o acesso.

---

## 💻 Linguagens e Frameworks

As principais tecnologias utilizadas no desenvolvimento do FinanZen são:

<p align="left">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original-wordmark.svg" alt="Java" width="80"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/spring/spring-original-wordmark.svg" alt="Spring Boot" width="80"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original-wordmark.svg" alt="Python" width="80"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/angularjs/angularjs-original.svg" alt="Angular" width="80"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="TypeScript" width="80"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="Node.js" width="80"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="PostgreSQL" width="80"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="Docker" width="80"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/rabbitmq/rabbitmq-original-wordmark.svg" alt="RabbitMQ" width="80"/>
</p>

---

## 🛠 Tech Stack & Arquitetura

Este projeto utiliza uma arquitetura de microsserviços para garantir escalabilidade, resiliência e manutenibilidade.

| Camada | Tecnologia | Descrição |
| :--- | :--- | :--- |
| 🖥 *Frontend* | *Angular* (LTS) | Framework robusto para uma Single Page Application (SPA) reativa e moderna. |
| | *NgRx* (ou similar) | Gerenciamento de estado para garantir consistência e performance. |
| ⚙ *Backend (Principal)* | *Java & Spring Boot* | Construído sobre uma Arquitetura Hexagonal para isolar a lógica de negócio. |
| 🤖 *Microsserviço (IA)* | *Python & FastAPI* | Serviço dedicado para processamento de IA e geração de relatórios. |
| 🗃 *Banco de Dados* | *PostgreSQL* | Banco de dados relacional robusto e confiável. |
| 🔄 *Comunicação* | *API RESTful (JSON)* | Padrão de comunicação principal entre frontend e backend. |
| 🗣 *Mensageria*| *RabbitMQ* | Message broker para comunicação assíncrona entre os microsserviços. |
| 🔐 *Autenticação* | *JSON Web Tokens (JWT)* | Padrão para proteger as rotas da API. |
| 🐳 *Infraestrutura* | *Docker & Docker Compose*| Containerização para garantir um ambiente de desenvolvimento e produção consistente. |
| 📄 *Documentação* | *OpenAPI 3 & Swagger UI* | Documentação clara e interativa para a API. |

---

## 🚀 Como Executar o Projeto Localmente

### Pré-requisitos
- [Docker](https://www.docker.com/get-started) e [Docker Compose](https://docs.docker.com/compose/install/)
- [Node.js](https://nodejs.org/) e [Angular CLI](https://angular.io/cli)
- [Java](https://www.java.com/) (versão X) e [Maven](https://maven.apache.org/)
- [Python](https://www.python.org/) (versão X) e [Poetry](https://python-poetry.org/)

### Passos
1. *Clone o repositório:*
   ```bash
   git clone [https://github.com/seu-usuario/finanzen.git](https://github.com/seu-usuario/finanzen.git)
cd finanzen

2. *Suba os contêineres:*
   ```bash
   docker-compose up -d

3. *Instale as dependências e execute o Front-end*
    ```bash
    cd frontend
    npm install
    ng serve
Acesse a aplicação em http://localhost:4200

4. *Execute os Back-ends fora do Docker:*
* Back-end Principal (Java):
   ```bash
   cd backend-main
   mvn spring-boot:run

* Microsserviço de IA (Python):
   ```bash
   cd microservice-ai
   poetry install
   poetry run unicorn main:app
   --reload

---

### 📚 Documentação da API
A documentação completa da API, gerada com OpenAPI 3, está disponível para consulta e interação através do Swagger UI.

* URL da API Principal: http://localhost:8080/swagger-ui.html
* URL do Microsserviço de IA: http://localhost:8000/docs

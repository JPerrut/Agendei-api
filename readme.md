# 🏥 Agendei - Sistema de Agendamento Médico (Backend) [![Node.js](https://img.shields.io/badge/Node.js-18.x-green)](https://nodejs.org/) [![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

### 🚀 Visão Geral

Sistema completo para agendamento de consultas médicas, composto por:

- 📱 **Aplicativo Mobile** (Pacientes)
- 🖥️ **Painel Admin** (Gestores)
- 🚀 **Backend** (API RESTful)

Este repositório contém o **backend** do sistema, desenvolvido para fornecer uma API robusta e escalável.

## ✨ Características do Projeto

✅ Cadastro de Usuários e Médicos – Permite o registro de pacientes e médicos no sistema.
<br>
✅ Agendamento de Consultas – Interface para marcar, editar e cancelar consultas.
<br>
✅ Autenticação Segura – Utilização de JWT (JSON Web Tokens) para autenticação de usuários e administradores.
<br>
✅ Gerenciamento de Consultas – Visualização e edição de consultas agendadas pelos administradores.
<br>
✅ Desenvolvimento Moderno – Utilização de tecnologias como Express, SQLite e TypeScript.
<br>
✅ Performance Otimizada – Código leve e rápido, com foco na eficiência de carregamento.

## 🛠️ Tecnologias Utilizadas

### Backend

- **Node.js** – Ambiente de execução JavaScript para construir o servidor.

- **Express** – Framework web para criação de APIs RESTful.

- **SQLite** – Banco de dados leve e embutido para armazenamento de dados.

- **JSON Web Tokens (JWT)** – Autenticação segura e stateless.

- **Bcrypt** – Biblioteca para criptografia de senhas.

- **CORS** – Middleware para habilitar o compartilhamento de recursos entre origens diferentes.

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original-wordmark.svg" width="30" height="30"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/express/express-original.svg" width="30" height="30" />
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/sqlite/sqlite-original.svg" width="30" height="30"/>

## Como Rodar o Projeto Localmente

### Pré-requisitos

- Node.js (versão 18 ou superior)
- SQLite – Banco de dados embutido.
- npm ou yarn (gerenciadores de pacotes)

### Passos

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/agendei-api.git
   ```
2. Acesse a pasta do projeto:
   ```bash
   cd agendei-api
   ```
3. Instale as dependências:
   ```bash
   npm install
   ```
4. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```
5. O servidor estará rodando em:
   ```bash
   http://localhost:3001
   ```

## Rotas da API

Abaixo estão os principais endpoints disponíveis para teste:

### Appointments

- Listar
  ```bash
  GET http://localhost:3001/appointments
  ```
- Inserir
  ```bash
  POST http://localhost:3001/appointments
  ```
  body - raw:
  ```bash
  {
      "id_doctor": 1,
      "id_service": 1,
      "booking_date": "2025-01-15",
      "booking_hour": "00:45"
  }
  ```

### Doctors

- Listar
  ```bash
  GET http://localhost:3001/doctors?
  ```
- Serviços
  ```bash
  GET http://localhost:3001/doctors/2/services
  ```
- Inserir

  ```bash
  POST http://localhost:3001/doctors
  ```

  body - raw:

  ```bash
  {
      "name": "Dr. Teste",
      "specialty": "Clinico Geral",
      "icon": "m"
  }
  ```

- Editar

  ```bash
  PUT http://localhost:3001/doctors/7
  ```

  body - raw:

  ```bash
  {
      "name": "Dr. João Costa Filho",
      "specialty": "Cardiologista",
      "icon": "m"
  }
  ```

- Excluir
  ```bash
  DELETE http://localhost:3001/doctors/8
  ```
  body - raw:
  ```bash
  {
      "name": "Dra. Nise da Silveira",
      "specialty": "Endocrinologista",
      "icon": "F"
  }
  ```

### Users

- Inserir
  ```bash
  POST http://localhost:3001/users/register
  ```
  body - raw:
  ```bash
  {
      "name": "João Pedro",
      "email": "joao@teste.com.br",
      "password": "12345"
  }
  ```
- Login
  ```bash
  POST http://localhost:3001/users/login
  ```
  body - raw:
  ```bash
  {
      "email": "joao@teste.com.br",
      "password": "12345"
  }
  ```

### Como Testar

Você pode testar as rotas usando ferramentas como <a href="https://www.postman.com">Postman</a>, <a href="https://insomnia.rest">Insomnia</a> ou diretamente no terminal com `curl`.

**Exemplo com `curl`:**

```bash
curl -X GET http://localhost:3000/appointments
```

## Contribuição

### Contribuições são bem-vindas! Siga os passos abaixo:

1. Faça um fork do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`).
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`).
4. Faça push para a branch (`git push origin feature/nova-feature`).
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a <a href="https://opensource.org/license/mit">MIT License</a>.

## Contato

### Se tiver dúvidas ou sugestões, entre em contato:

Nome: João Perrut <br>
Email: joaoperrutc@gmail.com <br>
Linkedin: https://www.linkedin.com/in/perrut/

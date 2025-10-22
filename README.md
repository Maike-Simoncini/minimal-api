# 🚗 Gerenciamento de Veículos - API com ASP.NET Minimal APIs

Este projeto foi desenvolvido durante o bootcamp da **[DIO – Codifique o seu futuro global agora](https://web.dio.me/)**. A aplicação é uma API REST construída com **ASP.NET Minimal APIs**, utilizando **Entity Framework Core**, **JWT para autenticação**, **Swagger/OpenAPI** para documentação e **testes automatizados**.

## 📌 Funcionalidades

- ✅ Autenticação de administradores com **login/senha** e geração de **token JWT**
- 🔐 Autorização por perfil: **Administrador** e **Editor**
- 🚘 CRUD completo de **Veículos** (criar, listar, atualizar, deletar)
- 🧪 Validações de entrada nos endpoints de veículos
- 📚 Documentação interativa com **Swagger**
- 🧪 Testes de unidade e testes de integração (requests)
- 🚀 Pronto para deploy em nuvem

## 🛠️ Tecnologias Utilizadas

- **ASP.NET Core 7+** (Minimal APIs)
- **Entity Framework Core** (Code First)
- **SQLite** (banco de dados em memória/disco para desenvolvimento)
- **JWT (JSON Web Token)** para autenticação
- **Swagger/OpenAPI** para documentação dos endpoints
- **xUnit / FluentAssertions** para testes
- **.NET CLI** e **Visual Studio / VS Code**

## 📦 Pré-requisitos

- [.NET 7 SDK ou superior](https://dotnet.microsoft.com/download)
- (Opcional) Visual Studio / VS Code com extensões C#
- (Opcional) SQLite Browser ou ferramenta de banco de dados

## 🚀 Como Executar o Projeto

1. **Clone o repositório**
   ```bash
   git clone <url-do-seu-repo>
   cd nome-do-projeto
   ```

2. **Restaure as dependências**
   ```bash
   dotnet restore
   ```

3. **Aplique as migrações do banco de dados**
   ```bash
   dotnet ef database update
   ```

4. **Execute a aplicação**
   ```bash
   dotnet run
   ```

5. **Acesse a documentação da API**
   - Abra no navegador: [https://localhost:5001/swagger](https://localhost:5001/swagger)  
     *(ou a porta exibida no terminal)*

## 🔐 Autenticação

- **Endpoint de login**: `POST /login`
  - Corpo da requisição (JSON):
    ```json
    {
      "email": "admin@dio.com",
      "password": "123456"
    }
    ```
  - Retorna um token JWT que deve ser usado nos headers das requisições protegidas:
    ```
    Authorization: Bearer <seu-token-aqui>
    ```

> Um administrador padrão é criado automaticamente via **Seed** na primeira execução.

## 🧪 Testes

O projeto inclui:
- Testes de unidade para o modelo de `Administrador`
- Testes de persistência com banco em memória
- Testes de requisição HTTP (endpoints)

Execute os testes com:
```bash
dotnet test
```

## 📁 Estrutura do Projeto

```
/src
  ├── GerenciamentoVeiculos.Api/     # Projeto principal da API
  └── GerenciamentoVeiculos.Tests/   # Projeto de testes
GerenciamentoVeiculos.sln            # Solução .NET
```

## 🌐 Deploy

A aplicação está pronta para ser implantada em provedores como:
- Azure App Service
- AWS Elastic Beanstalk
- Railway / Render (com Docker, se necessário)

## 📚 Referências

- [Documentação oficial do ASP.NET Minimal APIs](https://learn.microsoft.com/pt-br/aspnet/core/fundamentals/minimal-apis)
- [DIO – Codifique o seu futuro global agora](https://web.dio.me/)

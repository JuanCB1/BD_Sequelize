# BD_TypeORM
Projeto de exemplo de banco de dados interativo usando **Sequelize** e **SQLite** em Node.js.

---

## 📚 O que é o Sequelize?

**Sequelize** é um ORM (Object-Relational Mapping) para Node.js. Isso significa que ele permite trabalhar com banco de dados usando JavaScript/Node.js, sem precisar escrever SQL manualmente.

### Vantagens do Sequelize:

- ✅ **Escreve código JavaScript** ao invés de SQL puro
- ✅ **Funciona com vários bancos** (PostgreSQL, MySQL, SQLite, etc.)
- ✅ **Validações automáticas** (ex: email válido, campos obrigatórios)
- ✅ **Relacionamentos fáceis** entre tabelas
- ✅ **Migrações** para controlar versões do banco
- ✅ **Seguro contra SQL Injection** (proteção automática)

---

## 📦 Como Instalar

### ⚠️ Importante: Estrutura de Pastas

**Você NÃO precisa criar as pastas manualmente!** Este projeto já vem com toda a estrutura pronta:

```
pi/
├── src/
│   ├── database/     ✅ Já existe
│   ├── models/       ✅ Já existe
│   └── Teste.js ✅ Já existe
```

**Se você baixou/clonou este projeto:**  
Tudo já está pronto! Apenas execute `npm install` e depois `npm start`.

**Se você quer criar um projeto do zero:**  
Veja a seção "🔨 Criando um Projeto do Zero" no final deste README.

---

### 1. Pré-requisitos

Você precisa ter instalado:
- **Node.js** (versão 18 ou superior)
- **npm** (vem junto com o Node.js)

### 2. Instalar as Dependências

Abra o terminal na pasta do projeto e execute:

```bash
npm install sequelize sqlite3
```

Este comando vai instalar automaticamente:
- `sequelize` - O ORM principal
- `sqlite3` - Driver para trabalhar com SQLite

**Nota:** As pastas `src/`, `src/database/` e `src/models/` já existem no projeto. Você só precisa instalar as dependências!

---
## 🛠️ Passo a passo: criando seu banco com Sequelize

1. **Baixe o projeto**  
   - Clone com `git clone` ou faça download do ZIP e extraia para uma pasta.
   - Entre na pasta:  
     ```bash
     cd pi
     ```

2. **Instale as dependências**  
   ```bash
   npm install sequelize sqlite3
   ```
   Isso baixa o Sequelize, o driver SQLite.

3. **(Opcional) Configure o `.env`**  
   Crie um arquivo `.env` na raiz e personalize:
   ```env
   DATABASE_STORAGE=database.sqlite
   DATABASE_LOGGING=false
   ```

4. **Inicialize o banco**  
   Rode o script interativo (ele cria o arquivo `database.sqlite` automaticamente se ainda não existir):
   ```bash
   npm start
   ```
   Você verá a mensagem `✅ Banco de dados pronto!` no terminal.

5. **Cadastre seus primeiros dados**  
   - Escolha a opção `1` para criar um usuário.  
   - Informe nome, email e role.  
   - O registro é salvo na tabela `users`.

6. **Verifique se deu certo**  
   - Use a opção `2` para listar todos os usuários.  
   - O arquivo `database.sqlite` aparece na pasta do projeto com os dados salvos.

---

## 🎯 Conceitos Importantes

### Modelo (Model)
Um modelo representa uma tabela do banco de dados. Exemplo: o modelo `User` representa a tabela `users`.

### ORM (Object-Relational Mapping)
Traduz objetos JavaScript em comandos SQL e vice-versa. Você trabalha com objetos, o Sequelize cuida do SQL.

### SQLite
Banco de dados leve que salva tudo em um único arquivo (`.sqlite`). Perfeito para projetos pequenos e testes.

---

## 📖 Operações CRUD

O projeto demonstra todas as operações básicas:

- **C**reate (Criar) - `User.create()`
- **R**ead (Ler) - `User.findAll()`, `User.findByPk()`
- **U**pdate (Atualizar) - `User.update()`
- **D**elete (Deletar) - `User.destroy()`

---
## 🐛 Solução de Problemas

### Erro: "npm não é reconhecido"
- Instale o Node.js: https://nodejs.org/
- Reinicie o terminal após instalar

### Erro: "Cannot find module"
- Execute: `npm install` novamente

### Erro de permissão no PowerShell
- Use `npm.cmd` ao invés de `npm`
- Ou configure o alias (já está configurado no projeto)

---

## 📚 Aprender Mais

- **Documentação oficial do Sequelize:** https://sequelize.org/
- **Documentação do Node.js:** https://nodejs.org/docs/
- **SQLite:** https://www.sqlite.org/

---

## 💡 Dicas

1. **Backup:** O arquivo `database.sqlite` contém todos os dados. Faça backup regularmente!

2. **Novos Modelos:** Para adicionar novas tabelas, crie arquivos em `src/models/` seguindo o exemplo de `User.js`.

---
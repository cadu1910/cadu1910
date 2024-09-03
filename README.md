Você foi contratado para desenvolver um sistema de gerenciamento de biblioteca que inclui funcionalidades básicas para gerenciar livros, autores e empréstimos. O sistema deve permitir:

Cadastro de Autores: Registro de autores com nome e nacionalidade.
Cadastro de Livros: Registro de livros com título, autor, ano de publicação e gênero.
Empréstimos de Livros: Registro de empréstimos de livros com a data de empréstimo, data de devolução (se aplicável) e nome do usuário.
Consultas: Consultar todos os livros e seus autores, bem como listar empréstimos em aberto.
Atualizações e Exclusões: Atualizar datas de devolução de empréstimos e excluir livros e seus registros de empréstimos associados.
# Sistema de Gerenciamento de Biblioteca

## Descrição

Este projeto é um sistema de gerenciamento de biblioteca que inclui tabelas para armazenar informações sobre autores, livros e empréstimos. O sistema permite o cadastro de autores e livros, além de gerenciar empréstimos e consultas de dados.

## Estrutura do Banco de Dados

O banco de dados é composto por três tabelas principais:

1. **Autores**: Armazena informações sobre os autores.
   - `AutorID` (INT, PK): Identificador único do autor.
   - `Nome` (VARCHAR): Nome do autor.
   - `Nacionalidade` (VARCHAR): Nacionalidade do autor.

2. **Livros**: Armazena informações sobre os livros.
   - `LivroID` (INT, PK): Identificador único do livro.
   - `Titulo` (VARCHAR): Título do livro.
   - `AutorID` (INT, FK): Identificador do autor.
   - `AnoPublicacao` (YEAR): Ano de publicação do livro.
   - `Genero` (VARCHAR): Gênero do livro.

3. **Emprestimos**: Armazena informações sobre os empréstimos de livros.
   - `EmprestimoID` (INT, PK): Identificador único do empréstimo.
   - `LivroID` (INT, FK): Identificador do livro.
   - `DataEmprestimo` (DATE): Data em que o livro foi emprestado.
   - `DataDevolucao` (DATE): Data em que o livro foi devolvido (pode ser NULL se não devolvido ainda).
   - `NomeUsuario` (VARCHAR): Nome do usuário que emprestou o livro.

## Como Executar

1. **Criar o Banco de Dados e Tabelas**
   Execute o script SQL fornecido para criar o banco de dados `Biblioteca`, bem como as tabelas `Autores`, `Livros`, e `Emprestimos`.

2. **Inserir Dados**
   Execute as instruções de inserção fornecidas para popular as tabelas com dados de exemplo.

3. **Consultar Dados**
   Utilize as consultas SQL fornecidas para listar livros com autores e empréstimos em aberto.

4. **Atualizar Dados**
   Modifique registros de empréstimos conforme necessário utilizando as instruções de atualização fornecidas.

5. **Excluir Dados**
   Utilize as instruções de exclusão para remover livros e registros de empréstimos associados.

## Scripts SQL

- **Script de Criação do Banco de Dados**: Cria o banco de dados e as tabelas.
- **Script de Inserção de Dados**: Insere dados exemplo nas tabelas.
- **Consultas SQL**: Exemplos de consultas para extrair informações úteis.
- **Atualização e Exclusão de Dados**: Exemplos de atualização e exclusão de dados.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).


# Sistema de Gerenciamento de Produtos

Este projeto é uma aplicação web básica para gerenciar produtos. Ele foi desenvolvido utilizando Java, Servlets, JSP, JDBC e MySQL, seguindo o padrão MVC.

## Estrutura do Projeto

### 1. **Produto.java**

Esta classe representa o modelo de dados de um produto. Ela inclui os seguintes atributos e métodos:

- **Atributos:**
  - `id`: Identificador único do produto.
  - `nome`: Nome do produto.
  - `descricao`: Descrição do produto.
  - `preco`: Preço do produto.
  - `data_inclusao`: Data de inclusão do produto.

- **Métodos:**
  - Construtores para inicializar objetos.
  - Getters e setters para acessar e modificar os atributos.

**Localização:** `src/model/Produto.java`

---

### 2. **ProdutoServlet.java**

Esta servlet gerencia as requisições HTTP relacionadas ao gerenciamento de produtos. As ações suportadas incluem:

- Listar produtos (com suporte a busca por nome).
- Inserir um novo produto.
- Editar um produto existente.
- Atualizar as informações de um produto.
- Deletar um produto.

**Localização:** `src/controller/ProdutoServlet.java`

---

### 3. **ProdutoDAO.java**

Classe responsável por realizar as operações de banco de dados (CRUD) para a entidade `Produto`. Utiliza JDBC para conectar ao banco de dados MySQL.

- **Métodos:**
  - `insertProduto`: Insere um novo produto.
  - `selectProduto`: Retorna um produto pelo seu ID.
  - `selectAllProduto`: Lista todos os produtos.
  - `updateProduto`: Atualiza as informações de um produto.
  - `deleteProduto`: Remove um produto.
  - `searchProdutoByName`: Busca produtos pelo nome (suporte a consultas parciais).

**Localização:** `src/dao/ProdutoDAO.java`

---

### 4. **produto-list.jsp**

Página JSP para exibir a lista de produtos. Possui recursos para:

- Exibir todos os produtos em uma tabela.
- Realizar buscas por nome.
- Navegar para a criação ou edição de produtos.
- Excluir produtos.

**Localização:** `webapp/produto-list.jsp`

---

### 5. **produto-form.jsp**

Página JSP para criar ou editar produtos. Inclui um formulário com campos para:

- Nome.
- Descrição.
- Preço.
- Data de Inclusão.

O formulário se adapta automaticamente para inserção ou edição, dependendo da ação realizada.

**Localização:** `webapp/produto-form.jsp`

---

### 6. **Dependências do Projeto**

- **Java:** 11+
- **MySQL:** Para o banco de dados.
- **Bibliotecas:**
  - JSTL para iteração e exibição dinâmica.
  - Bootstrap 5 para o design responsivo.
- **Driver JDBC:** `mysql-connector-java`

---

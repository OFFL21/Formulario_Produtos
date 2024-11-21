# Sistema de Gerenciamento de Produtos

Este projeto é uma aplicação web básica para gerenciar produtos. Ele foi desenvolvido utilizando **Java**, **Servlets**, **JSP**, **JDBC** e **MySQL**, seguindo o padrão MVC.

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

## Ferramentas Utilizadas 🛠️

| Ferramenta                  | Função                                      | Ícone                                                                                         |
|-----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------|
| **Java**                    | Linguagem de programação principal          | ![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white) |
| **Servlets**                | Controle de requisições HTTP                | ![Servlet](https://img.shields.io/badge/Servlet-4CAF50?style=for-the-badge&logo=java&logoColor=white) |
| **JSP**                     | Renderização de páginas dinâmicas           | ![JSP](https://img.shields.io/badge/JSP-blue?style=for-the-badge&logo=java&logoColor=white)   |
| **JDBC**                    | Conexão com banco de dados                  | ![JDBC](https://img.shields.io/badge/JDBC-orange?style=for-the-badge&logo=java&logoColor=white) |
| **MySQL**                   | Banco de dados relacional                   | ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white) |
| **Bootstrap**               | Estilização e responsividade                | ![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white) |
| **Tomcat**                  | Servidor de aplicação para Java             | ![Tomcat](https://img.shields.io/badge/Tomcat-F8DC75?style=for-the-badge&logo=apache-tomcat&logoColor=black) |
| **Eclipse IDE** ou **IntelliJ IDEA** | IDEs para desenvolvimento             | ![Eclipse](https://img.shields.io/badge/Eclipse-2C2255?style=for-the-badge&logo=eclipse&logoColor=white)  |

---


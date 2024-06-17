# Cantina App

## Sobre a Aplicação

Cantina App é uma aplicação de e-commerce para pedidos de comida, desenvolvida como parte de um projeto acadêmico. A aplicação permite aos usuários se registrarem, fazer login, navegar por um menu de itens de comida, adicionar itens ao carrinho e completar pedidos com pagamento via QR code para PIX.

## Tecnologias Usadas

- **Front-end:** React, Bootstrap, CSS
- **Back-end:** Java, Spring Boot, MongoDB
- **Outras Ferramentas:** Axios, jsPDF, UUID, QRCode.react

## Estrutura do Código

### Front-end

- `src/components`: Contém componentes reutilizáveis da interface do usuário.
- `src/pages`: Contém as principais páginas da aplicação (Home, Login, Register, Dashboard, Cart, Checkout).
- `src/CartContext.js`: Contexto do carrinho para gerenciar o estado do carrinho de compras.
- `src/UserContext.js`: Contexto do usuário para gerenciar o estado de autenticação do usuário.

### Back-end

- `src/main/java/com/cantina`: Contém os pacotes do Spring Boot para a aplicação.
    - `controller`: Contém os controladores REST (UserController, FoodItemController, etc.).
    - `entity`: Contém as classes de entidade (User, FoodItem, etc.).
    - `repository`: Contém as interfaces de repositório para interagir com o MongoDB.
    - `service`: Contém as classes de serviço para a lógica de negócios.
    - `config`: Configurações de segurança e CORS.

## Requisitos para Executar a Aplicação

- **Node.js** (versão 12 ou superior)
- **npm** ou **yarn**
- **Java** (JDK 11 ou superior)
- **Maven**
- **MongoDB** (local ou em nuvem)

## Como Executar

### Backend

1. Clone o repositório:
    ```bash
    git clone https://github.com/seu-usuario/cantina-app.git
    cd cantina-app
    ```

2. Navegue até a pasta `cantina-app`:
    ```bash
    cd cantina-app
    ```

3. Configure o MongoDB:
    - Crie um cluster no MongoDB Atlas ou configure um MongoDB local.
    - Atualize a URI do MongoDB no `application.properties`:

    ```properties
    spring.data.mongodb.uri=mongodb+srv://usuario:senha@cluster0.mongodb.net/cantina?retryWrites=true&w=majority
    ```

4. Compile e execute o backend:
    ```bash
    mvn clean install
    mvn spring-boot:run
    ```

### Frontend

1. Navegue até a pasta `cantina-front`:
    ```bash
    cd cantina-front
    ```

2. Instale as dependências:
    ```bash
    npm install
    ```

3. Execute a aplicação React:
    ```bash
    npm start
    ```

4. Acesse a aplicação em [http://localhost:3000](http://localhost:3000).

## Funcionalidades

- **Registro e Login:** Os usuários podem se registrar e fazer login para acessar a aplicação.
- **Menu:** Exibe uma lista de itens de comida disponíveis para compra.
- **Carrinho:** Permite adicionar, remover e atualizar a quantidade de itens no carrinho.
- **Checkout:** Gera um PDF de confirmação do pedido com QR code para pagamento via PIX.
- **Persistência de Dados:** Os dados de usuários e itens são armazenados no MongoDB.

## Contribuição

Se você quiser contribuir para o projeto, sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

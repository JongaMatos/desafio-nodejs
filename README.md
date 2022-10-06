# Desafios trilha de NodeJS 

## Objetivos

Este projeto se trata do desafio da trilha de NodeJs ,criada pelo Squad de capacitação da Empresa Junior Orc'estra Gamificação, que visa a pratica dos conceitos de NodeJs e Express. E neste documento se encontram detalhados os requisitos não-funcionais (restrições) e funcionais (que devem ser desenvolvidos).

## Requisitos não-funcionais (restrições)

| Código | Descrição                                                                                               |
|:------:|:------------------------------------------------------------------------------------------------------- |
|  RN01  | Este projeto deve ser desenvolvido no formato de uma API Rest.                                          |
|  RN02  | Este projeto deve ser desenvolvido na linguagem Javascript/Typescript, com o uso da biblioteca Express. |
|  RN03  | Todos os Requisitos funcionais dentro da sessão "Obrigatório" devem ser desenvolvidos. |
|  RN04  | Toda e qualquer forma de autenticação deve ser feita atraves de JWT's ( JSON Web Tokens). |


## Desafio 1

### Requisitos funcionais


#### Lista de tarefas:

| Código | Descrição                                                    |
| :----: | :----------------------------------------------------------- |
|  RF01  | Um usuário deve ser capaz de criar uma lista de tarefas, com a rota `/list/` e o método **POST**. |
|  RF02  | Um usuário deve ser capaz de editar a descrição de suas listas de tarefas, com a rota `/list/`  e o método **PATCH**. |
|  RF03  | Um usuário deve ser capaz de excluir uma lista de tarefas, com a rota `/list/` e o método **DELETE**. |
|  RF04  | Ao excluir uma lista de tarefas, todas as tarefas relacionadas a mesma devem ser excluídas. |
|  RF05  | Um usuário deve ser capaz de visualizar todas as suas listas cadastradas, com a rota `/list/all` e o método **GET**. |
|  RF06  | Um usuário deve ser capaz de visualizar uma unica lista cadastrada, com a rota `/list/:id` e o método **GET**.(devem ser visiveis todas as tarefas desta lista). |

#### Tarefas:

| Código | Descrição                                                    |
| :----: | ------------------------------------------------------------ |
|  RF07  | Um usuário deve ser capaz de criar uma tarefa associada a uma lista de tarefas, com a rota `/task/` e o método **POST**|
|  RF08  | Um usuário deve ser capaz de editar tanto o status quanto a descrição de suas tarefa, com a rota `/task/` e o método **PATCH**. |
|  RF09  | Um usuário deve ser capaz de excluir uma tarefa , com a rota `/task/` e o método **DELETE**. |


## Desafio 2 

| Código | Descrição                                                                                              |
|:------:| ------------------------------------------------------------------------------------------------------ |
|  RF10  | Um usuário deve ser capaz de criar uma nova conta, com a rota `/user/` e o método **POST**.     |
|  RF11  | Um usuário deve ser capaz de excluir sua conta, com a rota `/user/` e o método **DELETE**.                 |
|  RF12  | Ao excluir uma conta, todas as listas e tarefas associadas a mesma devem ser excluidas .               |
|  RF013 | Cada lista criada deve conter uma referencia ao usuário ao qual ela pertence . |
|  RF14  | O usuário deve receber um JWT contendo seu Id, após enviar corretamente seu usuário e senha, na rota `/user/login/`. |
|  RF15 | O usuário só deve ser capaz de visualizar dados de sua própria conta (dados cadastrais/listas de tarefas/tarefas). |
|  RF16  | Caso o usuário tente acessar os dados de outro, ele deve receber uma mensagem de erro "Não autorizado" . |
|  RF17  | O usuário deve ser capaz de provar sua identidade informando um token de atenticação válido, recebendo o erro "Login expirado" se o mesmo extiver vencido e "Token invalido para outros erros". |


## Como rodar localmente

1. Certifique se que os sequintes encontram-se instalados:
    - Docker
    - Docker-compose
    - NodeJs (versão 16)
    - Yarn
    - Git 
2. Clone e instale:
    - Clone o repositório com o seguinte comando:
    ``` bash
        git clone https://github.com/JongaMatos/desafio-nodejs-2022-1.git
     ```
     - Navegue para dentro do diretório criado com o comando:
     ```bash
        cd desafio-nodejs-2022-1
     ```
    - E por fim, instale as dependencias do projeto com o comando:
    ```bash
        sudo yarn install
    ```
3. Adicionar variável de ambiente:
    - Criar um arquivo .env na raiz do projeto.
    - Adicionar uma variável SECRET, com uma string aleatória contendo apenas caracteres alfanuméricos e sem espaço.
    ```yml
        #exemplo
        SECRET=917B13A9091915D54B6336F45909539CCE452B3661B21F386418A257883B30A

    ```

4. Rodando a aplicação:
    Uma vez que os passos acima tenham sido cumpridos, deve se:
    - Na primeira vez, rodar:
    ```bash
        sudo docker-compose up --build
    ```
    - Nas vezes seguintes:
    ```bash
        sudo docker-compose up
    ```

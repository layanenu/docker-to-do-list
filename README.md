<strong>Docker Todo List :pencil:</strong>

<strong>:wavy_dash: Sobre</strong>

Nesse projeto foi dado uma aplicação full-stack, um aplicativo de tarefas, que precisava ser conteinerizado para funcionar.

O objetivo do projeto foi conteinerizar aplicações, criar uma conexão entre elas e orquestrar seu funcionamento.

<details>
  <summary><strong> Stacks </strong></summary><br />
  * Bash
  * Docker
  * React JS
  * Node JS
</details>

<strong>:wavy_dash: Layout</strong>

![gif](https://user-images.githubusercontent.com/99842422/234355788-3dd30ea9-240b-408c-a96b-533bb7ca99a6.gif)


<details>
  <summary><strong> :whale: Rodando com o Docker</strong></summary><br />

  Clone o repositório:
  ```bash
  git clone git@github.com:layanenu/docker-to-do-list.git
  ```

  Entre no diretório docker-to-do-list:
  ```bash
  cd docker-todo-list
  ```

  Instale as dependências:
  ```bash
  npm install
  ```

  Entre no diretório docker:
  ```bash
  cd docker
  ```

  Faça o build das imagens de back-end, front-end e testes
  ```bash
  docker image build -t todobackend ./todo-app/back-end
  docker image build -t todofrontend ./todo-app/front-end
  docker image build -t todotests ./todo-app/tests
  ```

  Suba e orquestre os containers
  ```bash
  docker-compose up -d
  ```

  Para rodar os teste de funcionamento da aplicação
  ```bash
  docker attach docker-todotests-1
  ```

  Para executar a aplicação acesse o endereço abaixo no browser
  ```bash
  http://localhost:3000
  ```
 </details>

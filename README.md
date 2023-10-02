# To-do List

[![NPM](https://img.shields.io/npm/l/react)](https://github.com/OArthur-Rocha/API-REST-Voll-Med/blob/main/LICENSE)

# Sobre o projeto

API que gerencia uma To-do list, fazendo CRUD das tarefas, que faz parte do [desafio da Simplify](https://github.com/simplify-liferay/desafio-junior-backend-simplify) para desenvolvedores backend júnior. 
Feito com instruções da [Giuliana Bezerra](https://github.com/giuliana-bezerra).


## Tecnologias
 
- [Spring Boot](https://spring.io/projects/spring-boot)
- [Spring MVC](https://docs.spring.io/spring-framework/reference/web/webmvc.html)
- [Spring Data JPA](https://spring.io/projects/spring-data-jpa)
- [SpringDoc OpenAPI 3](https://springdoc.org/v2/#spring-webflux-support)
- [Mysql](https://dev.mysql.com/downloads/)

## Práticas adotadas

- SOLID, DRY, YAGNI, KISS
- API REST
- Consultas com Spring Data JPA
- Injeção de Dependências
- Tratamento de respostas de erro
- Geração automática do Swagger com a OpenAPI 3

## Como Executar

- Clonar repositório git
- Construir o projeto:
```
$ ./mvnw clean package
```
- Executar a aplicação:
```
$ java -jar target/todolist-0.0.1-SNAPSHOT.jar
```

A API poderá ser acessada em [localhost:8080](http://localhost:8080).
O Swagger poderá ser visualizado em [localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

## API Endpoints

As requisições foram feitas usando o aplicativo Insomnia.


- Criar tarefa:
  ```
  $ POST http://localhost:8080/todos
  
  {
	"nome": "Todo 1",
	"descricao": "Desc todo 1",
	"prioridade": 1
  }

  [
    {
      "id": 1,
      "nome": "Todo 1",
      "descricao": "Desc todo 1",
      "realizado": false,
      "prioridade": 1
    }
  ]
  ```
  - Listar tarefa:
```
$ GET http://localhost:8080/todos

[
  {
    "id": 1,
    "nome": "Todo 1",
    "descricao": "Desc todo 1",
    "realizado": false,
    "prioridade": 1
  }
]
```
- Atualizar tarefa:
```
$ PUT http://localhost:8080/todos

{
  "id": 1,
  "nome": "Todo 1",
  "descricao": "Desc todo 1",
  "realizado": true,
  "prioridade": 1
}
  
[
  {
    "id": 1,
    "nome": "Todo 1",
    "descricao": "Desc todo 1",
    "realizado": true,
    "prioridade": 1
  }
]
```
- Excluir tarefa:
```
$ DELETE http://localhost:8080/todos/1

[]
```



# Autor

Arthur Rocha

https://www.linkedin.com/in/oarthur-rocha/

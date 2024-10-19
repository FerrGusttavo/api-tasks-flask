
# API de Tarefas

Uma API simples construída em Python, e utilizando o framework Flask. Com um CRUD para tarefas.


## Rodando localmente

Clone o projeto

```bash
  git clone https://github.com/FerrGusttavo/api-tasks-flask.git
```

Entre no diretório do projeto

```bash
  cd api-tasks-flask
```

Instale as dependências

```bash
  pip install -r requirements.txt
```

Inicie o servidor

```bash
  python app.py
```


## Documentação da API

#### Criar uma tarefa

```http
  POST /tasks
```

- Cria uma nova tarefa na lista.

| Parâmetro (Body)   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `title`      | `string` | **Obrigatório**. Título da tarefa a ser criada.|
| `description` | `string` | **Opcional**. Descrição da tarefa a ser criada.

#### Retornar todas as tarefas


```http
  GET /tasks
```

- Retorna a lista completa de todas as tarefas criadas.

#### Retornar uma tarefa específica 


```http
  GET /tasks/<id>
```

- Retorna os detalhes de uma tarefa específica pelo seu id.

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `id`      | `int` | **Obrigatório**. O ID da tarefa a ser retornada. |

#### Atualizar uma tarefa

```http
  PUT /tasks/<id>
```

- Atualiza os dados de uma tarefa existente.

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `id`      | `int` | **Obrigatório**. O ID da tarefa a ser atualizada. |

| Parâmetro (Body)   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `title`      | `string` | **Obrigatório**. Título da tarefa a ser atualizada.|
| `description` | `string` | **Obrigatório**. Descrição da tarefa a ser atualizada.
| `completed` | `boolean` | **Obrigatório**. Status da tarefa a ser atualizada.

#### Deletar uma tarefa

```http
  DELETE /tasks/<id>
```

- Remove uma tarefa específica da lista.

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `id`      | `int` | **Obrigatório**. O ID da tarefa a ser deletada. |

## Rodando os testes

Para rodar os testes, rode o seguinte comando

```bash
  pytest tests.py -v
```


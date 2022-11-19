# GRPC COURSE CATEGORY

<p>Repositório feito com intuito de aprender a usar GRPC com GOLang</p>

## Ferramentas

- [GoLang](https://go.dev/)
- [Protobuff](https://grpc.io/docs/protoc-installation/)
- [Evans](https://github.com/ktr0731/evans)
- [SQLite3](https://www.sqlite.org/index.html)

## Rodar o Aplicativo

Necessário criar tabela de categories com sqlite3 rode o comando abaixo:

```
sqlite3 db.sqlite
```

Após estar dentro do Sqlite 3 Rode o comando:

```
CREATE TABLE categories(id string, name string, description string);
```

Instale as dependências do Go rodando o seguinte comando:

```
go mod tidy
```

Rode o server:

```
go run cmd/grpcServer/main.go
```

Para testar, utilize o Evans com o seguinte comando:

```
evans -r repl
```

Agora so realizar as chamadas GRPC. Chamadas Disponibilizadas:

```
call CreateCategory
call CreateCategoryStream
call CreateCategoryStreamBidirectional
call ListCategories
call GetCategory
```

## Retorno de Dados:

CategoryResponse:

```
{
    "name": "John"
    "description": "Doe",
    "id": "0e23a351-43ee-466b-b102-caa3325844e7",
}
```

CategoryListRespose

```
{
    "categories": [
        {
            "name": "John"
            "description": "Doe",
            "id": "0e23a351-43ee-466b-b102-caa3325844e7",
        }
    ]
}
```

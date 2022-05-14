## Pessoa-API (Person API)

### Tech/Frameworks:
* Spring Boot (json/restful) 
* Srping data;
* Mavem;
* MongoDB no lugar do Postgres;
* Docker (to run the database);
* JUnit;
* Postman;

Endpoints:
- Save person (POST): /pessoas/
```
{
    "nome": "Adriano Ribeiro",
    "cpf": "00000000001",
    "dtNascimento": "1982-07-10",
    "endereco": {
    	"logradouro":"Rua A, 100",
    	"bairro":"Floradas de Sao José",
    	"cidade":"Sao Jose dos Campos",
    	"uf":"SP",
    	"cep":"12230087"
    }
}
```

- Get people (GET): /pessoas/ 
- Get person (GET): /pessoas/:id
- Delete a person (Delete): /pessoas/:id

### Suggestion to run the MongoDB into docker (I was using Windows as SO). 

1. docker run --name <nome-de-seu-container> -p 27017:27017 -d mongo
2. docker exec -it <nome-de-seu-container> mongo local

### Go to applications.properties file

```
#MongoDB
spring.data.mongodb.host=<host>
spring.data.mongodb.port=<porta>
spring.data.mongodb.database=<database>
```

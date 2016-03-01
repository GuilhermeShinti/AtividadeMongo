## Exercicio 01
## - Crie um banco de com o nome: Teste e uma collection com com o nome Usuario. Faça um script que insira 10 usuários nesta collection e exiba todas elas após seu cadastro.




```
 1- use Teste 

 2- db.createCollection("Usuario")
 
 3- for (var i = 1; i <= 10; i++) {
   		db.Usuario.insert( { nome : 'novoUsuario'+i } )
	}
 
 4- db.Usuario.find()
{
  "_id": ObjectId("56d4ea5d7c8a47ffd102f00b"),
  "nome": "Leonardo"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f00c"),
  "nome": "novoUsuario1"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f00d"),
  "nome": "novoUsuario2"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f00e"),
  "nome": "novoUsuario3"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f00f"),
  "nome": "novoUsuario4"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f010"),
  "nome": "novoUsuario5"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f011"),
  "nome": "novoUsuario6"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f012"),
  "nome": "novoUsuario7"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f013"),
  "nome": "novoUsuario8"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f014"),
  "nome": "novoUsuario9"
}
{
  "_id": ObjectId("56d4eec87c8a47ffd102f015"),
  "nome": "novoUsuario10"
}

```
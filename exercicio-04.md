4 - Usando o banco do Mercado, realize as consultas a baixo:

- Mostrar total de produtos cadastrados;

```
>db.Produtos.count()
19
```

- Mostrar todos os produtos do marca Apple;

```
>db.Produtos.find({"marca":"Apple")
{ "_id" : ObjectId("56d62aee8114ac0f9e26f8b8"), "produto" : "Smartphone", "marca" : "Apple", "valor" : 2000, "quantidadeComp" : 37, "unid" : "pçs" }
{ "_id" : ObjectId("56d62aee8114ac0f9e26f8b9"), "produto" : "Tablet", "marca" : "Apple", "valor" : 3000, "quantidadeComp" : 40, "unid" : "pçs" }

>db.Produtos.find({"marca":"Apple").pretty()
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b8"),
        "produto" : "Smartphone",
        "marca" : "Apple",
        "valor" : 2000,
        "quantidadeComp" : 37,
        "unid" : "pçs"
}
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b9"),
        "produto" : "Tablet",
        "marca" : "Apple",
        "valor" : 3000,
        "quantidadeComp" : 40,
        "unid" : "pçs"
```

- Mostrar todos os produtos que custam mais de R$1.500,00;

```
> db.Produtos.find({"valor":{$gt:1500}})
{ "_id" : ObjectId("56d62aee8114ac0f9e26f8b4"), "produto" : "TV Plasma", "marca" : "LG", "valor" : 3000, "quantidadeComp" : 2, "unid" : "pçs" }
{ "_id" : ObjectId("56d62aee8114ac0f9e26f8b5"), "produto" : "Geladeira", "marca" : "Consul", "valor" : 7000, "quantidadeComp" : 3, "unid" : "pçs" }
{ "_id" : ObjectId("56d62aee8114ac0f9e26f8b8"), "produto" : "Smartphone", "marca" : "Apple", "valor" : 2000, "quantidadeComp" : 37, "unid" : "pçs" }
{ "_id" : ObjectId("56d62aee8114ac0f9e26f8b9"), "produto" : "Tablet", "marca" : "Apple", "valor" : 3000, "quantidadeComp" : 40, "unid" : "pçs" }

> db.Produtos.find({"valor":{$gt:1500}}).pretty()
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b4"),
        "produto" : "TV Plasma",
        "marca" : "LG",
        "valor" : 3000,
        "quantidadeComp" : 2,
        "unid" : "pçs"
}
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b5"),
        "produto" : "Geladeira",
        "marca" : "Consul",
        "valor" : 7000,
        "quantidadeComp" : 3,
        "unid" : "pçs"
}
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b8"),
        "produto" : "Smartphone",
        "marca" : "Apple",
        "valor" : 2000,
        "quantidadeComp" : 37,
        "unid" : "pçs"
}
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b9"),
        "produto" : "Tablet",
        "marca" : "Apple",
        "valor" : 3000,
        "quantidadeComp" : 40,
        "unid" : "pçs"
}
```

- Mostrar apenas o nome do produto, marca e valor, dos produtos que foram comprados mais de 20 unidades;

```
> db.Produtos.find({"quantidadeComp":{$gt:20}},{produto:true,marca:true,valor:true}).pretty()
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8af"),
        "produto" : "Tomate",
        "marca" : "Hortifruti",
        "valor" : 8
}
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b0"),
        "produto" : "Bala Yogurt",
        "marca" : "Dori",
        "valor" : 0.2
}
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b7"),
        "produto" : "Panelas Inox",
        "marca" : "Consul",
        "valor" : 30
}
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b8"),
        "produto" : "Smartphone",
        "marca" : "Apple",
        "valor" : 2000
}
{
        "_id" : ObjectId("56d62aee8114ac0f9e26f8b9"),
        "produto" : "Tablet",
        "marca" : "Apple",
        "valor" : 3000
}
```

- Mostrar apenas o nome dos produtos da LG que custam mais de R$2.000,00
```
> db.Produtos.find({"valor":{$gt:2000}},{produto:true})
{ "_id" : ObjectId("56d62aee8114ac0f9e26f8b4"), "produto" : "TV Plasma" }
{ "_id" : ObjectId("56d62aee8114ac0f9e26f8b5"), "produto" : "Geladeira" }
{ "_id" : ObjectId("56d62aee8114ac0f9e26f8b9"), "produto" : "Tablet" }
```

Crie um banco de com o nome: Mercado. E transfira os valores da planilha para uma collection.

```
1- >use Mercado

2- >db.createCollection("Produtos")

```

|Produto             |	Marca      |	     Valor |	Quant. Comp.|    Unid.    |
|:------------------:|:-----------:|:-----------:|:------------:|:-----------:|
|Batata Frita 100 grs|	Yoki	     |3.00	       |2	            |unid         |
|Pet 2 Lts.	         |Coca-Cola	   |4.00	       |3	            |unid         |
|Recheado Morando    |	Marilan	   |2.00	       |4	            |unid         |
|Morango	           |Hortifruti	 |2.50	       |3	            |kgs          |
|Leite Condensado	   |Batavo	     |2.50	       |3	            |unid         |
|Azeite	             |Galo	       |10.00	       |5	            |unid         |
|Tomate	             |Hortifruti	 |8.00	       |50	          |kgs          |
|Bala Yogurti	       |Dori	       |0.20	       |500	          |unid         |
|Arroz	             |Tio João	   |3.00	       |4           	|kgs          |
|Feijao	             |Tio João	   |2.00	       |3	            |kgs          |
|Ventilador	         |Arno	       |400.00       |	2	          |pçs          |
|TV de Plasma	       |LG	         |3000.00      |	2	          |pçs          |
|Geladeira	         |Consul	     |7000.00      |	3	          |pçs          |
|DVD	               |LG	         |700.00       |	8	          |pçs          |
|Panelas Inox	       |Consul	     |30.00        |	60          |	pçs         |
|Smartphone	         |Apple	       |2000.00      |	37          |	pçs         |
|Tablet	             |Apple	       |3000.00      |	40          |	pçs         |
|Smartphone	         |LG	         |1500.00      |	3	          |pçs          |
|Recheado Baunilha	 |Marilan	     |5.00         |	2	          |pçs          |

```

var json = [
	{"produto": "Batata Frita 100grs", "marca": "Yoki", "valor": 3.00, "quantidadeComp" : 2, "unid" : "unid"},
	{"produto": "Pet 2 Lts", "marca": "Coca-Cola", "valor": 4.00, "quantidadeComp" : 3, "unid" : "unid"},
	{"produto": "Recheado Morango", "marca": "Marilan", "valor": 2.00, "quantidadeComp" : 4, "unid" : "unid"},
	{"produto": "Morango", "marca": "Hortifruti", "valor": 2.50, "quantidadeComp" : 3.00, "unid" : "kgs"},
	{"produto": "Leite Condensado", "marca": "Batavo", "valor": 2.50, "quantidadeComp" : 3, "unid" : "unid"},
	{"produto": "Azeite", "marca": "Galo", "valor": 10.00, "quantidadeComp" : 5, "unid" : "unid"},
	{"produto": "Tomate", "marca": "Hortifruti", "valor": 8.00, "quantidadeComp" : 50, "unid" : "kgs"},
	{"produto": "Bala Yogurt", "marca": "Dori", "valor": 0.20, "quantidadeComp" : 500, "unid" : "unid"},
	{"produto": "Arroz", "marca": "Tio Joao", "valor": 3.00, "quantidadeComp" : 4, "unid" : "kgs"},
	{"produto": "Feijao", "marca": "Tio Joao", "valor": 2.00, "quantidadeComp" : 3, "unid" : "kgs"},
	{"produto": "Ventilador", "marca": "Arno", "valor": 400.00, "quantidadeComp" : 2, "unid" : "pçs"},
	{"produto": "TV Plasma", "marca": "LG", "valor": 3000.00, "quantidadeComp" : 2, "unid" : "pçs"},
	{"produto": "Geladeira", "marca": "Consul", "valor": 7000.00, "quantidadeComp" : 3, "unid" : "pçs"},
	{"produto": "DVD", "marca": "LG", "valor": 700.00, "quantidadeComp" : 8, "unid" : "pçs"},
	{"produto": "Panelas Inox", "marca": "Consul", "valor": 30.00, "quantidadeComp" : 60, "unid" : "pçs"},
	{"produto": "Smartphone", "marca": "Apple", "valor": 2000.00, "quantidadeComp" : 37, "unid" : "pçs"},
	{"produto": "Tablet", "marca": "Apple", "valor": 3000.00, "quantidadeComp" : 40, "unid" : "pçs"},
	{"produto": "Smartphone", "marca": "LG", "valor": 1500.00, "quantidadeComp" : 3, "unid" : "pçs"},
	{"produto": "Recheado Baunilha", "marca": "Marilan", "valor": 5.00, "quantidadeComp" : 2, "unid" : "pçs"}
]

>db.Produto.insert(json)

```

# Lab05 - Marcadores e Taxonomia em Cypher

Estrutura de pastas:

~~~
├── README.md  <- arquivo apresentando a tarefa
~~~

# Aluno
* 231551: Antonio Gabriel da Silva Fernandes

## Tarefa de Cypher sobre Marcadores e Taxonomia

## Tarefa 1

Escreva em Cypher uma consulta que retorne os marcadores da categoria `Serviços`, sem considerar as categorias subordinadas.

### Resolução
~~~cypher
MATCH (m:Marcador)-[:Pertence]->(c:Categoria {id: 'Serviços'})
RETURN m
~~~

## Tarefa 2

Escreva em Cypher uma consulta que retorne os marcadores da categoria `Serviços`, considerando as categorias subordinadas.

### Resolução
A consulta faz um `MATCH` com todos os marcadores `m` tais que há um caminho direcionado de tamanho entre 1 e 5 entre `m` e o nó da categoria `Serviços`. Dessa forma, como não há aninhamentos mais profundos que 5 categorias, todos os marcadores pertencentes a categorias subordinadas a `Serviços` são retornados.
~~~cypher
MATCH (m:Marcador)-[*1..5]->(c:Categoria {id: 'Serviços'})
RETURN m
~~~

# Aula 04 - Lista de Exercícios

## Exercícios sobre Criação de JSON

1. Crie um objeto JSON que represente um carro com as propriedades: marca, modelo, cor e ano.
2. Crie um objeto JSON que represente uma pessoa com as propriedades: nome, idade e cidade.
3. Crie um objeto JSON que represente um livro com as propriedades: título, autor e ano de publicação.
4. Crie um objeto JSON que represente um filme com as propriedades: título, diretor e ano de lançamento.
5. Crie um objeto JSON que represente um produto com as propriedades: nome, preço e categoria.
6. Crie um objeto JSON que represente um aluno com as propriedades: nome, idade e curso.
7. Crie um objeto JSON que represente uma música com as propriedades: título, artista e duração.
8. Crie um objeto JSON que represente um restaurante com as propriedades: nome, endereço e tipo de cozinha.
9. Crie um objeto JSON que represente um evento com as propriedades: nome, data e local.
10. Crie um objeto JSON que represente uma viagem com as propriedades: destino, data de partida e data de retorno.
11. Crie um objeto JSON que represente uma empresa com as propriedades: nome, endereço e número de funcionários.
12. Crie um objeto JSON que represente uma escola com as propriedades: nome, endereço e número de alunos.
13. Crie um objeto JSON que represente um hospital com as propriedades: nome, endereço e número de leitos.
14. Crie um objeto JSON que represente uma loja com as propriedades: nome, endereço e tipo de produtos vendidos.
15. Crie um objeto JSON que represente um parque com as propriedades: nome, localização e área.
16. Crie um objeto JSON que represente um hotel com as propriedades: nome, endereço e número de quartos.
17. Crie um objeto JSON que represente uma cidade com as propriedades: nome, estado e população.
18. Crie um objeto JSON que represente um país com as propriedades: nome, capital e população.
19. Crie um objeto JSON que represente uma universidade com as propriedades: nome, endereço e número de cursos.
20. Crie um objeto JSON que represente uma empresa com uma lista de clientes, onde cada cliente possui as propriedades: nome, telefone, email e endereço.

## Explicação de Comandos MongoDB

### Banco de Dados em MongoDB
No MongoDB, um banco de dados é um contêiner para coleções. Cada banco de dados possui seu próprio conjunto de arquivos no sistema de arquivos. Um único servidor MongoDB pode ter múltiplos bancos de dados.

### Collection
Uma coleção no MongoDB é análoga a uma tabela em um banco de dados relacional como MySQL. Uma coleção armazena documentos BSON (uma extensão do JSON) e não possui esquema fixo, o que significa que os documentos em uma coleção podem ter diferentes campos.

### Comandos de Inserção e Seleção

#### Inserção em MySQL
```sql
INSERT INTO veiculos (marca, modelo, cor, ano) VALUES ('Fiat', 'Uno', 'Vermelho', 2020);
```

#### Inserção em MongoDB
```javascript
db.veiculos.insertOne({ marca: 'Fiat', modelo: 'Uno', cor: 'Vermelho', ano: 2020 });
```

#### Seleção em MySQL
```sql
SELECT * FROM veiculos WHERE marca = 'Fiat';
```

#### Seleção em MongoDB
```javascript
db.veiculos.find({ marca: 'Fiat' });
```

### Exemplo Completo

#### Inserir um Veículo
```javascript
db.veiculos.insertOne({ marca: 'Fiat', modelo: 'Uno', cor: 'Vermelho', ano: 2020 });
```

#### Pesquisar Veículos da Marca Fiat
```javascript
db.veiculos.find({ marca: 'Fiat' });
```

#### Alterar o Modelo do Veículo com Marca Fiat
```javascript
db.veiculos.updateOne(
    { marca: 'Fiat' },
    { $set: { modelo: 'Punto' } }
);
```

#### Selecionar Todos os Veículos
```javascript
db.veiculos.find();
```

### Explicação dos Comandos

- `insertOne`: Insere um único documento na coleção.
- `find`: Pesquisa documentos na coleção que correspondem aos critérios especificados.
- `updateOne`: Atualiza um único documento que corresponde aos critérios especificados.
- `$set`: Operador usado para definir o valor de um campo específico.

Esses comandos básicos permitem realizar operações CRUD (Create, Read, Update, Delete) em um banco de dados MongoDB.
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
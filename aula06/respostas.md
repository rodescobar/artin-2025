## Exercícios de MongoDB

### 1. Inserir Documentos
Insira três novos veículos na coleção `veiculos` com as seguintes informações:
- Marca: Toyota, Modelo: Corolla, Cor: Preto, Ano: 2021
- Marca: Honda, Modelo: Civic, Cor: Branco, Ano: 2019
- Marca: Ford, Modelo: Focus, Cor: Azul, Ano: 2018

```javascript
db.veiculos.insertMany([
    { marca: 'Toyota', modelo: 'Corolla', cor: 'Preto', ano: 2021 },
    { marca: 'Honda', modelo: 'Civic', cor: 'Branco', ano: 2019 },
    { marca: 'Ford', modelo: 'Focus', cor: 'Azul', ano: 2018 }
]);
```

### 2. Selecionar Documentos
Selecione todos os veículos da marca `Toyota`.

```javascript
db.veiculos.find({ marca: 'Toyota' });
```

### 3. Atualizar Documentos
Atualize a cor do veículo `Honda Civic` para `Cinza`.

```javascript
db.veiculos.updateOne(
    { marca: 'Honda', modelo: 'Civic' },
    { $set: { cor: 'Cinza' } }
);
```

### 4. Excluir Documentos
Exclua todos os veículos do ano `2018`.

```javascript
db.veiculos.deleteMany({ ano: 2018 });
```

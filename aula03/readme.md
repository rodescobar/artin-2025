# Aula Inicial de NodeJS

## Criando a Primeira Aplicação

1. **Instale o Node.js**:
    - Baixe e instale o Node.js a partir do [site oficial](https://nodejs.org/).

2. **Crie um Diretório para o Projeto**:
    ```bash
    mkdir minha-primeira-aplicacao
    cd minha-primeira-aplicacao
    ```

3. **Inicialize o Projeto**:
    ```bash
    npm init -y
    ```

4. **Crie o Arquivo `index.js`**:
    ```javascript
    // index.js
    console.log("Olá, mundo! Esta é minha primeira aplicação Node.js");
    ```

5. **Execute a Aplicação**:
    ```bash
    node index.js
    ```

## Criando um Arquivo JSON com Lista de Carros Brasileiros

1. **Crie o Arquivo `carros.json`**:
    ```json
    // carros.json
    [
      {
         "marca": "Chevrolet",
         "modelo": "Onix",
         "cor": "Branco",
         "ano": 2020
      },
      {
         "marca": "Fiat",
         "modelo": "Argo",
         "cor": "Prata",
         "ano": 2019
      },
      {
         "marca": "Volkswagen",
         "modelo": "Gol",
         "cor": "Preto",
         "ano": 2018
      }
    ]
    ```

## Alterando `index.js` para Ler e Exibir o JSON

1. **Instale o Módulo `fs`**:
    ```bash
    npm install fs
    ```

2. **Atualize o Arquivo `index.js`**:
    ```javascript
    // index.js
    const fs = require('fs');

    fs.readFile('carros.json', 'utf8', (err, data) => {
      if (err) {
         console.error(err);
         return;
      }
      const carros = JSON.parse(data);
      carros.forEach(carro => {
         console.log(`Marca: ${carro.marca}, Modelo: ${carro.modelo}, Cor: ${carro.cor}, Ano: ${carro.ano}`);
      });
    });
    ```

3. **Execute a Aplicação**:
    ```bash
    node index.js
    ```

Pronto! Você criou e executou sua primeira aplicação Node.js, criou um arquivo JSON com uma lista de carros brasileiros e leu esse arquivo para exibir os valores no console.
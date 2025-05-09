# 🛍️ Projeto API

## Entrega
- Seu projeto deverá estar salvo no GIT.
- **Individual**
- Envio do link do GIT via e-mail para rodrigo.noescobar@gmail.com
- Data e hora para entrega **06/06/2025 às 19h**
    - **Entregas feitas após este horário e data serão canceladas**
- *Alunos que não entregarem o trabalho deverão fazer avaliação substitutiva*
- **A correção terá início dia 06/06/2025 às 19h**

## 🎯 Objetivo

Desenvolver uma API completa

## 🧰 Tecnologias Utilizadas

- **Linguagem**: NodeJS
- **Banco de Dados**: MongoDB

---

### Funcionalidades:
- Login e Registrar
- CRUD de:
  - Categorias
  - Produtos
  - Vendas
  - Clientes 

- Todos os itens deverão possuir a consulta por ID, nome/descricao e Todos 

### Exemplo de Rotas:
```
/api/login
/api/registrar
/api/categorias
/api/produtos
/api/vendas
/api/clientes
```

### 🖼️ Exemplo de retorno da consulta de uma venda

```json
{
  "venda": {
    "data": "2025-05-09",
    "numeroNota": "123456",
    "cliente": {
      "cpf": "123.456.789-00",
      "nome": "João da Silva",
      "endereco": {
        "rua": "Rua das Flores",
        "numero": 123,
        "bairro": "Centro",
        "cidade": "São Paulo",
        "estado": "SP",
        "cep": "01001-000"
      },
      "telefone": "(11) 98765-4321",
      "email": "joao.silva@email.com"
    },
    "produtos": [
      {
        "codigoInterno": "P001",
        "nome": "Produto A",
        "quantidade": 2,
        "valorUnitario": 50.0
      },
      {
        "codigoInterno": "P002",
        "nome": "Produto B",
        "quantidade": 1,
        "valorUnitario": 100.0
      }
    ],
    "totalVenda": 200.0
  }
}
```

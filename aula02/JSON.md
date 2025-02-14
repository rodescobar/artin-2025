# JSON (JavaScript Object Notation)

## Origem do JSON

JSON (JavaScript Object Notation) é um formato leve de intercâmbio de dados que é fácil para os humanos lerem e escreverem, e fácil para as máquinas interpretarem e gerarem. Foi criado por Douglas Crockford no início dos anos 2000 como uma alternativa mais simples ao XML.

## Estrutura do JSON

A estrutura do JSON é baseada em uma coleção de pares chave/valor. Ele é composto por dois tipos principais de estruturas:

1. **Objetos**: Uma coleção de pares chave/valor, delimitada por chaves `{}`.
2. **Arrays**: Uma lista ordenada de valores, delimitada por colchetes `[]`.
3. **Strings**: Sequências de caracteres, delimitadas por aspas duplas `""`.
4. **Números**: Valores numéricos, que podem ser inteiros ou de ponto flutuante.
5. **Booleanos**: Valores lógicos, que podem ser `true` ou `false`.
6. **Nulos**: Representado pelo valor `null`.
7. **Bytes**: JSON não possui um tipo de dado específico para bytes, mas dados binários podem ser representados como strings codificadas em Base64.

### Exemplo de Arquivo JSON Simples

```json
{
  "nome": "João",
  "idade": 30,
  "cidade": "São Paulo"
}
```

### Exemplo de Arquivo JSON Complexo

```json
{
  "nome": "Empresa XYZ",
  "funcionarios": [
    {
      "nome": "Ana",
      "idade": 28,
      "cargo": "Desenvolvedora"
    },
    {
      "nome": "Carlos",
      "idade": 35,
      "cargo": "Gerente de Projetos"
    }
  ],
  "enderecos": [
    {
      "tipo": "Matriz",
      "cidade": "Rio de Janeiro",
      "estado": "RJ"
    },
    {
      "tipo": "Filial",
      "cidade": "Belo Horizonte",
      "estado": "MG"
    }
  ]
}
```

## Exercícios

1. **Exercício 1**: Crie um arquivo JSON que represente um livro com as seguintes propriedades: título, autor, ano de publicação e gênero.

2. **Exercício 2**: Crie um arquivo JSON que represente uma lista de produtos em um supermercado. Cada produto deve ter as seguintes propriedades: nome, preço, categoria e disponibilidade.

3. **Exercício 3**: Crie um arquivo JSON que represente uma turma de alunos. Cada aluno deve ter as seguintes propriedades: nome, idade, nota e presença.

4. **Exercício 4**: Crie um arquivo JSON que represente uma empresa com múltiplos departamentos. Cada departamento deve ter um nome e uma lista de funcionários. Cada funcionário deve ter as seguintes propriedades: nome, cargo e salário.

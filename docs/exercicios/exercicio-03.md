# Exercícios: Aula 03 – Tipos Avançados 🧩

### 🟢 Nível: Básico
1.  **Union Types**: Crie uma variável que possa receber `string` ou `boolean`.
2.  **Literal Types**: Crie um tipo chamado `Alinhamento` que permita apenas os valores `"left"`, `"center"` ou `"right"`.

### 🟡 Nível: Intermediário
3.  **Intersection Types**: Crie dois tipos de objetos, `Pessoa` (com nome) e `Trabalhador` (com cargo), e crie um terceiro tipo que seja a interseção de ambos.
4.  **Narrowing com typeof**: Escreva uma função que receba `number | string` e retorne o dobro se for número ou o comprimento se for string.

### 🔴 Nível: Desafio
5.  **Validação Completa**: Crie um Type Alias para um `UsuarioAPI` que pode ter um ID numérico ou ser `null`. Use Type Guards para garantir que você só acesse propriedades do ID se ele não for nulo.
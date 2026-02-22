# Aula 02 - Tipos Fundamentais e Inferência 🛠️

---

## Recapitulando 🔄
- TypeScript adiciona tipos ao JavaScript <!-- .element: class="fragment" -->
- O compilador protege nosso código <!-- .element: class="fragment" -->
- `tsconfig.json` é a base <!-- .element: class="fragment" -->

---

## Tipos Primitivos 🧱
Os blocos básicos:
- **string**: textos <!-- .element: class="fragment" -->
- **number**: números (inteiros e decimais) <!-- .element: class="fragment" -->
- **boolean**: verdadeiro ou falso <!-- .element: class="fragment" -->

---

## Exemplo: Sintaxe de Anotação ✍️

```typescript
let nome: string = "Ricardo";
let idade: number = 30;
let vivo: boolean = true;
```

---

## O Poder da Inferência 🧠
- O TypeScript é inteligente!
- Se você atribui um valor, ele adivinha o tipo.

```typescript
let curso = "TypeScript Profissional"; 
// TS já sabe que é string!
```

---

## Quando Anotar? ⚖️
- **Inferencia**: Variáveis locais simples. <!-- .element: class="fragment" -->
- **Anotação**: Parâmetros de função, retorno de funções e objetos complexos. <!-- .element: class="fragment" -->

---

## Trabalhando com Arrays 📚
Duas formas de escrever:

```typescript
let precos: number[] = [10, 20, 30];
// OU
let precos: Array<number> = [10, 20, 30];
```

---

## Arrays Fortemente Tipados 🛡️
- O TS impede que você adicione um `string` em um array de `number`.
- Segurança total em iterações (map, filter).

---

## Tuplas: Arrays com Regras 📏
- Tamanho fixo e tipos específicos por posição.

```typescript
let produto: [number, string] = [1, "Notebook"];
```

---

## Tuplas na Prática 📦
- Ideal para coordenadas (lat, long), retornos simples de funções ou estados (como no React).

---

## Enums: Legibilidade 🏷️
- Define um conjunto de nomes para valores constantes.

```typescript
enum Status {
    Pendente,
    Aprovado,
    Cancelado
}
```

---

## Enums de String 🔠
- Valores mais claros para depuração.

```typescript
enum Tema {
    Escuro = "DARK",
    Claro = "LIGHT"
}
```

---

## O Tipo `any` (Perigo!) ⚠️
- Desativa a checagem de tipos.
- Use apenas em migrações ou casos extremos.

---

## O Tipo `unknown` (Segurança) 🛡️
- Diferente do `any`, ele não permite operações sem checagem de tipo prévia.

```typescript
let valor: unknown = 10;
// valor.toUpperCase() -> Erro!
```

---

## Estreitamento (Type Guards) 🔍
- Como "provar" ao TS o tipo de uma variável.

```typescript
if (typeof valor === "string") {
    console.log(valor.toUpperCase());
}
```

---

## Void: Sem Retorno 🚫
- Usado em funções que executam uma tarefa mas não devolvem valor.

---

## Never: O Impossível 🛑
- Funções que lançam erro ou entram em loop infinito.

---

## Null e Undefined ❓
- No modo `strict`, eles são tratados como erros se você não os prever.
- Evita erros de "null references".

---

## Resumo 🏁
- Tipos Primitivos <!-- .element: class="fragment" -->
- Arrays e Tuplas <!-- .element: class="fragment" -->
- Enums e Any/Unknown <!-- .element: class="fragment" -->

---

## Próxima Aula: Tipos Avançados!
### Vamos ver Uniões, Interseções e mais. 🚀
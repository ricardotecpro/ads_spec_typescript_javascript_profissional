# Mini-Projeto: Aula 02 – Calculadora de IMC (Tipos Primitivos) ⚖️

!!! tip "Objetivo"
    Praticar o uso de tipos primitivos (`number`, `string`), inferência de tipos e interação simples via console.

---

## 🏗️ Requisitos do Projeto
- Receber peso e altura do usuário.
- Calcular o IMC (Peso / Altura²).
- Exibir o resultado formatado com uma classificação.
- Usar tipagem explícita para as variáveis principais.

---

## 🛠️ Passo a Passo

### 1. Estrutura do Código
No seu arquivo `src/index.ts`, defina as variáveis:
```typescript
const nome: string = "Ricardo";
const peso: number = 85;
const altura: number = 1.80;

function calcularIMC(p: number, a: number): number {
    return p / (a * a);
}
```

### 2. Lógica de Classificação
Use o resultado para determinar a categoria:
```typescript
const imc = calcularIMC(peso, altura);
let classificacao: string;

if (imc < 18.5) classificacao = "Abaixo do peso";
else if (imc < 25) classificacao = "Peso normal";
else classificacao = "Sobrepeso";

console.log(`${nome}, seu IMC é ${imc.toFixed(2)} (${classificacao})`);
```

---

## ✅ Desafio Extra
- Use um `enum` para as categorias de classificação (ABAIXO, NORMAL, SOBREPESO).
- Crie uma tupla para armazenar os dados do usuário: `[string, number, number]`.
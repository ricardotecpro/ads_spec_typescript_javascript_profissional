# Mini-Projeto: Aula 03 – Gerenciador de Inventário (Tipos Avançados) 📦

!!! tip "Objetivo"
    Utilizar `Union Types`, `Type Aliases` e `Intersection Types` para modelar um sistema de inventário de produtos.

---

## 🏗️ Requisitos do Projeto
- Definir tipos para diferentes categorias de produtos (Eletrônicos, Alimentos).
- Usar intersecção para criar modelos completos.
- Implementar uma função que aceita diferentes tipos de IDs (número ou string).

---

## 🛠️ Passo a Passo

### 1. Modelagem com Type Aliases
```typescript
type Categoria = "Eletronico" | "Alimento" | "Vestuario";

type ProdutoBase = {
    id: string | number;
    nome: string;
    preco: number;
    categoria: Categoria;
};

type Especificacoes = {
    peso: number;
    dimensoes?: string;
};

// Intersection Type
type ProdutoCompleto = ProdutoBase & Especificacoes;
```

### 2. Manipulação Tipada
Crie um array de produtos e uma função para buscar por ID.
```typescript
const inventario: ProdutoCompleto[] = [
    { id: 1, nome: "Celular", preco: 2000, categoria: "Eletronico", peso: 0.2 },
    { id: "A-123", nome: "Maçã", preco: 5, categoria: "Alimento", peso: 0.1 }
];

function buscar(id: string | number) {
    return inventario.find(p => p.id === id);
}
```

---

## ✅ Desafio Extra
- Implemente um `Type Guard` para verificar se um produto é da categoria "Eletronico".
- Use `Literal Types` para definir o status do produto: `"em_estoque" | "esgotado"`.
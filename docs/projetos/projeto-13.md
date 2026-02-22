# Mini-Projeto: Aula 13 – Testando um Carrinho de Compras (Testes) 🧪

!!! tip "Objetivo"
    Implementar uma suíte de testes unitários para um sistema de carrinho de compras, utilizando Jest e TypeScript para garantir que cálculos de totais e descontos estejam corretos.

---

## 🏗️ Requisitos do Projeto
- Classe `Carrinho` com métodos: `adicionar`, `remover` e `calcularTotal`.
- Testar se o carrinho inicia vazio.
- Testar se o total é calculado corretamente após adições.
- Mockar um "Serviço de Frete" para testar o total com entrega.

---

## 🛠️ Passo a Passo

### 1. Classe a ser Testada
```typescript
export class Carrinho {
    private itens: { nome: string, preco: number }[] = [];

    adicionar(item: { nome: string, preco: number }) {
        this.itens.push(item);
    }

    getTotal(): number {
        return this.itens.reduce((acc, curr) => acc + curr.preco, 0);
    }
}
```

### 2. Arquivo de Teste (`.spec.ts`)
```typescript
import { Carrinho } from './Carrinho';

describe('Carrinho de Compras', () => {
    it('deve calcular o total corretamente', () => {
        const c = new Carrinho();
        c.adicionar({ nome: 'Livro', preco: 50 });
        c.adicionar({ nome: 'Mouse', preco: 100 });
        expect(c.getTotal()).toBe(150);
    });
});
```

---

## ✅ Desafio Extra
- Implemente um teste para verificar se o método `remover(nome)` funciona conforme o esperado.
- Adicione um teste que valide uma mensagem de erro caso tentemos adicionar um item com preço negativo.
- Configure o Jest para exibir o relatório de cobertura (`coverage`) ao rodar os testes.
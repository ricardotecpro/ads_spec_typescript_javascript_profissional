# Mini-Projeto: Aula 15 – Refatorando para Clean Code (Arquitetura) 📐

!!! tip "Objetivo"
    Transformar um código funcional, porém "sujo" (com funções gigantes e múltiplas responsabilidades), em um sistema seguindo os princípios SOLID e Clean Code.

---

## 🏗️ Requisitos do Projeto
- Dividir uma função "faz-tudo" em funções menores e específicas.
- Aplicar nomes significativos em variáveis e tipos.
- Isolar a lógica de negócio de efeitos colaterais (log, persistência).
- Garantir que cada classe tenha apenas uma responsabilidade (SRP).

---

## 🛠️ Passo a Passo

### 1. O Código Sujo (Antes)
Analise este código que calcula desconto, salva no banco e envia email de uma vez:
```typescript
async function processar(pedido: any) {
    let total = 0;
    for(let i of pedido) { total += i.preco; }
    if (total > 100) total *= 0.9;
    await db.save(pedido, total);
    await email.send("Pedido feito");
}
```

### 2. O Código Limpo (Depois)
Separe em classes e métodos:
- `OrderScanner`: Para somar os itens.
- `DiscountService`: Para aplicar regras de negócio.
- `NotificationService`: Para envio de avisos.

---

## ✅ Desafio Extra
- Aplique o Princípio da Inversão de Dependência (D do SOLID) no `NotificationService`, permitindo trocar `Email` por `WhatsApp` através de uma interface comum.
- Implemente validações robustas que lancem exceções customizadas em vez de apenas retornar `null`.
# Mini-Projeto: Aula 14 – Gateway de Pagamentos (Design Patterns) 🛡️

!!! tip "Objetivo"
    Aplicar o padrão `Strategy` e `Repository` para criar um sistema de processamento de pagamentos flexível (Cartão, Boleto, Pix) sem acoplamento.

---

## 🏗️ Requisitos do Projeto
- Interface `IPaymentStrategy`.
- Implementações para `CreditCardPayment` e `PixPayment`.
- Classe `PaymentContext` que executa a estratégia selecionada.
- Uso de `Dependency Injection` para passar a estratégia desejada.

---

## 🛠️ Passo a Passo

### 1. O Padrão Strategy
```typescript
interface IPaymentStrategy {
    process(amount: number): string;
}

class PixPayment implements IPaymentStrategy {
    process(amount: number) { return `Pix de R$${amount} gerado.`; }
}

class CardPayment implements IPaymentStrategy {
    process(amount: number) { return `Cartão de R$${amount} processado.`; }
}
```

### 2. O Contexto
```typescript
class Checkout {
    constructor(private strategy: IPaymentStrategy) {}

    finalizar(valor: number) {
        console.log(this.strategy.process(valor));
    }
}

const pedido = new Checkout(new PixPayment());
pedido.finalizar(200);
```

---

## ✅ Desafio Extra
- Implemente o padrão `Factory` para instanciar a estratégia correta baseada em uma string (ex: "PIX", "CARD").
- Crie um `Repository` (interface + implementação em memória) para salvar o histórico de pagamentos realizados.
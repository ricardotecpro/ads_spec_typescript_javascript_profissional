# Mini-Projeto: Aula 05 – Sistema Bancário (Classes e POO) 🏦

!!! tip "Objetivo"
    Aplicar os conceitos de Programação Orientada a Objetos (Classes, Modificadores de Acesso, Herança) para criar um sistema de gerenciamento de contas bancárias.

---

## 🏗️ Requisitos do Projeto
- Classe base `Conta` com atributos privados.
- Uso de `protected` para permitir herança.
- Subclasses `ContaCorrente` e `ContaPoupanca` com regras específicas.
- Implementação de getters e setters para validação de saldo.

---

## 🛠️ Passo a Passo

### 1. Classe Base
```typescript
abstract class Conta {
    constructor(
        private _titular: string,
        protected _saldo: number = 0
    ) {}

    get saldo() { return this._saldo; }

    depositar(valor: number): void {
        if (valor > 0) this._saldo += valor;
    }

    abstract sacar(valor: number): boolean;
}
```

### 2. Extensões
```typescript
class ContaCorrente extends Conta {
    sacar(valor: number): boolean {
        if (valor <= this._saldo + 100) { // Limite extra
            this._saldo -= valor;
            return true;
        }
        return false;
    }
}

class ContaPoupanca extends Conta {
    sacar(valor: number): boolean {
        if (valor <= this._saldo) {
            this._saldo -= valor;
            return true;
        }
        return false;
    }
}
```

---

## ✅ Desafio Extra
- Crie uma classe `Banco` que armazena um array de `Conta` e possui um método para listar todos os titulares e seus saldos (Polimorfismo).
- Adicione uma propriedade `readonly` chamada `numeroConta` gerada automaticamente no construtor.
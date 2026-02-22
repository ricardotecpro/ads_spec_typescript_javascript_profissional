# Mini-Projeto: Aula 08 – Dinamismo com Tipos (Advanced Manipulation) 🧪

!!! tip "Objetivo"
    Explorar propriedades dinâmicas usando `keyof`, `Mapped Types` e `Template Literals` para criar um sistema de notificações inteligente.

---

## 🏗️ Requisitos do Projeto
- Usar `keyof` para criar um sistema de acesso seguro a chaves.
- Template Literals para gerar nomes de manipuladores de eventos.
- Criar tipos que se adaptam dinamicamente a modelos de dados.

---

## 🛠️ Passo a Passo

### 1. Acesso Dinâmico Seguro
```typescript
function getProp<T, K extends keyof T>(obj: T, key: K): T[K] {
    return obj[key];
}

const config = { porta: 3000, host: "localhost" };
const p = getProp(config, "porta"); // OK e Tipado!
```

### 2. Sistema de Eventos Literais
```typescript
type Eventos = "focus" | "blur" | "click";
type EventHandlers = {
    [K in Eventos as `on${Capitalize<K>}`]: () => void;
};

const handlers: EventHandlers = {
    onFocus: () => console.log("Focado"),
    onBlur: () => {},
    onClick: () => {}
};
```

---

## ✅ Desafio Extra
- Crie um `Mapped Type` que transforme todas as propriedades de um objeto em funções que retornam aquele tipo (Getters).
- Use `Conditional Types` para criar um utilitário que remova a propriedade "id" de qualquer tipo de objeto passado.
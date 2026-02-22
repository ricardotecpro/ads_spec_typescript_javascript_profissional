# Aula 11 – TypeScript com Frontend Moderno ⚛️

!!! tip "Objetivo"
    Nesta aula, aprenderemos como o TypeScript potencializa o desenvolvimento frontend, focando em React. Veremos como tipar componentes, props, hooks e o estado global da aplicação de forma profissional.

---

## 1. Por que TypeScript no Frontend? 🌐

Aplicações frontend lidam com muitas interações de usuário e dados dinâmicos. O TS ajuda a:
- Garantir que as **Props** passadas para um componente estão corretas.
- Evitar erros ao acessar o **Estado** (State).
- Facilitar o uso de **Context API** e bibliotecas de gerenciamento de estado.

---

## 2. Componentes e Props Tipados 🧩

Em React com TS, definimos uma interface para as props do componente.

```tsx
interface BotaoProps {
    texto: string;
    cor?: "primary" | "secondary";
    onClick: () => void;
}

const Botao = ({ texto, cor = "primary", onClick }: BotaoProps) => {
    return (
        <button className={cor} onClick={onClick}>
            {texto}
        </button>
    );
};
```

---

## 3. Hooks Tipados (useState / useRef) 🎣

O TS geralmente infere o tipo do `useState`, mas às vezes precisamos ser explícitos, especialmente com arrays ou objetos.

```tsx
import { useState, useRef } from 'react';

// Inferência automática
const [contagem, setContagem] = useState(0); 

// Explícito (Union Type)
const [usuario, setUsuario] = useState<Usuario | null>(null);

// Tipagem de Referências (DOM)
const inputRef = useRef<HTMLInputElement>(null);
```

---

## 4. Context API Tipada 🌍

Compartilhar estado global com segurança de tipos é um dos maiores benefícios do TS no React.

```tsx
interface ThemeContextType {
    tema: "light" | "dark";
    toggleTema: () => void;
}

const ThemeContext = createContext<ThemeContextType | undefined>(undefined);
```

---

## 5. Visualizando a Hierarquia de Componentes (Mermaid)

```mermaid
graph TD;
    App[App.tsx] --> Header[Header.tsx];
    App --> Main[MainContent.tsx];
    Main --> Card[Card.tsx (Generic)];
    Main --> List[List.tsx (Generic)];
    style Card fill:#f9f,stroke:#333
    style List fill:#f9f,stroke:#333
```

---

## 6. Exercícios Práticos 📝

1. **Básico**: Crie um componente `Saudacao` que receba uma prop `nome: string` e exiba na tela.
2. **Básico**: Crie um estado usando `useState` para armazenar uma lista de strings e exiba-os em uma lista `<ul>`.
3. **Intermediário**: Crie um componente de `Input` reutilizável que aceite todas as props padrão de um input HTML (use `React.InputHTMLAttributes`).
4. **Intermediário**: Implemente um hook customizado `useLocalStorage<T>` que seja genérico.
5. **Desafio**: Crie um componente `Tabela<T>` genérico que receba uma lista de dados de tipo `T` e uma configuração de colunas para renderizá-los.

---

## 🚀 Mini-Projeto da Aula
Desenvolva um **Dashboard de Tarefas (Todo List)**.
- Componentes para: `Header`, `AddTodoForm`, `TodoList` e `TodoItem`.
- Interfaces bem definidas para a entidade `Todo` (`id`, `titulo`, `concluida`).
- Use `useState` para gerenciar a lista e garanta que todas as funções de manipulação (adicionar, remover, alternar status) estejam devidamente tipadas.

---
**Próxima Aula**: Vamos aprender a conectar nossas aplicações ao mundo externo em [Integração com APIs e Tipagem de Dados Externos](./aula-12.md)!
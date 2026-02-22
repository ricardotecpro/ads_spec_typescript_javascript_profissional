# Mini-Projeto: Aula 09 – Biblioteca Modular (Organização de Projeto) 📁

!!! tip "Objetivo"
    Organizar um sistema de gerenciamento de livros em uma estrutura modular profissional, utilizando `ES Modules`, `Barrel Files` e `Path Aliases`.

---

## 🏗️ Requisitos do Projeto
- Dividir o código em pastas: `models`, `services` e `app`.
- Usar `index.ts` para centralizar as exportações de cada pasta.
- Configurar e usar um path alias `@core` para o diretório de modelos.

---

## 🛠️ Passo a Passo

### 1. Estrutura de Pastas
Crie a seguinte hierarquia:
```text
src/
  ├── models/
  │    ├── Livro.ts
  │    └── index.ts
  ├── services/
  │    ├── Biblioteca.ts
  │    └── index.ts
  └── index.ts
```

### 2. Barrel File em `models`
No arquivo `src/models/index.ts`:
```typescript
export * from './Livro';
```

### 3. Configurando o Alias no `tsconfig.json`
```json
"compilerOptions": {
  "baseUrl": ".",
  "paths": {
    "@core/*": ["src/models/*"]
  }
}
```

---

## ✅ Verificação Final
- Importe o modelo `Livro` em `Biblioteca.ts` usando o alias: `import { Livro } from '@core';`.
- Certifique-se de que o arquivo principal (`src/index.ts`) importa apenas do serviço e executa uma lógica de teste (ex: adicionar um livro e listar).
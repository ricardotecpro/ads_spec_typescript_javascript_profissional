# Exercícios: Aula 01 – Introdução ao TypeScript e Setup Profissional 🧠

### 🟢 Nível: Básico
1.  **Instalação Local**: Inicialize um projeto Node.js (`npm init -y`) e instale o TypeScript como dependência de desenvolvimento.
2.  **Configuração Inicial**: Gere o arquivo `tsconfig.json` e altere a propriedade `outDir` para "./dist" e `rootDir` para "./src".

### 🟡 Nível: Intermediário
3.  **Compilação Manual**: Crie um arquivo `src/app.ts`, adicione um `console.log` e execute o comando `npx tsc` para gerar o arquivo na pasta `dist`.
4.  **Watch Mode**: Configure o compilador para monitorar alterações automaticamente (`watch mode`) e valide se o arquivo JS é atualizado ao salvar o TS.

### 🔴 Nível: Desafio
5.  **Automação com NPM**: No seu `package.json`, crie dois scripts: `build` (para compilar uma única vez) e `dev` (para rodar o compilador em modo watch). Teste ambos os comandos via terminal.
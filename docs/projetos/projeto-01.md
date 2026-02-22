# Mini-Projeto: Aula 01 – Setup do Workspace Profissional 🛠️

!!! tip "Objetivo"
    Configurar um ambiente de desenvolvimento TypeScript completo, pronto para produção, seguindo as melhores práticas de organização de pastas e automação de scripts.

---

## 🏗️ Requisitos do Projeto
- Inicializar um projeto Node.js.
- Configurar o TypeScript com `tsconfig.json`.
- Organizar a estrutura de pastas (`src` e `dist`).
- Automatizar o processo de build e execução.

---

## 🛠️ Passo a Passo

### 1. Inicialização
Abra o terminal na pasta do projeto e execute:
<div class="termy" data-termynal>
  <span data-ty="input">npm init -y</span>
  <span data-ty="input">npm install -D typescript ts-node-dev</span>
</div>

### 2. Configuração do TS
Gere o arquivo de configuração e ajuste as seguintes propriedades:
<div class="termy" data-termynal>
  <span data-ty="input">npx tsc --init</span>
</div>

**Configurações recomendadas no `tsconfig.json`**:
```json
{
  "compilerOptions": {
    "target": "ES2020",
    "module": "NodeNext",
    "rootDir": "./src",
    "outDir": "./dist",
    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true,
    "forceConsistentCasingInFileNames": true
  }
}
```

### 3. Scripts de Automação
No arquivo `package.json`, adicione:
```json
"scripts": {
  "dev": "ts-node-dev --respawn --transpile-only src/index.ts",
  "build": "tsc",
  "start": "node dist/index.js"
}
```

### 4. Código de Teste
Crie a pasta `src/` e o arquivo `index.ts`:
```typescript
const mensagem: string = "Ambiente TypeScript configurado com sucesso! 🚀";
console.log(mensagem);
```

---

## ✅ Verificação Final
1. Execute `npm run dev` e verifique se o log aparece no terminal.
2. Altere o texto da mensagem e veja se o servidor reinicia sozinho.
3. Execute `npm run build` e verifique se a pasta `dist/` foi criada com o arquivo `.js`.
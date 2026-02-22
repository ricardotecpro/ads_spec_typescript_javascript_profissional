# Quiz: Aula 01 – Introdução ao TypeScript e Setup Profissional 🧠

1. O que é o TypeScript em relação ao JavaScript?
   - [ ] Uma nova linguagem que substitui o JavaScript.
   - [x] Um superset (superconjunto) que adiciona tipagem estática ao JavaScript.
   - [ ] Um framework para desenvolvimento web.
   - [ ] Um interpretador de código backend.
   > Explicação: O TypeScript é um superset, o que significa que todo código JS é TS válido, mas o TS adiciona funcionalidades extras como tipagem.

2. Qual é o principal benefício da tipagem estática?
   - [ ] Fazer o código rodar mais rápido.
   - [ ] Reduzir o tamanho do arquivo final.
   - [x] Detectar erros durante o desenvolvimento (tempo de compilação).
   - [ ] Permitir o uso de emojis no código.
   > Explicação: A tipagem estática permite que o compilador identifique erros de lógica e de tipos antes mesmo do código ser executado.

3. Qual comando é usado para instalar o TypeScript globalmente via NPM?
   - [ ] `npm get typescript`
   - [x] `npm install -g typescript`
   - [ ] `npm start typescript`
   - [ ] `npx install ts`
   > Explicação: O parâmetro `-g` (global) permite que o comando `tsc` fique disponível em qualquer lugar do sistema.

4. O que faz o comando `tsc --init`?
   - [ ] Inicia um novo servidor Node.js.
   - [ ] Compila todos os arquivos .ts da pasta.
   - [x] Cria um arquivo de configuração `tsconfig.json`.
   - [ ] Instala as dependências do projeto.
   > Explicação: O `tsconfig.json` é o arquivo central que define as regras do compilador TypeScript no projeto.

5. O que acontece com os tipos do TypeScript após a compilação?
   - [ ] Eles são mantidos no arquivo .js gerado.
   - [x] Eles são removidos (type erasure) e o resultado é JavaScript puro.
   - [ ] Eles são convertidos em comentários JSDoc.
   - [ ] Eles são ignorados pelo navegador.
   > Explicação: O navegador não entende TypeScript, por isso o compilador remove as anotações de tipo durante a transpilação para JS.

6. No `tsconfig.json`, o que a opção `"strict": true` faz?
   - [ ] Deixa o código mais curto.
   - [x] Ativa uma série de verificações rigorosas de tipo.
   - [ ] Permite o uso de qualquer tipo (any) livremente.
   - [ ] Ignora erros de variáveis não utilizadas.
   > Explicação: O modo strict é recomendado para garantir a máxima segurança e as melhores práticas da linguagem.

7. Qual é a extensão padrão de arquivos TypeScript?
   - [ ] .js
   - [x] .ts
   - [ ] .tsx
   - [ ] .typescript
   > Explicação: Arquivos TypeScript usam `.ts`. Para arquivos com React (JSX), usamos `.tsx`.

8. O que é o "DefinitelyTyped" (@types)?
   - [ ] Uma ferramenta de build.
   - [x] Um repositório de definições de tipos para bibliotecas JavaScript puras.
   - [ ] Um plugin do VS Code.
   - [ ] Uma versão alternativa do TypeScript.
   > Explicação: Como muitas bibliotecas não são escritas em TS, o community fornece tipos via pacotes `@types/nome-da-lib`.

9. Onde o arquivo compilado é geralmente colocado se configurarmos `outDir`?
   - [ ] Na mesma pasta do código fonte.
   - [ ] Na pasta `node_modules`.
   - [x] Na pasta especificada (ex: `dist/` ou `build/`).
   - [ ] Ele é enviado diretamente para a nuvem.
   > Explicação: O `outDir` define o diretório de saída para os arquivos JavaScript gerados pelo `tsc`.

10. Qual ferramenta é essencial para um setup profissional de TS para rodar o código em desenvolvimento sem gerar arquivos físicos?
    - [ ] Webpack
    - [x] ts-node ou ts-node-dev
    - [ ] Babel
    - [ ] Excel
    > Explicação: `ts-node` permite executar arquivos TS diretamente na memória, facilitando muito o ciclo de desenvolvimento.
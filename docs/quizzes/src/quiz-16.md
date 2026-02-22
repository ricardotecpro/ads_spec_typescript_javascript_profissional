# Quiz: Aula 16 – Projeto Final e Deploy 🚀

1. O que acontece durante a etapa de "Build" de um projeto TypeScript?
   - [ ] O código TS é enviado para o GitHub.
   - [x] O código TS é transpilado para JS puro para poder ser executado pelo Node ou Navegador.
   - [ ] O computador apaga todos os erros de tipo.
   - [ ] O código é traduzido para inglês.
   > Explicação: O ambiente de produção (seja servidor ou browser) não entende o TypeScript nativamente.

2. O que faz o comando `tsc --noEmit`?
   - [ ] Apaga o projeto.
   - [x] Apenas verifica os erros de tipo sem gerar arquivos JavaScript de saída.
   - [ ] Compila o código muito rápido.
   - [ ] Instala uma nova versão do TS.
   > Explicação: Comumente usado em CI/CD para validar se o código está correto antes de tentar o deploy.

3. Por que não devemos commitar a pasta `dist/` ou `node_modules/` no Git?
   - [ ] Porque elas têm vírus.
   - [x] Porque são arquivos gerados automaticamente; o Git deve conter apenas o seu código fonte original.
   - [ ] Porque o GitHub proíbe essas pastas.
   - [ ] Porque as pastas são muito pesadas.
   > Explicação: Outros desenvolvedores e servidores podem gerar esses arquivos a partir do seu código fonte e do `package.json`.

4. Para que serve o arquivo `.gitignore`?
   - [ ] Para ignorar as ordens do chefe.
   - [x] Para listar pastas e arquivos que o Git deve desconsiderar (como pastas de build e segredos).
   - [ ] Para apagar arquivos permanentemente.
   - [ ] Para mudar o nome dos arquivos.
   > Explicação: Essencial para manter o repositório limpo e seguro.

5. O que o Docker resolve no processo de Deploy?
   - [ ] Aumenta a velocidade da internet do servidor.
   - [x] Garante que a aplicação rode exatamente na mesma versão de Node e SO, evitando o problema "na minha máquina funciona".
   - [ ] Deixa o código TS mais rápido.
   - [ ] Cria backups da internet.
   > Explicação: Conteinerização padroniza o ambiente de execução em qualquer nuvem.

6. Em uma arquitetura profissional, onde o Frontend deve ser hospedado?
   - [ ] No mesmo servidor que o Banco de Dados.
   - [x] Em serviços de "Static Hosting" (Vercel, Netlify, S3) para maior performance.
   - [ ] No computador local do desenvolvedor.
   - [ ] Dentro de um arquivo PDF.
   > Explicação: Frontends modernos (React, Vue, etc) são apenas arquivos estáticos após o build.

7. O que é uma "Variável de Ambiente"?
   - [ ] Uma variável que muda conforme a temperatura.
   - [x] Configurações que mudam dependendo de onde o app está rodando (ex: porta do servidor, senha do banco).
   - [ ] Uma variável global no TypeScript.
   - [ ] Uma regra de reciclagem.
   > Explicação: Permitem que o mesmo código funcione em "Desenvolvimento", "Staging" e "Produção".

8. Qual o script padrão para iniciar a aplicação em produção no `package.json`?
   - [ ] `npm dev`
   - [x] `npm start` (geralmente executando `node dist/index.js`).
   - [ ] `npm compile`
   - [ ] `npm deploy`
   > Explicação: O script de start deve rodar o código compilado, não o TS original.

9. O "Continuous Deployment" (CD) serve para:
   - [ ] Deixar o desenvolvedor cansado.
   - [x] Automatizar o envio do código para produção assim que ele é aprovado no repositório.
   - [ ] Fazer backups das pastas.
   - [ ] Compilar apenas uma vez por semana.
   > Explicação: Agiliza o ciclo de vida do software e reduz o erro humano no processo de deploy manual.

10. Qual a importância de testar o build localmente antes de fazer o deploy?
    - [ ] Nenhuma, a nuvem resolve tudo.
    - [x] Para garantir que não existam erros de importação ou arquivos faltando que só aparecem após a transpilação.
    - [ ] Para ocupar o tempo livre.
    - [ ] Para esquentar o computador.
    > Explicação: O comportamento do código em desenvolvimento (`ts-node`) pode ser sutilmente diferente do código compilado (`dist`).
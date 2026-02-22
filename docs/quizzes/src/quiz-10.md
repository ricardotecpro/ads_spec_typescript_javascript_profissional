# Quiz: Aula 10 – TypeScript com Node.js (Backend) 🟢

1. Qual pacote é necessário para usar o Express com TypeScript?
   - [ ] express-ts
   - [ ] typescript-express
   - [x] @types/express (além do próprio express)
   - [ ] express-types
   > Explicação: O pacote `@types` fornece as definições de tipo que não vêm nativamente na biblioteca JS do Express.

2. O que o `ts-node-dev` faz de diferente do `tsc`?
   - [ ] Ele cria arquivos .js físicos.
   - [x] Ele roda o código TS diretamente na memória e reinicia o servidor em cada alteração (hot reload).
   - [ ] Ele apenas checa erros sem rodar o código.
   - [ ] Ele publica o site na nuvem.
   > Explicação: É a ferramenta padrão de produtividade para desenvolvimento backend com TS.

3. Como você tipa os argumentos `req` e `res` do Express?
   - [ ] req: any, res: any
   - [x] import { Request, Response } from 'express'
   - [ ] use express.types
   - [ ] O TS faz isso sozinho sem imports.
   > Explicação: Importar as interfaces `Request` e `Response` garante que você tenha autocompletar e validação nos métodos HTTP.

4. O que é um "DTO" (Data Transfer Object)?
   - [ ] Um motor de banco de dados.
   - [x] Um objeto que define precisamente o formato dos dados trafegados entre camadas (ex: da requisição para o serviço).
   - [ ] Uma forma de criptografar o banco de dados.
   - [ ] Um comando do terminal.
   > Explicação: DTOs evitam o uso de `any` no backend e garantem que o contrato da API seja respeitado.

5. Qual a importância de tipar o `req.body`?
   - [ ] Para o código ficar mais bonito.
   - [x] Para garantir que as propriedades esperadas existam antes de tentarmos usá-las, evitando erros de runtime.
   - [ ] Não é possível tipar o req.body.
   - [ ] Para aumentar o uso de memória.
   > Explicação: Sem tipagem, o `body` é tratado como `any`, o que anula os benefícios do TypeScript.

6. O que é um `Middleware` no Express?
   - [ ] Um hardware de rede.
   - [x] Uma função que tem acesso aos objetos `req` e `res` e pode interromper ou modificar o fluxo da requisição.
   - [ ] Uma base de dados leve.
   - [ ] Um tipo de loop infinito.
   > Explicação: Middlewares são usados para logs, autenticação, tratamento de erros e muito mais.

7. Como tipar um middleware customizado?
   - [ ] Usando o tipo string.
   - [x] Usando o tipo `NextFunction` além de `Request` e `Response`.
   - [ ] Não se tipa middlewares.
   - [ ] Usando a interface `Middleware`.
   > Explicação: O `NextFunction` é essencial para passar o controle para a próxima função na pilha do Express.

8. Onde os arquivos compilados de um projeto Node/TS devem ficar em produção?
   - [ ] Na pasta `src`
   - [x] Na pasta `dist` (ou similar definida no `outDir`).
   - [ ] No Desktop do servidor.
   - [ ] Não precisam ser compilados em produção.
   > Explicação: Em produção, rodamos o JavaScript puro por questões de performance e compatibilidade do ambiente Node.

9. Para que serve o arquivo `.env` em um projeto backend?
   - [ ] Para salvar o código fonte.
   - [x] Para guardar variáveis de ambiente e segredos (como senhas de banco) fora do código.
   - [ ] Para configurar o tema do editor.
   - [ ] Para listar os arquivos do projeto.
   > Explicação: Usar variáveis de ambiente é fundamental para a segurança e configuração dinâmica do app.

10. Qual a vantagem de usar TypeScript no backend (Node.js)?
    - [ ] Nenhuma, JS é melhor.
    - [x] Maior segurança em manipulação de dados, melhores ferramentas de refatoração e documentação automática através de tipos.
    - [ ] O Node.js roda TypeScript nativamente sem ferramentas.
    - [ ] Permite que o servidor use menos RAM.
    > Explicação: O TS reduz drasticamente os erros comuns de "propriedade não encontrada" em aplicações backend complexas.
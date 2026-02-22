# Quiz: Aula 09 – Módulos e Organização Profissional 📁

1. Qual a palavra-chave para disponibilizar uma função em outro arquivo?
   - [ ] provide
   - [ ] share
   - [x] export
   - [ ] public
   > Explicação: No sistema de módulos ES, `export` torna o código visível para fora do arquivo atual.

2. Como importo apenas uma função específica de um módulo?
   - [ ] `import modulo.funcao`
   - [x] `import { funcao } from './modulo'`
   - [ ] `require('./modulo').funcao`
   - [ ] `use funcao from modulo`
   > Explicação: A desestruturação no import permite carregar apenas o necessário, economizando recursos.

3. O que é um `export default`?
   - [ ] Um erro de exportação.
   - [x] Define a exportação principal do arquivo, que pode ser importada sem chaves `{}`.
   - [ ] Uma forma de exportar tudo do arquivo de uma vez.
   - [ ] Uma exportação que só funciona no servidor.
   > Explicação: Cada arquivo pode ter apenas um export default.

4. Para que serve um "Barrel File" (`index.ts`)?
   - [ ] Para guardar segredos do projeto.
   - [x] Para concentrar exportações de uma pasta e simplificar os pacotes de imports.
   - [ ] Para acelerar a internet do desenvolvedor.
   - [ ] Para apagar arquivos não utilizados.
   > Explicação: Permite que outros arquivos importem de uma pasta (`import { a, b } from './modulo'`) em vez de arquivos específicos.

5. O que os "Path Aliases" resolvem?
   - [ ] Erros de sintaxe no código.
   - [x] Evitam caminhos relativos longos e confusos como `../../../`.
   - [ ] Mudam o nome das variáveis automaticamente.
   - [ ] Permitem o uso de caminhos absolutos do Windows.
   > Explicação: Ao configurar aliases como `@models`, o código fica muito mais legível e fácil de mover.

6. Onde configuramos os Path Aliases?
   - [ ] No package.json
   - [x] No tsconfig.json, dentro de `compilerOptions.paths`.
   - [ ] No arquivo de índice do projeto.
   - [ ] No VS Code diretamente.
   > Explicação: O compilador TS precisa saber como resolver esses apelidos durante o build.

7. Posso usar `Namespace` e `ES Modules` no mesmo projeto?
   - [ ] Não, o TS proíbe.
   - [x] Sim, mas recomenda-se focar em ES Modules para projetos modernos.
   - [ ] Sim, mas Namespaces só funcionam em arquivos .js.
   - [ ] Apenas se o projeto for pequeno.
   > Explicação: ES Modules são o padrão da indústria e melhor suportados por bundlers modernos como Webpack e Vite.

8. Qual a função do `baseUrl` no tsconfig?
   - [ ] Define o endereço do site na nuvem.
   - [x] Define a pasta raiz de onde o compilador deve começar a procurar os módulos.
   - [ ] Muda a cor da base do terminal.
   - [ ] Não existe essa propriedade.
   > Explicação: `baseUrl` é necessário para que os path aliases funcionem corretamente.

9. O que acontece se eu esquecer o `export` em uma classe dentro de um módulo?
   - [ ] Ela fica pública por padrão.
   - [x] Ela fica privada (local) àquele arquivo e não pode ser importada.
   - [ ] O compilador gera um erro fatal.
   - [ ] O TS adiciona o export sozinho.
   > Explicação: No sistema de módulos, o isolamento é o comportamento padrão para segurança.

10. Como reorganizar um projeto conforme ele cresce?
    - [ ] Colocar tudo em um arquivo gigante para não perder nada.
    - [x] Dividir em pastas por responsabilidade (models, services, utils, controllers).
    - [ ] Mudar para JavaScript puro.
    - [ ] Criar uma pasta diferente para cada variável.
    > Explicação: A organização em camadas e diretórios semânticos é a chave para a escalabilidade de qualquer software.
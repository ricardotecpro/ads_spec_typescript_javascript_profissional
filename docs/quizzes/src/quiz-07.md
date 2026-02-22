# Quiz: Aula 07 – Utility Types e Manipulação de Tipos ⚙️

1. O que faz o utilitário `Partial<T>`?
   - [ ] Deleta metade das propriedades.
   - [x] Torna todas as propriedades do tipo T opcionais (inclui `?`).
   - [ ] Torna as propriedades apenas de leitura.
   - [ ] Cria um erro se faltarem propriedades.
   > Explicação: Essencial para funções de "update" onde nem todos os campos são enviados.

2. Qual utilitário é o oposto exato do `Partial`?
   - [ ] All<T>
   - [ ] Complete<T>
   - [x] Required<T>
   - [ ] Final<T>
   > Explicação: `Required` garante que todas as propriedades sejam obrigatórias, mesmo as que eram opcionais no original.

3. Para que serve o `Readonly<T>`?
   - [ ] Para ler arquivos do HD.
   - [x] Para impedir que qualquer propriedade do objeto seja alterada após a criação.
   - [ ] Para ocultar as propriedades no log do console.
   - [ ] Para transformar objetos em strings.
   > Explicação: Ajuda a manter a imutabilidade dos dados dentro da aplicação.

4. Se eu quiser um tipo com APENAS duas propriedades de uma interface com dez, qual uso?
   - [ ] Omit<T, K>
   - [x] Pick<T, K>
   - [ ] Choose<T, K>
   - [ ] Filter<T, K>
   > Explicação: `Pick` permite "pegar" seletivamente o que importa para um novo tipo.

5. E se eu quiser todas as propriedades EXCETO uma?
   - [ ] Ignore<T, K>
   - [ ] Remove<T, K>
   - [x] Omit<T, K>
   - [ ] Delete<T, K>
   > Explicação: `Omit` é ideal para remover campos sensíveis (como senhas) de um tipo antes de enviá-lo.

6. O que o `Record<K, T>` faz?
   - [ ] Grava um áudio do código.
   - [x] Cria um tipo de objeto com chaves específicas e valores de um tipo específico.
   - [ ] Salva os dados no banco de dados automaticamente.
   - [ ] Cria um log de todas as variáveis.
   > Explicação: Frequentemente usado para mapas, dicionários ou tabelas de lookup.

7. Posso aninhar Utility Types? Ex: `ReadOnly<Partial<Usuario>>`.
   - [ ] Não, gera erro de compilação.
   - [x] Sim, você pode combiná-los para criar tipos complexos.
   - [ ] Sim, mas apenas dois de cada vez.
   - [ ] Sim, mas apenas no VS Code Insiders.
   > Explicação: A composição de utilitários é uma técnica poderosa para manipulação de modelos.

8. Utility Types geram código no JavaScript final?
   - [ ] Sim, funções utilitárias são adicionadas.
   - [x] Não, eles servem apenas para checagem estática no TypeScript;
   - [ ] Sim, mas apenas o Record.
   - [ ] Sim, se usarmos o modo strict.
   > Explicação: Eles são abstrações de tipo puro.

9. Qual utilitário extrai o tipo de retorno de uma função?
   - [ ] Return<T>
   - [x] ReturnType<T>
   - [ ] GetReturn<T>
   - [ ] FuncResult<T>
   > Explicação: Útil quando queremos saber o que uma biblioteca de terceiros retorna.

10. Mapped Types são a base para os Utility Types. O que eles fazem?
    - [ ] Mapeiam a localização dos arquivos no disco.
    - [x] Permitem criar novos tipos transformando as propriedades de tipos existentes através de iteração.
    - [ ] Desenham diagramas das classes.
    - [ ] São um tipo de array.
    > Explicação: É a "mágica" por trás de como o TS consegue transformar todas as chaves em opcionais ou em apenas leitura.
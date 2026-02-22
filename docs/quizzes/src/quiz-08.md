# Quiz: Aula 08 – Manipulação Avançada de Tipos 🧪

1. O que o operador `keyof` faz?
   - [ ] Obtém todos os valores de um objeto.
   - [x] Gera uma união de strings contendo todas as chaves de um tipo de objeto.
   - [ ] Abre as chaves de um projeto no VS Code.
   - [ ] Deleta as chaves de um tipo.
   > Explicação: `keyof` é fundamental para criar funções genéricas que manipulam propriedades de objetos de forma segura.

2. Qual a sintaxe para "Indexed Access Types"?
   - [ ] `Tipo.propriedade`
   - [x] `Tipo["propriedade"]`
   - [ ] `Tipo<propriedade>`
   - [ ] `Tipo[0]`
   > Explicação: Permite que você "olhe" para dentro de outro tipo e extraia o tipo de uma propriedade específica.

3. Como funciona um "Conditional Type"?
   - [ ] Usando um bloco `if/else` no TypeScript.
   - [x] Usando uma sintaxe de ternário: `T extends U ? X : Y`.
   - [ ] Usando um `switch` de tipos.
   - [ ] Não existem tipos condicionais no TS.
   > Explicação: Permite criar lógicas de decisão complexas em nível de tipo.

4. Para que serve a palavra-chave `infer`?
   - [ ] Para inferir o valor de uma variável.
   - [x] Para capturar e extrair um tipo de dentro de outra estrutura (como o retorno de uma função) em tipos condicionais.
   - [ ] Para sugerir um novo nome para uma função.
   - [ ] Para forçar o compilador a ignorar um erro.
   > Explicação: `infer` é usado exclusivamente dentro da cláusula `extends` de um tipo condicional.

5. O que são "Template Literal Types"?
   - [ ] Apenas strings comuns.
   - [x] Tipos de string construídos a partir de outros tipos usando a sintaxe de crases (` `` `).
   - [ ] Templates HTML para o frontend.
   - [ ] Comentários dinâmicos no código.
   > Explicação: Permitem gerar uniões de strings baseadas em combinações de outros tipos literais.

6. Qual o resultado de `keyof { a: 1, b: 2 }`?
   - [ ] `number`
   - [ ] `1 | 2`
   - [x] `"a" | "b"`
   - [ ] `{ a, b }`
   > Explicação: Ele extrai os nomes das propriedades como tipos literais de string.

7. Se eu tenho `type Pessoa = { nome: string }`, o que é `Pessoa["nome"]`?
   - [ ] `"nome"`
   - [x] `string`
   - [ ] `object`
   - [ ] `any`
   > Explicação: O acesso indexado retorna o **tipo** associado àquela chave.

8. Onde os tipos condicionais são mais úteis?
   - [ ] Em scripts pequenos de aprendizado.
   - [x] No desenvolvimento de bibliotecas e frameworks que precisam ser altamente flexíveis.
   - [ ] Em arquivos CSS.
   - [ ] Para mudar a cor do terminal.
   > Explicação: Eles permitem que os tipos se adaptem dinamicamente às entradas, fornecendo APIs muito inteligentes.

9. `T extends any[] ? T[number] : T`. O que esse tipo faz?
   - [ ] Converte T em um array.
   - [x] Se T for um array, retorna o tipo de seus itens; se não, retorna T.
   - [ ] Conta quantos itens o array T possui.
   - [ ] Gera um erro se T não for array.
   > Explicação: É um padrão comum para "desembrulhar" arrays em seus tipos base.

10. Pode-se usar Template Literals para criar nomes de eventos como `on-click` | `on-change`?
    - [ ] Não, strings de tipos são estáticas.
    - [x] Sim, combinando um prefixo `"on-"` com uma união de ações.
    - [ ] Sim, mas apenas no backend.
    - [ ] Sim, mas apenas se a ação for uma string única.
    > Explicação: A combinação de uniões em template literals cria o produto cartesiano de todas as possibilidades.
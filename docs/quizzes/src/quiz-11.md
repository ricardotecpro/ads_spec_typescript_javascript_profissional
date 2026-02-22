# Quiz: Aula 11 – TypeScript com Frontend Moderno ⚛️

1. Qual o principal benefício de usar React com TypeScript?
   - [ ] Os sites carregam mais rápido.
   - [x] Garantia de que as Props passadas para os componentes estão corretas.
   - [ ] Não precisa mais usar CSS.
   - [ ] O React remove o TypeScript automaticamente.
   > Explicação: O TS no React foca na segurança da comunicação entre componentes através das Props.

2. Como definimos as props de um componente funcional?
   - [ ] Usando um array.
   - [x] Definindo uma interface ou type e passando como tipo ao componente.
   - [ ] Não se define tipos para props.
   - [ ] No arquivo index.html.
   > Explicação: Ao tipar as props, o editor avisa se você esquecer um campo obrigatório ou passar um tipo errado.

3. Qual a sintaxe correta para um estado numérico com `useState` explícito?
   - [ ] `useState(number)(0)`
   - [x] `useState<number>(0)`
   - [ ] `useState[number](0)`
   - [ ] `useState.number(0)`
   > Explicação: O uso de `<number>` (Generics) define o tipo de dado que aquele estado pode carregar.

4. O TS consegue inferir o tipo de um estado se eu fizer `useState("Olá")`?
   - [ ] Não, é sempre obrigatório ser explícito.
   - [x] Sim, ele infere que o estado é do tipo `string`.
   - [ ] Sim, mas apenas se estiver no modo estrito.
   - [ ] Ele infere como `any`.
   > Explicação: O TypeScript usa o valor inicial para deduzir o tipo, facilitando a escrita do código.

5. Para que serve o `React.FC` ou `React.FunctionComponent`?
   - [ ] Para criar classes em React.
   - [x] É um tipo auxiliar para definir componentes funcionais (aunque hoje em dia o uso simples de interfaces é mais comum).
   - [ ] Para conectar com o banco de dados.
   - [ ] Para definir o estado global.
   > Explicação: Ele fornece tipagem automática para propriedades como `children`, embora muitos desenvolvedores prefiram tipar manualmente hoje em dia.

6. Como tipar o evento de mudança de um input (`onChange`)?
   - [ ] e: any
   - [ ] e: Event
   - [x] e: React.ChangeEvent<HTMLInputElement>
   - [ ] e: string
   > Explicação: O React usa um sistema de eventos próprios (Synthetic Events) que precisam ser mapeados corretamente para ter acesso ao `e.target.value`.

7. O que acontece se você passar uma prop não definida na interface do componente?
   - [ ] O React ignora e o código roda.
   - [x] O TypeScript gera um erro de compilação informando que a prop não existe.
   - [ ] O componente não renderiza.
   - [ ] O navegador trava.
   > Explicação: Essa é a "mágica" do TS: prevenir o uso de propriedades inexistentes antes mesmo de salvar o arquivo.

8. Como tipar uma referência de um elemento DOM com `useRef`?
   - [ ] `useRef<Element>(null)`
   - [x] `useRef<HTMLInputElement>(null)` (substituindo pelo elemento correto).
   - [ ] `useRef(any)`
   - [ ] Referências não podem ser tipadas.
   > Explicação: Tipar corretamente o elemento permite que você use propriedades específicas do DOM (como `.focus()` ou `.value`) com segurança.

9. No Context API, o que passamos como Generic no `createContext`?
   - [ ] O nome do contexto.
   - [x] O formato (interface) dos dados que o contexto irá carregar.
   - [ ] O componente principal.
   - [ ] Nada.
   > Explicação: Isso garante que qualquer componente que consuma o contexto saiba exatamente quais dados estão disponíveis lá dentro.

10. Componentes Genéricos em React servem para quê?
    - [ ] Deixar o design genérico.
    - [x] Criar componentes abstratos (como Tabelas ou Listas) que funcionam com qualquer tipo de dado fornecido.
    - [ ] Criar componentes sem estilo.
    - [ ] Não existem componentes genéricos.
    > Explicação: Permite máxima reutilização de UI para diferentes tipos de dados de negócio.
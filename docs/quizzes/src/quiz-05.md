# Quiz: Aula 05 – Classes e Programação Orientada a Objetos 🏛️

1. Qual o modificador de acesso padrão no TypeScript (se nada for escrito)?
   - [ ] private
   - [ ] protected
   - [x] public
   - [ ] readonly
   > Explicação: Por padrão, todo membro de uma classe é público, permitindo acesso de qualquer lugar.

2. O que acontece com membros marcados como `private`?
   - [ ] Eles podem ser acessados por subclasses.
   - [x] Eles só podem ser acessados de dentro da própria classe.
   - [ ] Eles aparecem com erro no JavaScript compilado.
   - [ ] Eles são removidos pelo compilador.
   > Explicação: O encapsulamento privado protege dados internos de modificações acidentais externas.

3. Para que serve o modificador `protected`?
   - [ ] Protege o arquivo contra leitura.
   - [x] Permite o acesso dentro da própria classe e por suas subclasses (herança).
   - [ ] É o mesmo que o modificador private.
   - [ ] Torna a classe imutável.
   > Explicação: `protected` é ideal para permitir extensibilidade sem expor dados para o mundo externo.

4. Qual a vantagem da "Shorthand Syntax" no construtor?
   - [ ] Fazer o código rodar em navegadores antigos.
   - [x] Declarar e inicializar atributos da classe em uma única linha.
   - [ ] Impedir a criação de objetos.
   - [ ] Aumentar o número de linhas de código.
   > Explicação: Facilita a escrita de classes concisas e limpas.

5. O que os métodos `get` e `set` permitem fazer?
   - [ ] Baixar dados da internet.
   - [x] Interceptar e validar a leitura ou escrita em propriedades privadas.
   - [ ] Criar backups da classe.
   - [ ] Apenas mudar o nome das variáveis.
   > Explicação: Getters e setters são a base do encapsulamento moderno, permitindo lógica personalizada.

6. Como uma classe herda de outra no TypeScript?
   - [ ] implements
   - [x] extends
   - [ ] inherits
   - [ ] using
   > Explicação: Assim como no JS moderno (ES6+), usamos `extends` para herança de classes.

7. O que é uma "Classe Abstrata"?
   - [ ] Uma classe que só tem teoria.
   - [x] Uma classe que serve de base, mas não pode ser instanciada diretamente.
   - [ ] Uma classe sem métodos.
   - [ ] Uma classe criada automaticamente pelo compilador.
   > Explicação: Classes abstratas definem comportamentos comuns que devem ser implementados pelas subclasses.

8. Qual o comando usado para chamar o construtor da classe pai (base)?
   - [ ] parent()
   - [ ] this.base()
   - [x] super()
   - [ ] constructor.call()
   > Explicação: O `super()` deve ser a primeira chamada no construtor de uma classe que estende outra.

9. Propriedades `readonly` em classes podem ser alteradas onde?
   - [ ] Em qualquer lugar.
   - [x] Apenas no momento da declaração ou dentro do construtor.
   - [ ] Apenas em métodos estáticos.
   - [ ] Nunca, nem no construtor.
   > Explicação: Após a inicialização no construtor, um campo `readonly` torna-se imutável.

10. O que significa "Polimorfismo" na prática?
    - [ ] Mudar a forma física do servidor.
    - [x] Classes diferentes executando o mesmo método de formas diferentes.
    - [ ] Criar muitos tipos com o mesmo nome.
    - [ ] Ocultar propriedades private.
    > Explicação: Permite tratar objetos de subclasses diferentes como se fossem da classe base, mas executando cada um sua lógica própria.
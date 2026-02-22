# Quiz: Aula 12 – Integração com APIs e Tipagem de Dados Externos 📡

1. Por que não podemos confiar 100% nos tipos do TS ao receber dados de uma API?
   - [ ] Porque as APIs são proibidas de usar TS.
   - [x] Porque o TS não existe em tempo de execução; se a API mudar o formato dos dados, o TS não saberá.
   - [ ] Porque os dados da internet são criptografados.
   - [ ] Porque preferimos usar `any`.
   > Explicação: O TypeScript é uma ferramenta de desenvolvimento e compilação, mas não valida dados reais durante a execução do programa.

2. Qual a forma correta de tipar uma resposta do Axios?
   - [ ] `axios.get(url, { type: Usuario })`
   - [x] `axios.get<Usuario>(url)`
   - [ ] `axios.get(url) as Usuario`
   - [ ] O Axios não aceita tipagem.
   > Explicação: O uso de Generics no método `.get<T>` do Axios informa ao TS qual o formato esperado para o campo `.data`.

3. Para que serve o padrão "DTO" (Data Transfer Object) na integração?
   - [ ] Para salvar dados no disco.
   - [x] Para transformar e limpar os dados que vêm da API antes de usá-los na aplicação.
   - [ ] Para criptografar a resposta.
   - [ ] Para diminuir a velocidade da internet.
   > Explicação: DTOs permitem que sua aplicação dependa de modelos limpos, independentemente de como a API envia os dados originais.

4. O que é o "Zod"?
   - [ ] Um editor de texto.
   - [x] Uma biblioteca de declaração e validação de esquemas em tempo de execução (runtime).
   - [ ] Um plugin do Chrome.
   - [ ] Um novo tipo de servidor.
   > Explicação: O Zod garante que os dados externos realmente sigam o contrato definido enquanto o app está rodando.

5. O que faz o comando `z.infer<typeof schema>`?
   - [ ] Deleta o schema.
   - [x] Extrai automaticamente um tipo (Type) do TypeScript a partir de um schema do Zod.
   - [ ] Executa a validação.
   - [ ] Cria uma interface no Java.
   > Explicação: Evita a duplicidade de ter que escrever a interface manualmente e o schema de validação; um gera o outro.

6. O que acontece se o Zod validar dados que estão em formato errado?
   - [ ] Ele converte os dados à força.
   - [x] Ele lança um erro detalhado (ou retorna um status de falha) descrevendo o que está errado.
   - [ ] Ele ignora e segue o fluxo.
   - [ ] Ele apaga a variável.
   > Explicação: Isso permite tratar erros de API de forma robusta e amigável para o usuário.

7. Por que devemos evitar o uso de `as` ao receber dados de uma API?
   - [ ] Porque deixa o código mais longo.
   - [x] Porque o `as` apenas "silencia" o compilador sem garantir que o dado é real, podendo causar erros depois.
   - [ ] Porque o `as` é exclusivo para números.
   - [ ] Porque o `as` foi removido do TS 5.0.
   > Explicação: O uso de assertions (`as`) pode esconder bugs graves se a API mudar.

8. Qual o benefício de lidar com erros de API usando `axios.isAxiosError()`?
   - [ ] Para fechar o programa.
   - [x] Permite que o TS conheça as propriedades específicas de erro do Axios (como `response.data`).
   - [ ] Faz a requisição ser reexecutada.
   - [ ] Nenhuma vantagem técnica.
   > Explicação: É um "Type Guard" específico para erros de rede.

9. O que significa uma API ser "Self-Documenting" através de tipos no TS?
   - [ ] Ela fala com você.
   - [x] Quando você tem as interfaces, o código diz exatamente o que enviar e o que esperar receber.
   - [ ] A API cria seu próprio site de documentação.
   - [ ] Não existe esse conceito.
   > Explicação: Tipos atuam como documentação viva que nunca fica desatualizada em relação ao código.

10. Durante o desenvolvimento, o que o "Network Tab" do navegador ajuda na integração?
    - [ ] A mudar o tema do Chrome.
    - [x] A inspecionar os dados reais (JSON) que estão chegando para criar suas interfaces fielmente.
    - [ ] A editar o código TS diretamente.
    - [ ] A aumentar a velocidade do Wi-Fi.
    > Explicação: Ver o JSON real que a API envia é o primeiro passo para criar os tipos corretos no TypeScript.
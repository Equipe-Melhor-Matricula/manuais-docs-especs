BDD (Behavior-Driven Development) é uma abordagem de desenvolvimento de software que visa melhorar a colaboração entre desenvolvedores, testadores e partes interessadas no projeto, como gerentes de produto e analistas. O objetivo principal do BDD é criar um entendimento compartilhado dos requisitos do sistema, baseando-se em um formato simples e compreensível para todos os envolvidos, sem recorrer a jargões técnicos complexos.

**Principais Características do BDD:**

1. **Especificação baseada no comportamento:**
   Em vez de focar em testes unitários tradicionais, que testam componentes isolados do sistema, o BDD enfoca o comportamento do sistema de forma mais ampla, alinhada aos requisitos de negócio.

2. **Histórias de usuário e exemplos concretos:**
   O BDD utiliza histórias de usuário para capturar requisitos e exemplos para ilustrar o comportamento desejado. Essas histórias são escritas de forma simples e geralmente seguem a estrutura:
   - **Cenário** (onde se passa)
   - **Dado que** (contexto inicial)
   - **Quando** (ação realizada)
   - **Então** (resultado esperado)

   Exemplo de uma história de usuário escrita em BDD:
```plaintext
Cenário: Tela do carrinho de compras.                       (cenário possível)
  Dado um usuário autenticado,                              (contexto)
    E 3 pepinos a R$ 5,00 cada no carrinho de compras,      (contexto)
  Quando ele escolhe a opção de efetuar a compra,           (ação)
  Então o sistema redireciona para a página de pagamento,   (resultado)
    E o valor total é de R$ 15,00.                          (resultado)
```

3. **Linguagem ubíqua:**
   BDD adota uma linguagem simples e acessível, chamada de "linguagem ubíqua", que todos os membros da equipe podem entender e usar para descrever funcionalidades, sem a necessidade de se aprofundar em detalhes técnicos.

4. **Testes automatizados:**
   As histórias de usuário são transformadas em testes automatizados. Ferramentas como Cucumber, SpecFlow ou Behave permitem escrever testes em linguagem natural, que depois são vinculados a código, garantindo que o comportamento descrito na história de usuário seja validado automaticamente durante o desenvolvimento.

**Exemplo de um fluxo típico em BDD:**
1. A equipe define um comportamento esperado do sistema, que é descrito de forma simples (Gherkin).
2. O comportamento é validado através de testes automatizados.
3. O código é escrito para satisfazer as expectativas definidas na história de usuário.
4. O código é refatorado, se necessário, para melhorar a clareza e manter a funcionalidade desejada.

**Vantagens do BDD:**
- **Melhor comunicação**: A utilização de uma linguagem comum entre todas as partes envolvidas melhora a compreensão mútua.
- **Testes mais legíveis e colaborativos**: O foco em exemplos concretos facilita a revisão e adaptação do software durante o desenvolvimento.
- **Documentação viva**: Os testes em BDD servem como uma documentação que está sempre atualizada com o comportamento esperado do sistema.

**Ferramentas populares:**
- **Cucumber** (Java, Ruby, etc.)
- **SpecFlow** (para .NET)
- **Behat** (PHP)
- **JBehave** (Java)

**Nosso caso de uso:**
 - [Cypress](https://www.cypress.io/) + [Cypress Cucumber Preprocessor](https://www.npmjs.com/package/cypress-cucumber-preprocessor)
 - Escrevendo os casos BDD em linguagem natural português br e usando essas duas ferramentas, poderemos automatizar os testes de validação na interface.


A principal diferença entre BDD e TDD (Test-Driven Development) é que no BDD o foco está no comportamento do sistema, enquanto no TDD o foco está nos testes do código. Além disso, o BDD usa uma linguagem natural para descrever o comportamento do sistema, enquanto o TDD é mais técnico e focado em testes de mais baixo nível. 

Referências:

https://medium.com/revista-tspi/gherkin-o-dia-em-que-entendi-que-estava-escrevendo-errado-220a84520819

https://renatogroffe.medium.com/asp-net-core-specflow-implementando-testes-a-partir-de-uma-user-story-8a60f6335d70

https://docbehat.readthedocs.io/pt/v3.1/guides/1.gherkin.html

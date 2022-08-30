# BDD
O que é BDD (o Behaviour Driven Development)
- BDD tenta melhorar a comunicação e colaboração.
- BDD tenta aproximar o negócio e criar um entendimento melhor como a aplicação deveria funcionar.
   Existem vários tipos e níveis de testes, como por exemplo:

       - testes de unidade
       - testes de integração
       - testes ponta a ponta (end-to-end)

# Cucumber
não fornece nenhuma ferramenta para efetivamente verificar condições.

Para isso devemos utilizar o Junit que traz inúmeros métodos interessantes de verificação, a partir da classe org.junit.Assert

Essa classe fornece métodos estáticos muito simples que verificam se o parâmetro é verdadeiro, se há igualdade etc, como por exemplo:

Assert.assertEquals(Object expected, Object actual);

Para saber mais sobre essa função você pode conferir a documentação oficial:

https://junit.org/junit4/javadoc/4.8/org/junit/Assert.html

e a documentação do Cucumber:

https://cucumber.io/docs/cucumber/checking-assertions/



### Como integrar a biblioteca Cucumber na aplicação

    Cucumber pode ser inicializado a partir do junit4 (@RunWith)
    os arquivos .feature são analisados pelo Gherkin e Cucumber
        - Gerkin é uma linguagem para definir os .feature
        - Cucumber gera e roda os passos (steps) associados ao .feature
    dentro do .feature escrevemos a funcionalidade e os critérios de aceitação
    um critério de aceitação segue a estrutura de um teste (passos ou steps)
        os passos são Given-When-Then ou Dado-Quando-Entao
    cada passo será implementado por um método anotado (step).

    
        um arquivo .feature pode ter vários cenários e passos (steps)
    os métodos associado aos passos são reaproveitados entre cenários
        podemos passar parâmetros do cenário ao método
    Cucumber possui anotações para inicializar (@Before) e finalizar (@After) o cenários
        - os métodos anotados com @Before e @After são chamados de Hooks
        cuidado, pois os Hooks não são visíveis no arquivo .feature
        
        Usados Exemplos para alimentar o mesmo teste com dados diferentes
	Usado DataTables para passar vários dados ao teste de uma vez só



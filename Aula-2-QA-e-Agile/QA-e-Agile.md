# Anotações

## Quais as características de um Tester Ágil?
A principal diferença entre um tester ágil e um tradicional está na participação distribuída x centralizada, o tester ágil faz presença em toda a cadeia de desenvolvimento do software, buscando alinhar as expectativas com o resto do time e prevenindo bugs antes mesmo deles ocorrerem, em contraste com o tester tradicional que atua apenas fase final do desenvolvimento do software, testando e relatando os bugs/erros somente depois de boa parte do desenvolvimento. Outra característica está na distribuição de responsabilidade, enquanto no modelo tradicional a qualidade de software é 100% de responsabilidade do tester, no modelo ágil espera-se que o time inteiro coopere com o fator de qualidade durante todo o processo de desenvolvimento, sendo o tester ágil o principal instigador da qualidade, mas não 100% responsável pela qualidade do software. Além disso, o tester ágil busca automatizar testes e manter o desenvolvimento alinhado com as expectativas do cliente.


## Em quais momentos o Tester Ágil aparece no desenvolvimento de um software?
Em toda a cadeia de desenvolvimento do software, no modelo ágil, o teste e os alinhamentos para garantir a qualidade do software acontecem de forma recorrente e não linear, diferente de um processo tradicional onde o teste e analise de qualidade ocorre apenas depois do desenvolvimento.  

## Quando um code review faz sentido e quando ele deixa de fazer sentido?

### Quando faz sentido:
1. A implementação tem impacto potencialmente crítico para a aplicação.
Quando a feature/alteração/melhoria que será implementada pode quebrar processos importantes ou é direcionada para setores sensíveis como área fiscal e financeira, o code review é uma boa camada adicional de verificação e validação da implementação.

2. Aprendizado de Juniors/Aprendizado no geral
O code review pode ser valioso em equipes com juniors ou integrantes que buscam aprender, proporcionando feedbacks com profissionais mais experientes.  

3. Quando uma feature tem implementação muito específica.
Caso o código do proprietário tenha algum elemento desconhecido pelo resto da equipe ou implementa de uma forma necessária que só ele entende, o code review é interessante para alinhar o resto da equipe.

### Quando não faz sentido:
1. É uma mudança trivial
Cor de botão, texto com erro de linguagem e etc.

2. Quando o responsável pelo review não tem ideia do contexto da implementação
Pode acabar gerando um feedback falso negativo/falso positivo para bugs ou implementações.

3. Código temporário
Quando o código da implementação é temporário, atuando mais como um "bandage" da situação, talvez não seja tão interessante um code review dedicado.

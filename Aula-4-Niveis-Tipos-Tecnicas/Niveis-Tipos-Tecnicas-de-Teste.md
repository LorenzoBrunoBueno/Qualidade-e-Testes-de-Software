# Anotações

## Níveis de Teste

### Pirâmide de Testes
Representação comparativa visual da incidênca, impacto e velocidade dos diferentes níveis de testes. 

### Teste de Componente/Unitário
Realizado em componentes que permitem testes isoladamente de outros componentes/setores do sistema. Buscam bugs de forma localizada e geralmente envolvem erros de lógica. Um exemplo seria qualquer função de cálculo do sistema, que não requisita dado de algum outro serviço, podendo ser testada de forma isolada. São os testes mais rápido, numerosos  e geralmente exigem menos custo de retrabalho segundo a pirâmide de testes.

### Teste de Integração
Realizado na interação entre mais de um componentes distintos. Buscam bugs provenientes da conexão e comunicação entre dois ou mais componentes/serviços. O exemplo mais comum seria a interação de um serviço com um banco de dados, como em um cadastro de usuário, requisição de dados ou login. Se encontra no meio da pirâmide de testes, com métricas moderadas em quantidade, velocidade e custo de retrabalho para os problemas encontrados.

### Teste de Sistema/End to End
Realizado no sistema por completo, focando em fluxos reais de utilização dentro do aplicativo. Como exemplo, enquanto no teste de integração testariamos o cadastro de usuário começando do envio da requisição pelo serviço de usuário, passando pelo cadastro do banco e terminando na resposta do banco de dados ao serviço, no Teste de Sistema testariamos tudo isso, além do usuário efetuando login, acessando e utilizando outros serviços pela home até que o fluxo de utilização da aplicação acabasse. Encontram retrabalhos mais custosos, são mais lentos e aparecem em menos quantidade que o teste de integração. 

### Teste de Aceite
Realizado para validar se o sistema atende os requisitos requisitados pelo cliente, padronizações/exigências de outros orgãos ou o que é esperado pelo usuário final. Como exemplo, teste feito de ponta a ponta em conjunto com um advogado ou uma autoridade jurídica para validar a conformidade do sistema com alguma lei ou requisito contratual. Em relação a pirâmide de testes, apresentam características parecidas com o teste de sistema, mas menos recorrentes.

## Tipos de Teste

### Teste Funcional
Teste para avaliar funções que o sistema deveria ter com base eu seus requisitos, por exemplo, no desenvolvimento de um sistema de delivery com o requisito de uma função para cálculo de vendas diárias de produtos, essa função precisa ser testada e a sua funcionalidade precisa estar alinhada com as especificações no requisito.

### Teste não funcional
Teste também baseado em requisitos do sistema, mas nesse caso os não funcionais que mantém características como desempenho, disponibilidade ou segurança. Como exemplo, uma loja digital de jogos com fluxo grande de usuários com o seguinte requisito não funcional: "O sistema deve funcionar sem perdas significativas de desempenho com até 10.000 usuários simultâneos", o teste não funcional precisa validar esse requisito não funcional.

### Teste de Caixa-Branca
Os testes devem surgir da lógica diretamente implementada no código, quase que linha por linha, onde para aplicá-los é obrigatório o conhecimento do código. Por exemplo, caso exista a presença de um if no código, essa seção do código deve ser testada para ambos os resultados, caso seja verdadeiro ou falso.

### Teste de Caixa-Preta
Teste puramente baseado na entrada e na expectativa da saída, sem nenhum contado com o código-fonte da função testada. Por exemplo, ao testar uma função que realiza um cálculo específico, o testador conhece apenas as informações que entram para a operação e o resultado que a operação deve retornar, mas comoa operação faz isso ele não tem ideia.

### Teste Relacionado à Mudança
Teste realizado juntamente à mudança, por exemplo, foi solicitada uma correção em uma das funções da aplicação, logo após a implementação dessa correção o teste relacionado à mudança já é aplicado, verificando se a correção está conforme o solicitado.

## Técnicas de Teste

### Técnicas de Teste Caixa-Preta
1. Particionamento de equivalência:
Em um sistema que necessita de uma entrada de dados específica, o testador cria grupos com dados que seguem algum padrão que será testado, e depois testa os dados do mesmo grupo buscando verificar se o sistema reage a todos os integrantes do grupo da mesma forma. Exemplo, o sistema espera uma string para senha com pelo menos 6 caracteres e um caractere especial, ao testar os grupos senha maior que 6 digitos, senha menor que 6 digitos, senha com caractere especial são criados, depois os dados exemplos inseridos em cada grupo são testados no sistema, buscando verificar se a resposta para cada um deles é igual no mesmo grupo.
2. Análise de valor limite: 
Em uma entrada de dado que possui limites de mínimos e máximos bem definidos, nessa técnica os valores mais aos extremos (limite e próximo do limite) seriam os testados. Por exemplo, em um sistema uma string de nome precisa ser de no mínimo 3 caracteres e no máximo 50 caracteres, nesse cenário o teste seria aplicado com strings de tamanhos: 3, 2, 49 e 50. 
3. Teste de tabela de decisão:
Nessa técnica, em um sistema com uma regra de comportamento bem definido com base em um comportamento ou padrão, o testador criaria uma tabela com diferentes combinações que atendem ou não o critério, de diferentes formas, com o resultado esperado, depois essa combinações seriam testadas e os resultados no sistema seriam comparados com os esperados na tabela. Por exemplo, para soliciar o saldo de um motorista em um sistema de transporte, é necessário que o CTe da carga esteja com status "Feito" e os canhotos de entrega devem estar anexados na carga, nesse caso o testador criaria uma tabela com as possíveis combinações e testaria para depois comparar o resultado esperado (se é possível solicitar o saldo ou não) com o obtido.
4. Teste de transição de estado:
Essa técnica é utilizada quando a aplicação possui alteração de estados de algum item/registro a partir de um pontos de alteração desse estado bem definidos, exemplo, em um sistema que precisa analisar quanto um carro em alta velocidade percorrendo uma linha reta desalinha para os lados, com o objetivo de identificar problemas de alinhamento. Nesse caso, o valor de referência seria o 0° = Alinhado, sendo > 0° desalinhado para a direita e < 0° desalinhado para a esquerda, nessa situação o tester precisaria verificar se o status apresentado obedece essa regra.
5. Teste de caso de uso:
Nessa técnica, o testador criaria diferentes casos de teste para testar uma função, tanto com fluxos adequados e não adequados, verificando como a aplicação responde para cada caso. Um clássico exemplo seria uma função Cadastrar de um CRUD básico, onde o tester escreveria casos de teste como esses: Cadastrar usuário com campos corretos, cadastrar usuário sem nome, cadastrar usuário com senha menor que 6 caracteres, e verificaria se o sistema responde da forma esperada.

### Técnicas de Teste Caixa-Branca
1. Teste e cobertura de instruções
Garantir que todas as linhas do código sejam testadas e ao menos uma vez nos testes. Em um teste unitário com 1000 linhas, todas as linhas do componente seriam testadas.
2. Teste de decisão e cobertura
Testes baseados em estrutura de decisão lógica, garantindo que todos os IF, Else, Switch e seus casos e etc sejam testados ao menos uma vez. Em um teste unitário com 50 estruturas de decisão lógica, todas seriam testadas.
3. O valor da instrução e teste de decisão
Além de todas as decisões lógicas, o tester precisa testar cada resultado possível dentro do da estrutura de decisão, caso dentro do if tenham 20 retornos diferentes possíveis, todos devem ser testados.

### Técnicas de Teste baseadas na experiência
1. Suposição de erro
Testes projetados com base em experiências parecidas anteriores do tester, no mesmo sistema ou pela colaboração em outros projetos. Por exemplo, um tester Senior que já trabalhou em vários sistemas, escreve testes de erros que sempre se deparou com em seus anos de experiência.
2. Teste exploratório
O testador realiza os testes sem planejar nada em específico, apenas pensando na hora em um fluxo que pode causar um bugs, baseando-se pela própria intuição e experiências passadas. Por exemplo, um tester Senior que está testando pela primeira vez um sistema e realiza testes por conta própria, pensando em uma validação específica que pode não ter sido implementada, como um campo inserido em um formato muito específico ou SQL Injection.
3. Teste baseado em lista de verificação
O testador segue uma lista de verificações existente, por exemplo, uma lista de verificações que existe em uma empresa, montada a partir do conhecimento adquirido com projetos anteriores.  


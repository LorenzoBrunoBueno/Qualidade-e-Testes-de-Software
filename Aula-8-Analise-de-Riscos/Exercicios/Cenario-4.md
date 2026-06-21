# Cenário 4
##  Falha em Processo de Backup de Dado
### Uma falha no processo de backup de dados resulta na perda de uma quantidade significativa de dados dos usuários

* Probabilidade
B
* Impacto
5
* Matriz de Risco
B5 - Alto
* Testes Utilizados
Teste Funcional, Teste de Regressão, Teste Automaziado E2E
* Estratégia de Mitigação
Realizar verificação no backup de dados em cada ação importante no banco de dados. Realizar múltiplos backups de dados, distribuídos em diversas máquinas. 
* Tipos de Risco
Negócio
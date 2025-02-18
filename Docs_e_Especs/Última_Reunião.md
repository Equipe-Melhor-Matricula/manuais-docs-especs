## Primeira Sprint
Todo mundo vai aprender a usar suas stacks e se ajudar com isso.

### Lucas
+ Fique de modelar o algoritmo de otimização e apresentar a modelagem pra equipe (e colocar no Jira, presumo)
+ Se possível, também montar o servidor com ambiente dev. Mas são duas coisas diferentes e grandes, não prometi fazer ambos na mesma semana.
+ Prometi organizar a nossa primeira sprinto no Jira, bem como o épico do trabalho de treino com as tecnologias.
+ E também preparar os repositórios para essa etapa de aprendizado.
+ Além de preparar o CI/CD pelo Github.

### Desenvolvimento Dirigido por Comportamento

Do inglês, BDD (Behavior Driven Development).  
É uma forma de organizar o fluxo de desenvolvimento de software, derivado do TDD (Test-Driven Development), porém de forma a abstrair questões de programação nas definições dos comportamentos esperados do software, deixando detalhes de implementação para outra parte do trabalho.

1. Primeiro vem a ideação do problema e da proposta de solução.
2. Definição formal do problema.
3. Definição formal da solução e por que ela é melhor que a forma como se lida com esse problema atualmente.
4. Proposta de um MVP.
5. Definição dos comportamentos esperados por esse MVP.
6. Criação de testes para validar os comportamentos.
7. Desenvolvimento das funcionalidades a passarem nos testes.
8. Após funcionalidades passarem nos testes automatizados, QA faz os últimos testes, de validação manual dos fluxos.

Quando, após uma reunião, for constatado a necessidade de atualizar os testes, serão abertas as issues com devidas informações sobre isso para o QA trabalhar nelas.

Quando surgir a necessidade de se atualizar os testes durante a semana:

1. A pessoa que viu a necessidade de atualizar os testes vai no canal do Whatsapp e dá um ping no Victor e no Lucas, e inclui o Antônio se a atualização for afetar o backend e o Micael se for afetar o front.
2. Os envolvidos se juntam pra conversar sobre a atualização, escopo, implicações, etc.
3. Lucas cria a issue sobre essa atualização, e o resto da equipe é notificada sobre a atualização.
4. Victor inicia a issue e implementa a atualização.
5. Após terminada a atualização, Victor notifica a equipe que a versão atualizada dos testes está pronta para ser usada no repo QA-Design.
6. Todos dão pull em QA-Design para ter os testes atualizados em mãos.

Incluir isso de forma explícita no guia interno e notificar a todos sobre a atualização do guia interno.

Backend cuida do banco de dados.

Microserviço do algoritmo de otimização não interage com o BD. Ele recebe tudo que precisa do backend no payload, processa de forma assíncrona, e manda notificação com o resultado do processamento em payload para o backend ao terminar de rodar o alg.otim.

Entregar o resumo da sprint ao Ranilson ao final de cada semana, na forma de um relatório do que foi feito. Se necessário, alguém da equipe vai até ele reportar presencialmente. Não ficar cobrando coisa do professor. Tomar a frente, montar relatório incluindo links pro Jira e Github, e entregar ao professor toda semana.
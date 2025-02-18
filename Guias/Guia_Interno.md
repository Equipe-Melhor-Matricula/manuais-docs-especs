Manual de funcionamento interno da equipe Melhor Matrícula

## Comunicação e Reuniões

Usar mensagens na issue Daily no Jira todos os dias de trabalho, segundo o cronograma de cada um, informando como foram as atividades do dia.
> **Iasmin, Filipe** : Sábado e Domingo, qualquer horário.
> **Lucas**: Segunda à Sexta, qualquer horário.
> **Resto da Equipe** : Segunda a Sexta, até as 19h (eu preciso revisar as mensagens de todos de 19h para até as 20h fazer ajustes necessários quando surgirem dificuldades)

Reuniões online semanais às sextas de 18h para fazermos retrospectiva da semana e planejamento da semana seguinte.

As reuniões devem ter pauta e ata. A pauta técnica sobre o andamento do projeto fica a cargo do Lucas, para organização do scrum e das sprints do projeto. Toda a equipe pode trazer pautas que julgue pertinente para as reuniões, inclusive dificuldades enfrentadas, problemas iminentes e divergências internas.

O ideal é que as pautas sejam compartilhadas via doc no drive da equipe para todos terem a oportunidade de ler a pauta antes da reunião, a fim de clareza e de encurtar as reuniões de sexta.

Antônio grava as reuniões e usa as gravações para transcrever as falas com IA, monta ata da reunião, e sobre o vídeo pro YouTube, a transcrição das falas e a ata para nosso drive.

## Organização Interna

* **Gestão, CI/CD, Infra, Algoritmo:** Lucas
* **Design, QA, Testes:** Victor
* **Frontend:** Micael (PR rev), Thiago
* **Backend:** Antônio (PR rev), Iasmin, Filipe

Lucas monta a sprint da semana seguinte com base no que for definido na reunião de sexta, e monta tudo no Jira após a reunião. As issues de Iasmin e Filipe serão adicionadas primeiro, pois eles definiram que vão trabalhar no projeto aos fins de semana, enquanto o resto da equipe trabalhará no projeto de segunda a sexta.

**Drive da equipe:** Temos uma pasta compartilhada no drive institucional para documentarmos e compartilharmos todos os arquivos, planilhas e afins pertinentes ao projeto. A exceção são os vídeos das reuniões, que serão subidos ao YouTube e seus links listados na planilha de atas.

**Documentações:** Se é código vai pro Github. Se é rota de API vai pro Postman. Se é tarefa a ser feita ou problema a ser resolvido, vira issue no Jira. Se é vídeo, vai pro YouTube sem ser listado. Se é documentação de algo, vai pro drive e será linkado no Jira.

**Repositórios:** Direito de leitura de todos os repositórios para todos os integrantes da equipe. Direito de escrita de cada time no seu repositório.

**Testes e Documentação:** Os arquivos do Postman pertencem ao repositório de QA, sua devida documentação e manter atualizados é de responsabilidade do Victor. Sempre que algo precisar ser atualizado (ou algo novo surgir), o Vitor deve ser invocado para escrever e documentar os testes e rotas, e notificar todos os times da equipe sobre a atualização no Postman. Rodar o Postman antes de qualquer push ou PR.

## Issues e Fluxo de Trabalho

**Issues:** Para cada issue a ser resolvida, deve ser feito um ramo novo partindo do ramo dev. Esse ramo novo teve ser prefixado com a tag/etiqueta da respectiva issue do Jira. Ex: "MM-123 feature-cadastro-de-dependente" para uma issue de criar o fluxo de cadastro de dependentes que tem no Jira a tag ou etiqueta "MM-123". Os commits devem ter o mesmo prefixo na mensagem de commit.

O Jira oferece a funcionalidade de conectar a issue do Github com a issue no Jira, para melhor visualização e documentação do processo. Essa funcionalidade depende desses prefixos nos nomes dos ramos e nas mensagens de commit. Não incluir esses prefixos quebra a funcionalidade. Já conectei nosso Jira com nossa organização no Github, para ativar essa funcionalidade, agora é só nomear os ramos e commits adequadamente.

> Demonstração de como fazer os ramos e commits funcionarem de forma integrada com o Jira: https://www.youtube.com/watch?v=N-RZjp4og28&t=146s

#### Fluxo de uma issue:

2. Quando criada, a issue estará no Jira em estado NÃO INICIADO no quadro scrum.
3. O dev vai na issue (no Jira), e copia a abreviação/tag/etiqueta da issue (ex MM-123), e então move a issue da coluna NÃO INICIADO para a coluna EM PROGRESSO, no quadro scrum.
4. Atualizar repositório local com `git fetch --all`
5. Ativar o ramo principal, de desenvolvimento com `git checkout dev`
6. Criar novo ramo para a issue a desenvolver com `git checkout -b MM-123-nome-da-funcionalidade` ou similar, de acordo com o nome da feature e sua abreviação no Jira.
7. Desenvolver e resolver a issue. Faz os testes unitários e afins no próprio ambiente de desenvolvimento durante esse ciclo. Essa é a parte mais longa do trabalho, com a qual todo mundo já está habituado.
8. Commits devem ter o prefixo da issue na mensagem de commit, tipo `git commit -m "MM-123 Cria interface para X e Y."`  
    Se uma mensagem mais longa for necessária, usar `git commit` (sem o parâmetro `-m`) e colocar a abreviação da issue na primeira linha, escrevendo a mensagem explicando o commit nas linhas seguintes. Exemplo:  
    ```
    MM-123
    Cria interface X e Y.
    Utiliza uma busca binária para achar bla bla bla e por isso faz
    assim e assado ao invés daquele outro jeito.
    ```
9. Use os testes de integração (Postman) para garantir que a funcionalidade está correta e não afeta de forma inesperada outras partes do sistema. Modificações no Postman são solicitadas e precisam passar pelo QA, para não violar nenhum princípio nem quebrar nada.
10. Abre PR. O revisor precisa testar e aprovar a PR, garantindo que ela de fato não quebrou nada.
11. Com a PR aprovada pelo revisor, o ramo será mesclado ao ramo principal, dev. Isso vai disparar o fluxo de CI. Esse fluxo vai rodar testes de serviço no ambiente isolado do Github Actions, e se os testes passarem, vai efetuar deploy da nova versão no ambiente de desenvolvimento. Caso contrário, isso vai gerar uma notificação de erro de deploy.
12. O servidor será notificado via webhook que um push passou nos testes de serviço do Github Actions. Então o servidor vai desligar os serviços pertinentes, se atualizar com o ramo dev no Github, e reiniciar os serviços atualizados. O servidor enviará uma notificação com o resultado (canal a definir, mas provavelmente no Jira).
13. Se o serviço atualizou corretamente, a issue deve ser movida do estado EM PROGRESSO para o estado REVISÃO, e o trabalho do QA é disparado. Se o QA validar tudo de acordo com as especificações dos requisitos, ele deve mover a issue para o estado CONCLUÍDO.

**Revisão de Pull Requests:** O Antônio fica responsável de revisar (e testar) PRs no backend, e o Thiago fica responsável por isso no frontend. Neste contexto, revisar significa ler o código da PR, verificar se ele implementa o que foi pedido na sua issue, rodar e testar tudo na máquina do revisor. Se a PR passar nesse crivo, a PR pode ser aceita para ir online e ser revisada pelo QA.

Issue concluída é feature online ou bug corrigido, com tudo funcionando e sem quebrar nada no sistema. Só mover a issue de EM PROGRESSO para REVISÃO a PR subir e ficar online no servidor com sucesso.

Se o servidor cair depois de uma PR subir, o responsável pela infra (Lucas) deve ser acionado imediatamente para depurar o que houve no servidor, junto com o responsável pela issue e revisor da PR que falhou em funcionar online.

**Ramo principal:** é o ramo `dev`. Toda funcionalidade parte de lá e volta pra lá quando concluída. Quando estivermos prestes a lançar um release, o ambiente de `stage` será preparado para isso, iniciaremos um ciclo de release e o ramo `release` será criado/atualizado a partir de `stage`.

**Ciclo de release:** inicia com uma PR de `dev` para `stage`. Durante os dias seguintes, as atividades em `dev`são suspensas, e toda a equipe foca em corrigir bugs e refinar coisas no ramo `stage`. Quando tudo estiver pronto, o ramo `stage` será e testado exaustivamente, e depois serão feitas duas PR: uma de volta pra `dev` e outra para o ramo `release`. Por fim, partindo de `release`, será feito a entrega da versão estável no ambiente de produção, de forma manual.


# Projeto

Para a Secretaria Municipal da Eduçação, o processo de efetuar e distribuir as matrículas dos estudantes do ensino médio e fundamental é um trabalho longo, complexo e atualmente feito de forma completamente manual pelos funcionários da secretaria, com muitos estudantes sendo matriculados em escolas longe de suas casas, longe dos trabalhos dos pais, quando tém alguma necessidade especial os secretarios de escola devem ser encontrada manualmente em uma lista impressa de escolas com atendimento especial, sem informação no sistema sobre rotas de transporte público, apenas mostrando quais alunos desejam/tem transporte, sem mostrar a rota que é necessária para quais alunos em determinadas escolas, ou outras informações de tomada de decisão para a alocação dos estudantes, assim como não sabem quais escolas precisam de auxiliar de salas para atendimento especial para alunos com deficiências.

O "Melhor Matrícula" é um sistema com interface web para uso pelos cuidadores dos estudantes e pela própria secretaria para melhorar o processo de matrícula e alocação dos estudantes pelas escolas do município.

O que difere o "Melhor Matrícula" da solução atualmente em uso, é que quando o MM recebe os dados dos estudantes e dos cuidadores, o MM vai alocar os estudantes da melhor forma possível com base nas preferências fornecidas na hora da solicitação de matrícula, usando um algoritmo heurístico de otimização, levando em conta as informações geográficas, de transporte público, necessidades especializadas dos estudantes e a preferência dos cuidadores sobre a escola ser próxima da casa ou do trabalho, assim como horários de preferência. Dessa forma grande parte do trabalho será automatizado de forma inteligente, agilizando o processo de matrícula dos estudantes e melhorando a distribuição deles pelas escolas do município.

### Problemas

1) Matrículas Desbalanceadas
2) Matrículas Migratórias
3) Matriculas de Risco

### Expectativas

1) Uma interface clara, fácil de usar e com suporte para usuários PCD.
2) Opção de solicitação de matrícula com preferências, 1ª opção e 2ª opção de escola.
3) Distribuição automática dos estudantes pelas escolas de forma otimizada.

## Personas

Uma persona representa um usuário do produto e essa descrição deve falar não só o papel, mas também suas necessidades e seus objetivos. Isso cria uma representação realista dos usuários, auxiliando a equipe a descrever funcionalidades a partir do ponto de vista de quem vai usar o produto (Aguiar, 2021).

### Funcionário da Secretaria

*O que ela faz?* : Alimenta o sistema com informações novas sobre escolas. Faz matrícula/solicitação para cuidadores que não estão aptos a usarem a interface web do sistema para solicitarem matrícula sozinhos.

*O que ela espera?* : Ter menos trabalho com o processo de matrícula e alocação dos estudantes.

### Cuidador Apto com Computadores e Internet

*O que ela faz?* : Usa a interface web (site) do "Melhor Matrícula" para fazer a solicitação de matrícula dos seus dependentes.

*O que ela espera?* : Que o sistema seja intuitivo, permita solicitar matrícula para escolas específicas, perto de casa ou do trabalho, e receber alguma forma de notificação quando o resultado do processamento estiver disponível.

### Cuidador Não Apto com Computadores ou Internet

*O que ela faz?* : Vai à secretaria solicitar a matrícula de seus dependentes.

*O que ela espera?* : Ser atendido por um profissional da secretaria que saberá efetuar a matrícula de seus dependentes, de acordo com suas necessidades, e ser notificado do resultado quando este sair.

## Marcos

Devemos entregar **pequenas versões frequentes**. A equipe deve definir os marcos do projeto (*milestones)*, definindo os prazos de entrega e quais funcionalidades serão implementados até o final de cada marco. No final de cada marco devemos distribuir uma nova versão do produto, pronta para produção.

Podemos pensar nessas pequenas versões como MVPs (do inglês, *minimum viable product*). MVP é a versão mais simples de um produto que pode ser disponibilizada para a validação de um pequeno conjunto de hipóteses sobre o negócio. Após ser **construído,** o MVP é colocado à prova. Com isso, teremos dados que possibilitam **medir** o seu uso e, portanto, gerar o **aprendizado** desejado (Caroli, 2018).

### Marco 1 - 20/12/2022

Acreditamos que esse `Marco 1` vai conseguir `resultado esperado`. Saberemos que isso aconteceu com base em `métricas para validar a hipótese do negócio`.

#### Funcionalidades

- [x] Funcionalidade 1.
- [x] Funcionalidade 2.
- [x] Funcionalidade 3.

[Release Notes ](release_notes_1.md)

### Marco 2 - 20/01/2023

Acreditamos que esse `Marco 1` vai conseguir `resultado esperado`. Saberemos que isso aconteceu com base em `métricas para validar a hipótese do negócio`.

#### Funcionalidades 

- [x] Funcionalidade 1.
- [x] Funcionalidade 2.
- [ ] Funcionalidade 3.

[Release Notes ](release_notes_1.md)

## Riscos

1. **Risco 1** descrição do risco. *Severidade Baixa e Probabilidade Alta*.

   Ações para mitigação do risco:

   * Ação de mitigação 1.1.

2. **Risco 2** descrição do risco. *Severidade Média e Probabilidade Alta*.

   Ações para mitigação do risco:

   * Ação de mitigação 2.1.
   * Ação de mitigação 2.2.

## Componentes

### Frontend

Website contendo a interface gráfica para interação humana com sistema.

https://github.com/edgebr/templates-artefatos

### Backend

API REST servindo o sistema.

https://github.com/edgebr/templates-artefatos


### Algoritmo

Algoritmo heurístico de otimização que calcula a alocação dos estudantes para as escolas.


## Stakeholders

Stakeholder 1 <br />
*Key User - Cargo na Empresa X* <br />
*E-mail* <br />
(xx) xxxxx-xxxx

Stakeholder 2 <br />
*Key User - Cargo na Empresa X* <br />
*E-mail* <br />
(xx) xxxxx-xxxx

## Equipe

**Lucas Carvalho**  
Infra, DevOps, CI/CD, Algoritmo de Otimização, Coordenador da Equipe  
E-mail:  
https://github.com/kallyous


**Antônio**  
Desenvolvedor Backend  
E-mail:  
https://github.com/???

**Filipe**
Desenvolvedor Backend
E-mail:
https://github.com/???

**Iasmin Borba**  
Desenvolvedora Backend  
E-mail:  icb2@ic.ufal.br
https://github.com/IasminBorba


**Thiago**  
Desenvolvedor Frontend  
E-mail: trs@ic.ufal.br
https://github.com/ThiagoORuby


**Mickael**  
Desenvolvedor Frontend  
E-mail: 
https://github.com/mick3211  


**Victor**
Analista de Qualidade, Design
E-mail:
https://github.com/???

## Status Reports

[Status Report 1 (20/12/2022)](status_report_1.md)

## 1. Resumo do Problema

A Secretaria Municipal de Educação (Semed) de Maceió, órgão da Administração Direta, possui uma rede de ensino com 157 unidades escolares, sendo 60 CMEIs (Centros Municipais de Educação Infantil) e 91 Escolas de Ensino Fundamental, atendendo, ao todo, cerca de 58 mil estudantes. A Semed Maceió tem como principal missão a garantia de uma educação pública de qualidade e inclusiva, que proporcione o desenvolvimento integral de todas as crianças, adolescentes, jovens e adultos matriculados na rede.

Um dos desafios da Semed, é matricular e alocar os estudantes em sua rede de ensino de forma eficaz, a fim de prover educação pública a todos da forma mais acessível possível.

## 2. Solução Atual: SisLame (SL)

O SisLame (SL) é o sistema de matrículas atualmente em uso pela Semed. Ele oferece uma interface por onde matrículas podem ser feitas online ou presencialmente na própria secretaria.

As matrículas são feitas manualmente, entrando os dados do responsável e dos estudantes à mão. Tudo é escrito por extenso, mesmo endereços, o que gera grande quantidade de inconsistências e dados errados na base de dados da Semed.

A escola onde matricular o estudante precisa ser encontrada manualmente em uma lista de 157 escolas em ordem alfabética do nome das escolas, sem opção de busca por nome, suporte a necessidades específicas, localidade ou qualquer outra característica relevante para o interessado em efetuar a matrícula.

A interface do SL é contra-intuitiva, não possui opções de "Voltar" para telas anteriores, o botão de voltar do navegador quebra a página se for usado, qualquer modificação na operação sendo feita, requer recomeçar a operação desde o começo, as informações e fluxo de telas não estão organizados de forma compreensível.

Por esses e outros problemas com o SL, quase todas as pessoas vão à Semed para efetuar matrícula de forma presencial, para que os funcionários da Semed usem o SL para efetuar a matrícula, o que congestiona a secretaria ~~em períodos de matrícula~~.

Há também pessoas solicitando matrícula em escolas longe de suas casas por motivos como "essa escola é mais bonita" ou "está bem localizada, em bairro bom", e outros motivos subjetivos como esses, ocupando vagas em escolas que melhor poderiam ser alocadas para estudantes morando mais perto da escola em questão, levando a mais gastos de recursos e de tempo com deslocamentos, transporte escolar municipal, ou recorrendo a outros meios, como transporte coletivo ou privado.

Todos esses problemas levam a gargalos burocráticos e humanos no processo de matrículas, maior demora e pouca transparência no processo de matrícula, muitos estudantes acabam matriculados em escolas distantes ou de difícil acesso, maiores gastos públicos com transporte escolar e muitos estudantes com necessidades suporte específicos sem obter vaga em escolas que possuem infra-estrutura para atender suas necessidades específicas.

## 3. Nosso Projeto: Melhor Matrícula (MM)

Os objetivos principais do Melhor Matrícula são:

1. Fornecer um sistema de solicitação de matrículas com um fluxo online intuitivo e fácil de usar, para que o máximo possível de pessoas não precise ir presencialmente à Semed para efetuar a matrícula, descongestionando a secretaria;
2. Fornecer um sistema onde os fluxos de tarefas da secretaria são igualmente intuitivos e amigáveis, a fim de facilitar e agilizar o trabalho dos funcionários da Semed;
3. Através de um algoritmo inteligente de otimização combinatória, automatizar a alocação dos estudantes que solicitaram matrícula, priorizando estudantes com necessidades específicas em escolas com devido suporte, proximidade das residências dos estudantes com as escolas, ~~disponibilidade de transporte~~ (não incluir isso na primeira tentativa de vender o MVP aos professores, só se eles cobrarem algo nesse sentido ou disserem que nosso MVP é pequeno demais), ~~possibilidade de considerar a proximidade do trabalho dos pais mediante solicitação no próprio fluxo~~ (evitar isso também, argumentar que abre brecha pra fraude), duas escolas de preferência informadas na solicitação de matrícula, e disponibilidade de vagas nas escolas válidas.
4. Geração de relatórios com os resultados do processamentos das matrículas, para haver maior transparência sobre a alocação de estudantes pela rede de ensino.
5. Ter um fluxo no sistema que permita a funcionários da Semed ajustarem manualmente as matrículas após o algoritmo de otimização fazer as alocações, antes de efetivar as matrículas, permitindo aos profissionais da Semed terem a decisão final sobre as alocações de estudantes com ajustes finos que julguem necessários e tratar casos excepcionais.

Com isso o Melhor Matrícula não apenas facilitará o trabalho da Semed Maceió, mas automatizará o cerne do processo de matrícula de forma inteligente e otimizada, além de prover maior transparência para com a população.

## 4. Nosso MVP do Melhor Matrícula

### 4.1 Escopo do projeto:

* Escolas do ensino fundamental do município de Maceió.
* Estudantes residentes no município de Maceió.

A Semed Maceió é um ente administrativo municipal, então o escopo do projeto será restrito ao município de Maceió.

### 4.2 Fluxos do MVP proposto

#### 4.2.1 Fluxo de cadastro de Responsável/Cuidador

Fluxo de telas da interface web que provêm acesso à opção de uma pessoa se cadastrar no sistema. Uma pessoa pode ser sua própria responsável, se for maior de idade.

Tecnicamente, é possível um menor de idade responsável por si (emancipação), mas não vamos incluir esses casos excepcionais no escopo do MVP.

#### 4.2.2 Fluxo de cadastro de Dependente/Estudante

Após o cadastro de responsável, partindo de sua tela inicial pós login, ele pode adicionar dependentes e marcar a si mesmo como seu próprio dependente, para efetuar solicitações de matrícula.

#### 4.2.3 Fluxo de solicitação de matrícula online

Partindo da tela de responsável/cuidador, teremos também o fluxo de matrícula para os seus dependentes. Esse fluxo deve ficar disponível em períodos de matrícula apenas.

#### 4.2.4 Fluxo de solicitação de matrícula presencial

Uma variação do fluxo anterior, mas que assume o cuidador/responsável não ser apto ao uso de tecnologias, e portanto ele vai até a secretaria para efetuar os fluxos anteriores através de alguém da Semed.

#### 4.2.5 Fluxo automatizado de alocação de matrículas

Fluxo de quando o tempo de solicitação se encerra e o sistema inicia, na data e hora programada, (faz parte desse fluxo as telas usadas para agendar as datas de abertura das matrículas)

#### ~~4.2.? Fluxo de interposição de recursos~~

Importante no caso real, mas vamos tentar vender nosso MVP aos professores sem incluir esse fluxo, pois é uma coisa a menos para fazer.

#### 4.2.6 Fluxo de ajustes de matrículas pela secretaria

Disponível a funcionários da Semed para ajuste fino nas matrículas, antes de efetivar e publicar o resultado final. Cada ajuste feito dispara uma verificação na(s) escola(s) afetada pelo ajuste que alerta qualquer inconsistência que posse ser gerada pelo ajuste, e só efetiva o ajuste (ou sequencia de ajustes) se não causar nenhuma inconsistência.

#### 4.2.7 Fluxo de efetivação das matrículas (Resultado Final)

Encerrado o prazo de ajustes, o sistema efetiva as matrículas e gera um relatório geral, para a Semed incluir na publicação dos resultados na forma de edital, e disponibiliza um relatório pessoal para cada matrícula, acessível pelo usuário cuidador/responsável para ele entender como foi o processo e porquê ele teve sua solicitação de matrícula efetivada na escola para o qual foi alocado.

## 5. Conclusão

Para a Secretaria Municipal de Eduçação, o processo de efetuar e distribuir as matrículas dos estudantes do ensino fundamental é um trabalho longo, complexo e atualmente feito de forma completamente manual pelos funcionários da secretaria, com muitos estudantes sendo matriculados em escolas longe de suas casas, longe dos trabalhos dos pais, quando tém alguma necessidade especial os secretarios devem procurar manualmente em uma lista impressa de escolas com atendimento especial, sem informação no sistema sobre isso, apenas mostrando quais alunos desejam/tem transporte, sem informações claras de transporte, ou outras informações de tomada de decisão para a alocação dos estudantes, assim como não sabem quais escolas precisam de auxiliar de salas para atendimento especial para alunos com necessidades específicas.

O "Melhor Matrícula" é um sistema com interface web para uso pelos cuidadores dos estudantes e pela própria secretaria para melhorar o processo de matrícula e alocação dos estudantes pelas escolas do município.

O que difere o "Melhor Matrícula" da solução atualmente em uso, além da melhor interface para as funcionalidades que o SL já possui, é que quando o MM recebe os dados dos estudantes e dos cuidadores, o MM vai alocar os estudantes da melhor forma possível com base nas informações fornecidas na hora da solicitação de matrícula, usando um algoritmo de otimização que leva em conta as informações geográficas, de transporte, necessidades especializadas dos estudantes e a preferência dos cuidadores sobre a escola ser próxima da casa ou do trabalho, assim como horários de preferência.

Dessa forma grande parte do trabalho será automatizado de forma inteligente, agilizando o processo de matrícula dos estudantes, melhorando a distribuição deles pelas escolas do município, e aumentando a transparência do processo.
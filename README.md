### Links Importantes

- [Jira do Projeto](https://melhormatricula.atlassian.net/jira/software/projects/PMM/boards/3/timeline)
- [Figma dos Fluxos](https://www.figma.com/design/bCR5ORM1DpJ0wMOpMye99x/Telas?node-id=0-1&t=4HncMTk98sHpyP49-1)
- [Google Drive da Equipe](https://drive.google.com/drive/folders/1SheVcli1gWLMxCBHIedX6ASs3x-gNztp?usp=sharing)
- [Organização Interna](Organizacao.md)

# 1. Introdução

O sistema de matrículas atual da rede de ensino público municipal de Maceió é ineficiente, o que leva a muitos estudantes não conseguirem estudar por causa das consequências da má alocação dos estudantes pelas escolas.

A maior parte desse problema pode ser solucionado com um sistema de matrículas mais transparente e que faça uma alocação automatizada e inteligente dos estudantes através de um algoritmo de otimização.

# 2. Definição do Problema e Proposta
## 2.1 Resumo do Problema

A Secretaria Municipal de Educação (Semed) de Maceió, órgão da Administração Direta, possui uma rede de ensino com 157 unidades escolares, sendo 60 CMEIs (Centros Municipais de Educação Infantil) e 91 Escolas de Ensino Fundamental, atendendo, ao todo, cerca de 58 mil estudantes. A Semed Maceió tem como principal missão a garantia de uma educação pública de qualidade e inclusiva, que proporcione o desenvolvimento integral de todas as crianças, adolescentes, jovens e adultos matriculados na rede.

Um dos desafios da Semed, é matricular e alocar os estudantes em sua rede de ensino de forma eficaz, a fim de prover educação pública a todos da forma mais acessível possível.

## 2.2 Solução Atual: SisLame (SL)

O SisLame (SL) é o sistema de matrículas atualmente em uso pela Semed. Ele oferece uma interface por onde pré-matrículas podem ser feitas online ou presencialmente na própria secretaria.

As matrículas são feitas manualmente, entrando os dados do responsável e dos estudantes à mão. Tudo é escrito por extenso, mesmo endereços, o que gera grande quantidade de inconsistências e dados errados na base de dados da Semed.

A escola onde matricular o estudante precisa ser encontrada manualmente em uma lista de 157 escolas em ordem alfabética do nome das escolas, sem opção de busca por nome, suporte a necessidades específicas, localidade ou qualquer outra característica relevante para o interessado em efetuar a matrícula.

A interface do SL é contra-intuitiva, não possui opções de "Voltar" para telas anteriores, o botão de voltar do navegador quebra a página se for usado, qualquer modificação na operação sendo feita, requer recomeçar a operação desde o começo, as informações e fluxo de telas não estão organizados de forma compreensível.

Por esses e outros problemas com o SL, a maioria das pessoas vai à Semed para efetuar matrícula de forma presencial, para que os funcionários da Semed usem o SL para efetuar a matrícula, o que congestiona a secretaria em períodos de matrícula.

Há também pessoas solicitando matrícula em escolas longe de suas casas por motivos como "essa escola é mais bonita" ou "está bem localizada, em bairro bom", e outros motivos subjetivos como esses, ocupando vagas em escolas que melhor poderiam ser alocadas para estudantes morando mais perto da escola em questão, levando a mais gastos de recursos e de tempo com deslocamentos, transporte escolar municipal, ou recorrendo a outros meios, como transporte coletivo ou privado.

Todos esses problemas levam a gargalos burocráticos e humanos no processo de matrículas, maior demora e pouca transparência no processo de matrícula, muitos estudantes acabam matriculados em escolas distantes ou de difícil acesso, maiores gastos públicos com transporte escolar e muitos estudantes com necessidades suporte específicos sem obter vaga em escolas que possuem infra-estrutura para atender suas necessidades específicas.

## 2.3 Solução Proposta

### 4.1 Sistema Melhor Matrícula (MM)

Os objetivos principais do sistema Melhor Matrícula são:

1. Fornecer um sistema de solicitação de matrículas com um fluxo online intuitivo e fácil de usar, para que o máximo possível de pessoas não precise ir presencialmente à Semed para efetuar a matrícula, descongestionando a secretaria;

2. Fornecer um sistema onde os fluxos de tarefas da secretaria são igualmente intuitivos e amigáveis, a fim de facilitar e agilizar o trabalho dos funcionários da Semed;

3. Através de um algoritmo inteligente de otimização combinatória, automatizar a alocação dos estudantes que solicitaram matrícula, priorizando estudantes com necessidades específicas em escolas com devido suporte, proximidade das residências dos estudantes com as escolas, possibilidade de considerar a proximidade do trabalho dos pais mediante solicitação no próprio fluxo, duas escolas de preferência informadas na solicitação de matrícula, horários de preferência solicitados na matrícula, disponibilidade de vagas e horários  nas escolas válidas.

4. Geração de relatórios com os resultados dos processamentos das matrículas, para haver maior transparência sobre a alocação de estudantes pela rede de ensino.

5. Ter um fluxo no sistema que permita a funcionários da Semed ajustar manualmente as matrículas após o algoritmo de otimização fazer as alocações, antes de efetivar as matrículas, permitindo aos profissionais da Semed terem a decisão final sobre as alocações de estudantes com ajustes finos que julguem necessários e tratar casos excepcionais.

Com isso o Melhor Matrícula não apenas facilitará o trabalho da Semed Maceió, mas automatiza o cerne do processo de matrícula de forma inteligente e otimizada, além de prover maior transparência para com a população.


### 4.2 MVP do Melhor Matrícula

#### 4.2.1 Escopo do projeto:

- Escolas do ensino fundamental do município de Maceió.
- Estudantes residentes no município de Maceió.

A Semed Maceió é um ente administrativo municipal, então o escopo do projeto será restrito ao município de Maceió.

#### 4.2.2 Fluxos do MVP proposto
##### 4.2.2.0 Cadastro de funcionário da secretaria

Fluxo de telas pra adicionar funcionários da secretaria novos. Estes usuários terão acesso aos fluxos específicos de uso interno pela secretaria.

##### 4.2.2.1 Cadastro de responsável/cuidador

Fluxo de telas da interface web que provêm acesso à opção de uma pessoa se cadastrar no sistema. Uma pessoa pode ser sua própria responsável, se for maior de idade.

Tecnicamente, é possível um menor de idade responsável por si (emancipação), mas não vamos incluir esses casos excepcionais no escopo do MVP.

##### 4.2.2.2 Cadastro de dependente/estudante

Após o cadastro de responsável, partindo de sua tela inicial pós login, ele pode adicionar dependentes e marcar a si mesmo como seu próprio dependente, para efetuar solicitações de matrícula.

##### 4.2.2.3 Solicitação de pré-matrícula online

Partindo da tela home do responsável, teremos também o fluxo de pré-matrícula para os seus dependentes. Esse fluxo deve ficar disponível em períodos de matrícula apenas.

##### 4.2.2.4 Solicitação de matrícula presencial

Uma variação do fluxo anterior, mas que assume que o responsável vai até a secretaria para efetuar os fluxos anteriores através de alguém da Semed. Esse fluxo pertence à interface voltada para o secretário.

##### 4.2.2.5 Automatização de alocação de matrículas

Fluxo de quando o tempo de solicitação se encerra e o sistema inicia, na data e hora programada, (faz parte desse fluxo as telas usadas para agendar as datas de abertura das matrículas)

##### 4.2.2.6 Ajustes de matrículas pela secretaria

Disponível a funcionários da Semed para ajuste fino nas matrículas, antes de efetivar e publicar o resultado final. Cada ajuste feito dispara uma verificação na(s) escola(s) afetada pelo ajuste que alerta qualquer inconsistência que possa ser gerada pelo ajuste, e só efetiva o ajuste (ou sequência de ajustes) se não causar nenhuma inconsistência.

##### 4.2.2.7 Efetivação das matrículas (Resultado Final)

Encerrado o prazo de ajustes, o sistema efetiva as matrículas e gera um relatório geral, para a Semed incluir na publicação dos resultados na forma de edital, e disponibiliza um relatório pessoal para cada matrícula, acessível pelo usuário cuidador/responsável para ele entender como foi o processo e porquê ele teve sua solicitação de matrícula efetivada na escola para o qual foi alocado.

## 2.4 Conclusão

Para a Secretaria Municipal de Educação, o processo de efetuar e distribuir as matrículas dos estudantes do ensino fundamental é um trabalho longo, complexo e atualmente feito de forma completamente manual pelos funcionários da secretaria, com muitos estudantes sendo matriculados em escolas longe de suas casas, longe dos trabalhos dos pais, quando têm alguma necessidade especial os secretários devem procurar manualmente em uma lista impressa de escolas com atendimento especial, sem informação no sistema sobre isso, apenas mostrando quais alunos desejam/tem transporte, sem informações claras de transporte, ou outras informações de tomada de decisão para a alocação dos estudantes, assim como não sabem quais escolas precisam de auxiliar de salas para atendimento especial para alunos com necessidades específicas.

O "Melhor Matrícula" é um sistema com interface web para uso pelos cuidadores dos estudantes e pela própria secretaria para melhorar o processo de matrícula e alocação dos estudantes pelas escolas do município.

O que difere o "Melhor Matrícula" da solução atualmente em uso, além da melhor interface para as funcionalidades que o SL já possui, é que quando o MM recebe os dados dos estudantes e dos cuidadores, o MM vai alocar os estudantes da melhor forma possível com base nas informações fornecidas na hora da solicitação de matrícula, usando um algoritmo de otimização que leva em conta as informações geográficas, de transporte, necessidades especializadas dos estudantes e a preferência dos cuidadores sobre a escola ser próxima da casa ou do trabalho, assim como horários de preferência.

Dessa forma, grande parte do trabalho será automatizado de forma inteligente, agilizando o processo de matrícula dos estudantes, melhorando a distribuição deles pelas escolas do município, e aumentando a transparência do processo.
# 3. Personas e suas Histórias

### 3.1 [Sra Viviane](Recursos_Ferramentas/Personas/Persona_Sra_Viviane.pdf)

### 3.2 [Sra Daniela](Recursos_Ferramentas/Personas/Persona_Sra_Daniela.pdf)

### 3.3 [Sr Fábio](Recursos_Ferramentas/Personas/Persona_Sr_Fabio.pdf)

### 3.4 [Srta Amanda](Recursos_Ferramentas/Personas/Persona_Srta_Amanda.pdf)

### 3.5 [Dona Maria](Recursos_Ferramentas/Personas/Persona_Dona_Maria.pdf)

### 3.6 [Secretário Manoel](Recursos_Ferramentas/Personas/Persona_Secretario_Manoel.pdf)


# 6. Macros

## Macro 1: Estudo do Problema - 27/02/2025

Acreditamos que o estudo aprofundado do problema irá munir a equipe do conhecimento e entendimento necessário para planejar uma boa solução, que ataque o problema de forma efetiva. Isso pode ser medido pela documentação produzida ao final desse macro, contando com a elaboração detalhada de personas, suas histórias e refinamentos na proposta de solução que reflitam a especificidade do problema e das personas.

### Funcionalidades

- [x] Definição do problema refinada
- [x] Personas refinadas
- [x] Histórias de usuário refinadas
- [x] Solução proposta refinada

## Macro 2: Planejamento da Solução - 21/03/2025

O planejamento da solução vai prover um mapa sólido sobre como construir a solução ajustada ao problema. Ao final desse marco teremos uma apresentação clara e objetiva da solução, bem como um fluxo enxuto de telas demonstrando como o MVP da solução será quando construído.

### Funcionalidades

- [x] Fluxo de telas no Figma
- [x] Vídeo de apresentação das telas no Figma
- [x] Apresentação do projeto como um todo

## Marco 3: Autenticação e cadastro

O sistema de autenticação e cadastro vai possibilitar que usuários, responsáveis ou secretários, consigam acessar o sistema de forma segura.

Funcionalidade 1. Autenticação

- História 1.1: Como responsável, quero fazer login com email e senha para acessar minha conta
- História 1.2: Como secretário, quero fazer login com as credenciais da secretaria para acessar o sistema
- História 1.3: Como usuário, quero poder recuperar minha senha via email

#### Funcionalidade 2. Cadastro de responsável

- História 2.1: Como responsável, quero criar minhas credenciais para login, fornecendo dados básicos sobre mim
- História 2.2: Como responsável, quero poder já associar um dependente durante o meu cadastro
  
## Marco 4: Gerenciamento de dependentes, pré-matrícula e perfil

O gerenciamento vai permitir que responsáveis possam administrar seus dependentes e solicitar suas pré-matrículas. 

#### Funcionalidade 1. Cadastro/Edição de dependentes

- História 1.1: Como responsável, quero poder adicionar um novo dependente, fornecendo dados básicos sobre ele
- História 1.2: Como responsável, quero editar ou remover um dependente cadastrado

#### Funcionalidade 2. Gerenciamento de perfil

- História 2.1: Como responsável, quero poder atualizar meus dados de cadastro

#### Funcionalidade 3. Solicitação de pré-matrícula

- História 3.1: Como responsável, quero, para um dependente, realizar a solicitação de matrícula para o ano letivo corrente
- História 3.2: Como responsável, quero realizar a pré-matrícula em etapas, de forma clara e objetiva
- História 3.3: Como responsável, quero poder escolher as opções de escola na pré-matrícula conhecendo as escolas disponíveis, de acordo com as informações fornecidas nas etapas anteriores

## Marco 5: Administração e consultas por secretários

A administração e consultas vai possibilitar que secretários realizem a pré-matrícula para responsáveis impossibilitados de fazê-la de forma online, bem como busquem, de forma mais detalhadas, dados cadastrados no sistema

#### Funcionalidade 1. Cadastro manual

- História 1.1: Como secretário, quero cadastrar um responsável/dependente manualmente para casos de baixo letramento digital.

#### Funcionalidade 2. Solicitação de pré-matrícula

- História 2.1: Como responsável, quero poder ir até uma secretaria de educação para realizar a pré-matrícula do(s) meu(s) dependentes
- História 2.2: Como secretário, quero realizar pré-matrícula para um dependente específico

#### Funcionalidade 3. Realização de consultas

História 3.1: Como secretário, quero realizar consultas nos dados de alunos, responsáveis e matrículas, podendo aplicar filtros a eles**


# 7. Componentes

### Frontend

Website contendo a interface gráfica para interação humana com sistema.

[https://github.com/Equipe-Melhor-Matricula/Frontend](https://github.com/Equipe-Melhor-Matricula/Frontend)

### Backend

API REST servindo o sistema.

[https://github.com/Equipe-Melhor-Matricula/Backend](https://github.com/Equipe-Melhor-Matricula/Backend)

### Algoritmo

Algoritmo heurístico de otimização que calcula a alocação dos estudantes para as escolas.

[https://github.com/Equipe-Melhor-Matricula/Otimizador](https://github.com/Equipe-Melhor-Matricula/Otimizador)

# 8. Equipe

Lucas  
Infra, DevOps, CI/CD, Algoritmo de Otimização, Coordenador da Equipe  
E-mail: [lcf@ic.ufal.br](mailto:lcf@ic.ufal.br)  
[https://github.com/kallyous](https://github.com/kallyous)  

Antônio  
Desenvolvedor Backend  
E-mail: [aeso@ic.ufal.br](mailto:aeso@ic.ufal.br)  
[https://github.com/AntoniEduardoSO](https://github.com/AntoniEduardoSO)  

Filipe  
Desenvolvedor Backend  
E-mail: [mrf@ic.ufal.br](mailto:mrf@ic.ufal.br)  
[https://github.com/Filipemrr](https://github.com/Filipemrr)  

Iasmin Borba  
Desenvolvedora Backend  
E-mail: [icb2@ic.ufal.br](mailto:icb2@ic.ufal.br)  
[https://github.com/IasminBorba](https://github.com/IasminBorba)  

Thiago  
Desenvolvedor Frontend  
E-mail: [trs@ic.ufal.br](mailto:trs@ic.ufal.br)  
[https://github.com/ThiagoORuby](https://github.com/ThiagoORuby)  

Mickael  
Desenvolvedor Frontend  
E-mail: [jvgs@ic.ufal.br](mailto:jvgs@ic.ufal.br)  
[https://github.com/mick3211](https://github.com/mick3211)  

Victor  
Analista de Qualidade, Design  
E-mail: [jvdso@ic.ufal.br](mailto:jvdso@ic.ufal.br)  
[https://github.com/josevict0r](https://github.com/josevict0r)  

# 9. Stakeholders

```
Patrick Santos Ferreira
Professor e secretário
(82) 9675-2638

Prof Narciso  
Professor e secretário
(82) 9907-8946
```

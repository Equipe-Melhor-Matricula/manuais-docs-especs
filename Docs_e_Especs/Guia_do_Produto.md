# Projeto

Para a Secretaria Municipal da Eduçação, o processo de efetuar e distribuir as matrículas dos estudantes do ensino médio e fundamental é um trabalho longo, complexo e atualmente feito de forma completamente manual pelos funcionários da secretaria.

O "Melhor Matrícula" é um sistema online para pré-matrículas, para o uso dos responsáveis pelos estudantes e da Semed, para melhorar o processo de matrícula e alocação dos estudantes pelas escolas.

O que difere o "Melhor Matrícula" da solução atualmente em uso, é que quando o MM recebe os dados dos estudantes e dos cuidadores, o MM vai alocar os estudantes da melhor forma possível com base nas informações sobre o estudante, usando um algoritmo de otimização.

Dessa forma, grande parte do trabalho será automatizado de forma inteligente, agilizando o processo de matrícula dos estudantes e melhorando a distribuição deles pelas escolas do município.

### Problemas

1) Alocações Desbalanceadas
2) Alocações Migratórias
3) Alocações de Risco

### Expectativas

1) Uma interface clara e fácil de usar, para computadores pessoais ou celulares.
2) Fluxo de pré-matrícula fácil de percorrer.
3) Transparência: Emissão de relatórios e/ou informativos explicando o resultado das alocações.
4) Alocação automática dos estudantes pelas escolas de forma otimizada.

## Personas

### Persona 1

*O que ela faz?* : Alimenta o sistema com informações novas sobre escolas. Faz matrícula/solicitação para cuidadores que não estão aptos a usarem a interface web do sistema para solicitarem matrícula sozinhos.

*O que ela espera?* : Ter menos trabalho com o processo de matrícula e alocação dos estudantes.

### Persona 2

*O que ela faz?* : Usa a interface web (site) do "Melhor Matrícula" para fazer a solicitação de matrícula dos seus dependentes.

*O que ela espera?* : Que o sistema seja intuitivo, permita solicitar matrícula para escolas específicas, perto de casa ou do trabalho, e receber alguma forma de notificação quando o resultado do processamento estiver disponível.

### Persona 3

*O que ela faz?* : Vai à secretaria solicitar a matrícula de seus dependentes.

*O que ela espera?* : Ser atendido por um profissional da secretaria que saberá efetuar a matrícula de seus dependentes, de acordo com suas necessidades, e ser notificado do resultado quando este sair.

## Marcos

### Lembretes

Devemos entregar **pequenas versões frequentes**. A equipe deve definir os marcos do projeto (*milestones*), definindo os prazos de entrega e quais funcionalidades serão implementados até o final de cada marco. No final de cada marco devemos distribuir uma nova versão do produto, pronta para produção.

Podemos pensar nessas pequenas versões como MVPs (do inglês, *minimum viable product*). MVP é a versão mais simples de um produto que pode ser disponibilizada para a validação de um pequeno conjunto de hipóteses sobre o negócio. Após ser **construído,** o MVP é colocado à prova. Com isso, teremos dados que possibilitam **medir** o seu uso e, portanto, gerar o **aprendizado** desejado (Caroli, 2018).

### Estudo do Problema - 27/02/2025

Acreditamos que o estudo aprofundado do problema irá munir a equipe do conhecimento e entendimento necessário para planejar uma boa solução, que ataque o problema de forma efetiva. Isso pode ser medido pela documentação produzida ao final desse macro, contando com a elaboração detalhada de personas, suas histórias e refinamentos na proposta de solução que reflitam a especificidade do problema e das personas.

#### Funcionalidades

- [x] Definição do problema refinada
- [x] Personas refinadas
- [x] Histórias de usuário refinadas
- [x] Solução proposta refinada

### Planejamento da Solução - 21/03/2025

Acreditamos que esse `Marco 1` vai conseguir `resultado esperado`. Saberemos que isso aconteceu com base em `métricas para validar a hipótese do negócio`.

O planejamento da solução vai prover um mapa sólido sobre como construir a solução ajustada ao problema. Ao final desse marco teremos uma apresentação clara e objetiva da solução, bem como um fluxo enxuto de telas demonstrando como o MVP da solução será quando construído.

#### Funcionalidades

- [x] Fluxo de telas no Figma
- [x] Vídeo de apresentação das telas no Figma
- [x] Apresentação do projeto como um todo

## Riscos

Não foram identificados riscos para os marcos _Estudo do Problema_ e _Planejamento da Solução_

## Componentes

### Frontend

Website contendo a interface gráfica para interação humana com sistema.

[https://github.com/Equipe-Melhor-Matricula/Frontend](https://github.com/Equipe-Melhor-Matricula/Frontend)

### Backend

API REST servindo o sistema.

[https://github.com/Equipe-Melhor-Matricula/Backend](https://github.com/Equipe-Melhor-Matricula/Backend)


### Algoritmo

Algoritmo heurístico de otimização que calcula a alocação dos estudantes para as escolas.

[https://github.com/Equipe-Melhor-Matricula/Otimizador](https://github.com/Equipe-Melhor-Matricula/Otimizador)

## Stakeholders

```
Elisabete
Funcionária da Secretaria
E-mail: TODO
(xx) xxxxx-xxxx

Carinha que usa o Sislame  
Autônomo
E-mail: TODO
(xx) xxxxx-xxxx
```

## Equipe

**Lucas Carvalho**  
Infra, DevOps, CI/CD, Algoritmo de Otimização, Coordenador da Equipe  
E-mail:  lcf@ic.ufal.br
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

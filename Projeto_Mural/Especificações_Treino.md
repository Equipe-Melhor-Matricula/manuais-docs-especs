# Especificações do Projeto Mural

O objetivo é se familiarizar com nossas ferramentas e fluxo de trabalho. Cada um vai reproduzir sua parte do projeto localmente apenas, mas deverá tudo passar nos testes ao final do treino. Não serão abertas PRs. Esse projeto de treino não será mesclado em dev, embora algumas coisas possam ser aproveitadas (uns copia e cola da vida).

Não é pra ficar bom ou bonito. É pra funcionar (i.e. passar nos testes) e aprender.

## Histórias de Usuário em BDD

**Cadastro -> Entrar**
```plaintext
Cenário: Página de cadastro
  Dado que usuário forneceu email "joao@mail.com" e senha "12345"
  Quando ele seleciona a opção de efetuar o cadastro
  Então o sistema cria uma conta nova com essas credencias
    E notifica usuário de que a operação funcionou
    E o direciona para a página de login
```

**Entrar / Login -> Mural**
```plaintext
Cenário: Página de login
  Dado que usuário forneceu email "joao@mail.com" e senha "12345"
  Quando ele escolhe a opção de entrar
  Então o direciona o usuário para a página do mural
```

**Mural -> Sair / Logout**
```plaintext
Cenário: Página do mural de avisos
  Dado um usuário logado
  Quando ele escolher a opção sair
  Então o sistema deve direcioná-lo para página de entrar
```

**Mural -> Criar Aviso**
```plaintext
Cenário: Página do mural de avisos
  Dado um usuário logado
  Quando ele escolher a opção de criar novo aviso
  O sistema deve direcionar para página de criar novo aviso
```

**Criar Aviso**
```plaintext
Cenário: Página de criar aviso
  Dado que usuário forneceu o título "Alerta de chuva forte"
    E o corpo do aviso "Previsão de chuvas fortes, instituto não abrirá."
  Quando ele escolher a opção de confirmar criação do aviso
  Então o sistema deve criar nova mensagem com esse título e corpo
    E direcionar o usuário para a página do mural
    E a mensagem criada deve aparecer no mural
```

**Mural -> Opções de Modificar Avisos**
```plaintext
Cenário: Página do mural
  Dado um usuário logado
  Quando ele é o dono de uma mensagem visível no mural
  Então aparecem as opções de editar e remover esse aviso
```

**Mural -> Editar Aviso**
```plaintext
Cenário: Página do mural
  Dado um usuário logado
    E um aviso de sua autoria com título "Alerta de chuva forte"
  Quando o usuário escolher a opção de editar esse aviso
  Então o sistema direciona o usuário para a página de editar esse aviso
    E exibe o título atual "Alerta de chuva forte"
    E exibe o corpo atual "Previsão de chuvas fortes, instituto não abrirá."
```

**Editar Aviso -> Cancelar**
```plaintext
Cenário: Página de editar aviso
  Dado a mensagem de título "Alerta de chuva forte"
    E corpo "Previsão de chuvas fortes, instituto não abrirá."
  Quando o usuário escolher a opção cancelar
  Então o sistema o direciona para a página do mural
```

**Editar Aviso -> Confirmar**
```plaintext
Cenário: Página de editar aviso
  Dado a mensagem de título "Alerta de chuva forte"
    E corpo "Previsão de chuvas fortes, instituto não abrirá."
  Quando o usuário modificar o título para "Chuvas nem tão fortes"
    E modificar o corpo para "As chuvas serão brandas, o instituto abrirá."
    E escolher a opção confirmar
  Então o sistema altera o aviso
    E redireciona o usuário para a página do mural de avisos
```

**Mural -> Remover Aviso**
```plaintext
Cenário: Página do mural
  Dado um usuário logado
    E um aviso de sua autoria com título "Alerta de chuva forte"
  Quando o usuário escolher a opção de remover esse aviso
    E escolher opção confirmar na mensagem de confirmação de remoção
  Então o sistema remove o aviso do mural
```

## Fluxo de Telas

**São 5 páginas no total:**
- Cadastro
- Entrar
- Mural
- Criar Aviso
- Editar Aviso

![[fluxo-de-telas.jpg]]

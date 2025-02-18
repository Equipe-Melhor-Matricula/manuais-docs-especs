# Guia: Como Revisar uma Pull Request no GitHub

Revisar uma Pull Request é uma etapa essencial no desenvolvimento colaborativo, pois ajuda a garantir qualidade, padronização e a detecção de problemas antes que o código seja integrado.

---

## 1. **Objetivo da Revisão**

O objetivo da revisão de código é:
- Garantir que o código segue as melhores práticas e padrões da equipe.
- Identificar erros lógicos ou técnicos.
- Confirmar que as mudanças atendem aos requisitos especificados.
- Ajudar os desenvolvedores a melhorar, fornecendo feedback construtivo.

---

## 2. **Passo a Passo**

### 2.1. **Acesse a Pull Request**
1. Vá até o repositório no GitHub.
2. Clique na aba **Pull Requests**.
3. Encontre a PR que você precisa revisar e clique nela.

---

### 2.2. **Leia o Título e a Descrição**
Antes de olhar o código, entenda o contexto da PR:
- O **título** deve resumir a mudança.
- A **descrição** deve explicar:
  - O problema que está sendo resolvido.
  - A abordagem utilizada.
  - Como testar as mudanças.
  
Certifique-se de que a descrição está clara. Se não estiver, peça ao autor para melhorar.

---

### 2.3. **Verifique a Lista de Arquivos Alterados**
Na aba **Files changed**, você verá os arquivos modificados. Analise:
- **Número de alterações**: Se a PR for muito grande, avalie se ela pode ser dividida em partes menores.
- **Escopo**: As mudanças estão dentro do propósito descrito? Evite "PRs gigantes" que resolvem problemas não relacionados.

---

### 2.4. **Revisão Técnica**
Agora é hora de analisar o código. Confira os seguintes pontos:

#### **1. Qualidade do Código**
- O código está limpo e legível?
- Segue os padrões definidos pela equipe?
- Há comentários explicativos para trechos complexos?

#### **2. Lógica**
- A lógica implementada é correta?
- Teste mentalmente os fluxos principais e alternativos.
- Existem casos extremos (edge cases) que não foram tratados?

#### **3. Testes**
- A PR inclui testes automatizados?
- Testes cobrem os cenários esperados?
- A cobertura de código diminuiu? 

#### **4. Segurança**
- O código introduz vulnerabilidades, como injeções SQL ou exposição de dados sensíveis?
- Dados fornecidos pelo usuário são devidamente validados?

#### **5. Performance**
- Há gargalos óbvios no desempenho?
- Operações de leitura/escrita estão otimizadas?

#### **6. Manutenção**
- O código é fácil de entender e modificar?
- Nomes de variáveis, funções e classes são descritivos?

---

### 2.5. **Teste o Código Localmente (Opcional)**
Se necessário, baixe a branch da PR e teste localmente:
```bash
git fetch origin minha-feature
git checkout minha-feature
```
Execute o projeto e os testes automatizados:
```bash
npm test  # Para projetos Node.js
pytest    # Para projetos Python
dotnet test  # Para projetos C#
```
Avalie se as mudanças funcionam conforme o esperado.

---

### 2.6. **Forneça Feedback**
Na aba **Files changed**:
4. Clique na linha de código que deseja comentar.
5. Deixe um comentário claro e construtivo:
   - Evite comentários vagos como "Isso está errado".
   - Prefira sugestões específicas, como:  
     _"Essa variável poderia ter um nome mais descritivo para facilitar a leitura."_  
6. Use exemplos, se necessário.

Você também pode deixar **comentários gerais** no topo da PR.

---

### 2.7. **Aprovar ou Solicitar Alterações**
Após revisar, escolha uma das opções no GitHub:

#### **1. Request changes** (Solicitar alterações):
- Use se houver problemas técnicos, de lógica ou qualidade que precisam ser corrigidos.
- Escreva claramente o que precisa ser alterado e por quê.

#### **2. Approve** (Aprovar):
- Use quando a PR estiver pronta para ser integrada.

#### **3. Comment** (Comentar):
- Use para feedback não bloqueante ou sugestões opcionais.

---

## 3. **Dicas para Feedback Construtivo**

7. **Seja específico**:
   - _"Essa função tem uma lógica duplicada com a função X. Sugiro criar uma função genérica para evitar redundância."_  

8. **Evite tom crítico**:
   - Prefira _"Talvez fosse mais eficiente usar Y aqui"_ ao invés de _"Isso está errado."_  

9. **Reconheça pontos positivos**:
   - _"Ótima abordagem para resolver o problema da validação."_  

10. **Forneça contexto**:
   - _"Com base nos padrões que definimos, acho que podemos melhorar essa parte."_  

---

## 4. **Checklist de Revisão**

Use esta lista para garantir que a revisão foi completa:
- [ ] A descrição da PR está clara?
- [ ] A PR resolve o problema descrito?
- [ ] O código segue os padrões da equipe?
- [ ] O código está bem organizado e legível?
- [ ] Testes foram escritos e cobrem casos principais e extremos?
- [ ] Há problemas de segurança ou performance?
- [ ] A PR está dentro do escopo definido?

---

## 5. **Finalizando**
- Após aprovação, informe o autor que o merge pode ser feito ou faça você mesmo, conforme a política da equipe.
- Certifique-se de apagar a branch se não for mais necessária.

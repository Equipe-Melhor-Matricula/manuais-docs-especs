# Guia: Como abrir um Pull Request no GitHub

## 1. **Pré-requisitos**
Antes de abrir um Pull Request, você deve:
- Ter um repositório configurado e acesso ao GitHub.
- Ter feito alterações no código local ou em uma branch específica no repositório remoto.
- Ter certeza de que as alterações estão organizadas, testadas e prontas para revisão.

---

## 2. **Passo a Passo**

### 2.1. **Crie uma branch para suas alterações**
É uma boa prática criar uma branch separada para suas mudanças, evitando alterar diretamente a branch principal (`main` ou `master`).  
No terminal, faça:
```bash
git checkout -b minha-feature
```
Substitua `minha-feature` por um nome descritivo da sua mudança, como `adicionar-login`.

### 2.2. **Faça suas alterações e commit**
1. Edite os arquivos necessários no projeto.
2. Adicione suas mudanças:
   ```bash
   git add .
   ```
3. Crie um commit com uma mensagem clara:
   ```bash
   git commit -m "Adiciona funcionalidade de login para usuários"
   ```

### 2.3. **Envie as alterações para o repositório remoto**
Empurre sua branch para o repositório remoto:
```bash
git push origin minha-feature
```

---

### 2.4. **Abra o Pull Request (PR) no GitHub**
4. **Acesse o repositório no GitHub**.  
   Vá para a página do repositório no navegador.

5. **Identifique a branch para merge**:
   - Você verá uma notificação ou botão sugerindo a criação de um PR para a branch que acabou de enviar.
   - Caso contrário, clique em **Pull requests** na barra de navegação e em **New Pull Request**.

6. **Configure o PR**:
   - Escolha a branch de destino (geralmente `main` ou `master`) no lado direito.
   - Escolha sua branch de origem (`minha-feature`) no lado esquerdo.
   - Certifique-se de que as mudanças estão corretas na visualização.

7. **Adicione um título e descrição**:
   - **Título**: Resuma o que a mudança faz, como `Adiciona funcionalidade de login para usuários`.
   - **Descrição**: Explique as alterações, incluindo:
     - O problema que a mudança resolve.
     - As abordagens usadas.
     - Como testar as mudanças (se aplicável).

   Exemplo:
   ```markdown
   **Descrição**
   Este PR adiciona a funcionalidade de login para os usuários. Ele utiliza autenticação JWT para gerenciar sessões.

   **Como testar**
   - Clone o repositório.
   - Execute `npm start`.
   - Acesse `/login` e use as credenciais test@example.com / password123.
   ```

8. **Defina revisores e assignees (opcional)**:
   - Adicione revisores da equipe (quem vai revisar o código).
   - Assigne a si mesmo ou a outra pessoa responsável pelo PR.

9. **Envie o PR**:
   Clique no botão **Create Pull Request**.

---

### 2.5. **Acompanhe o PR**
- Aguarde revisões da equipe.
- Responda a comentários diretamente no GitHub.
- Faça mudanças solicitadas em sua branch local e atualize o PR:
   ```bash
   git add .
   git commit -m "Correções solicitadas no PR"
   git push origin minha-feature
   ```
O GitHub atualizará automaticamente o PR com suas novas alterações.

---

### 2.6. **Finalizando o PR**
10. Após aprovação, você ou alguém da equipe pode fazer o merge:
   - Escolha **Merge Pull Request** na página do PR.
   - Apague a branch no GitHub, se necessário, clicando em **Delete Branch**.

11. Verifique se as mudanças foram incorporadas corretamente na branch principal.

---

## 3. **Dicas Importantes**
- **Faça commits atômicos**: Divida alterações grandes em commits menores e mais descritivos.
- **Escreva boas mensagens de commit**: Seja claro e explique o que foi alterado.
- **Sincronize frequentemente**: Sempre atualize sua branch com a branch principal antes de abrir o PR:
  ```bash
  git pull origin main
  ```

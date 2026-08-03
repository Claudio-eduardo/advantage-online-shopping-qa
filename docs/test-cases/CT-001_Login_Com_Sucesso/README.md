# CT-001 – Login com sucesso

---

# Objetivo

Validar que um usuário previamente cadastrado consegue realizar login com sucesso na aplicação utilizando credenciais válidas.

---

# Tipo de Teste

**Teste Funcional**

---

# Prioridade

**Alta**

### Justificativa

A autenticação é necessária para acessar funcionalidades restritas, como gerenciamento do perfil, histórico de pedidos e fluxo completo de checkout.

---

# Pré-condições

- Aplicação disponível.
- Usuário previamente cadastrado.
- Usuário deslogado.
- Tela de autenticação acessível.

---

# Massa de teste

| Campo | Valor |
|---|---|
| Username | Usuário válido previamente cadastrado |
| Password | Senha válida correspondente ao usuário |

---

# Passos para execução

1. Acessar a aplicação **Advantage Online Shopping**.
2. Clicar no ícone de usuário localizado no cabeçalho.
3. Aguardar a abertura do modal de autenticação.
4. Informar um nome de usuário válido no campo **Username**.
5. Informar a senha correspondente no campo **Password**.
6. Clicar no botão **SIGN IN**.

---

# Resultado esperado

- O sistema deve autenticar o usuário com sucesso.
- O modal de login deve ser fechado.
- O nome do usuário autenticado deve ser exibido no cabeçalho.
- O usuário deve permanecer autenticado durante a navegação.
- Nenhuma mensagem de erro deve ser apresentada.

---

# Critério de aprovação

O caso será considerado **Aprovado** quando o usuário conseguir realizar login com credenciais válidas e seu nome for exibido no cabeçalho da aplicação.

---

# Resultado da execução

**Status:** ✅ Aprovado

O sistema autenticou o usuário corretamente, fechou o modal de login e passou a exibir o nome do usuário no cabeçalho.

---

# Observações

- O teste foi realizado utilizando o Google Chrome.
- Não foram observadas inconsistências no fluxo de autenticação com credenciais válidas.
- O usuário permaneceu autenticado durante a navegação realizada após o login.

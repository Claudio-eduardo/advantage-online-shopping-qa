# CT-004 – Editar quantidade do produto no carrinho

---

# Objetivo

Validar que um usuário autenticado consegue editar a quantidade de um produto já adicionado ao carrinho e que os valores são recalculados corretamente.

---

# Tipo de Teste

**Teste Funcional**

---

# Prioridade

**Alta**

### Justificativa

A edição de quantidade afeta diretamente o conteúdo e o valor total da compra, sendo uma funcionalidade importante do carrinho.

---

# Pré-condições

- Aplicação disponível.
- Usuário autenticado.
- Produto adicionado ao carrinho.
- Produto com estoque suficiente para a nova quantidade.

---

# Massa de teste

| Campo | Valor |
|---|---|
| Usuário | Usuário válido e autenticado |
| Quantidade inicial | 1 unidade |
| Nova quantidade | 2 unidades |
| Estoque | Igual ou superior a 2 unidades |

---

# Passos para execução

1. Acessar a aplicação.
2. Realizar login com uma conta válida.
3. Adicionar um produto ao carrinho com quantidade igual a 1.
4. Acessar o carrinho de compras.
5. Clicar em **EDIT** no produto.
6. Alterar a quantidade de 1 para 2 unidades.
7. Clicar em **ADD TO CART** para confirmar a alteração.
8. Retornar ao carrinho.
9. Verificar a quantidade e o valor total.

---

# Resultado esperado

- Apenas o produto selecionado deve ser atualizado.
- A quantidade deve ser alterada para 2 unidades.
- A cor e as demais informações do produto devem permanecer inalteradas.
- O valor referente ao produto deve ser recalculado.
- O valor total do carrinho deve ser atualizado corretamente.
- Nenhum outro item deve sofrer alterações.

---

# Critério de aprovação

O caso será considerado **Aprovado** quando apenas o produto selecionado tiver sua quantidade atualizada e os valores forem recalculados corretamente.

---

# Resultado da execução

**Status:** ✅ Aprovado

Para o usuário autenticado, a quantidade do produto selecionado foi atualizada corretamente e o valor total do carrinho foi recalculado.

---

# Observações

- O cenário principal foi aprovado para usuário autenticado.
- Foram identificadas inconsistências no fluxo de edição para usuários não autenticados.
- Os comportamentos inesperados estão documentados nos relatórios **BUG-002**, **BUG-003** e **BUG-008**.

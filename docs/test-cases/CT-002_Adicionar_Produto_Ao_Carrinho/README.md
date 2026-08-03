# CT-002 – Adicionar produto ao carrinho

---

# Objetivo

Validar que o usuário consegue selecionar um produto, definir suas características e adicioná-lo corretamente ao carrinho de compras.

---

# Tipo de Teste

**Teste Funcional**

---

# Prioridade

**Alta**

### Justificativa

A adição de produtos ao carrinho é uma etapa essencial do fluxo de compra e necessária para que o usuário consiga prosseguir até o checkout.

---

# Pré-condições

- Aplicação disponível.
- Existência de produtos disponíveis para compra.
- Produto selecionado deve possuir estoque disponível.
- Usuário pode estar autenticado ou não autenticado.

---

# Massa de teste

| Campo | Valor |
|---|---|
| Categoria | Speakers |
| Produto | Produto disponível na categoria |
| Cor | Uma das variações disponíveis |
| Quantidade | 1 unidade |

---

# Passos para execução

1. Acessar a aplicação **Advantage Online Shopping**.
2. Selecionar a categoria **Speakers**.
3. Escolher um produto disponível.
4. Acessar a página de detalhes do produto.
5. Selecionar uma cor disponível.
6. Manter a quantidade em **1 unidade**.
7. Clicar no botão **ADD TO CART**.
8. Abrir o carrinho de compras.

---

# Resultado esperado

- O produto deve ser adicionado ao carrinho.
- O contador do carrinho deve ser atualizado.
- O carrinho deve apresentar o nome correto do produto.
- A cor selecionada deve ser registrada corretamente.
- A quantidade deve ser exibida como 1 unidade.
- O preço do produto deve corresponder ao apresentado na página de detalhes.
- O valor total do carrinho deve ser calculado corretamente.

---

# Critério de aprovação

O caso será considerado **Aprovado** quando o produto for incluído no carrinho com nome, cor, quantidade e preço correspondentes às opções selecionadas.

---

# Resultado da execução

**Status:** ✅ Aprovado

O produto foi adicionado corretamente ao carrinho, apresentando as informações selecionadas e o valor total calculado conforme esperado.

---

# Observações

- O fluxo principal de adição de uma unidade ao carrinho funcionou corretamente.
- A aplicação atualizou o contador do carrinho após a inclusão do produto.
- Comportamentos relacionados à seleção de determinadas cores foram avaliados separadamente nos relatórios de bugs.

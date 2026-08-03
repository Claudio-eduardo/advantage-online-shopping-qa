# CT-003 – Finalizar compra com dados válidos

---

# Objetivo

Validar que um usuário autenticado, com informações de entrega e método de pagamento válidos, consegue concluir o fluxo de compra com sucesso.

---

# Tipo de Teste

**Teste Funcional de ponta a ponta**

---

# Prioridade

**Alta**

### Justificativa

O checkout é o principal fluxo de negócio de uma aplicação de comércio eletrônico. Sua indisponibilidade impediria a conclusão das compras.

---

# Pré-condições

- Aplicação disponível.
- Usuário previamente cadastrado.
- Usuário autenticado.
- Informações válidas de entrega cadastradas.
- Produto disponível adicionado ao carrinho.
- Método de pagamento válido disponível.

---

# Massa de teste

| Campo | Valor |
|---|---|
| Usuário | Usuário válido e autenticado |
| Produto | Produto disponível em estoque |
| Quantidade | 1 unidade |
| Endereço | Dados completos e válidos |
| Método de pagamento | SafePay |

---

# Passos para execução

1. Acessar a aplicação.
2. Realizar login com uma conta válida.
3. Selecionar um produto disponível.
4. Adicionar o produto ao carrinho.
5. Acessar o carrinho de compras.
6. Confirmar os dados do produto e o valor total.
7. Clicar no botão **CHECKOUT**.
8. Conferir as informações de entrega.
9. Clicar em **NEXT**.
10. Selecionar o método de pagamento **SafePay**.
11. Informar as credenciais válidas do método de pagamento, quando solicitado.
12. Clicar em **PAY NOW**.
13. Aguardar a confirmação do pedido.

---

# Resultado esperado

- O sistema deve permitir o avanço entre todas as etapas do checkout.
- As informações de entrega devem ser apresentadas corretamente.
- O resumo do pedido deve exibir produto, quantidade e valores corretos.
- O pagamento deve ser processado.
- Uma mensagem de confirmação deve ser exibida.
- O sistema deve gerar um número de pedido e um número de rastreamento.
- O pedido deve ser registrado no histórico do usuário.

---

# Critério de aprovação

O caso será considerado **Aprovado** quando a compra for concluída, a confirmação for apresentada e o pedido for registrado com as informações correspondentes ao fluxo executado.

---

# Resultado da execução

**Status:** ✅ Aprovado

A aplicação permitiu concluir a compra e apresentou a confirmação, o número do pedido e o número de rastreamento.

---

# Observações

- O fluxo foi executado utilizando um usuário autenticado.
- O método de pagamento utilizado foi o **SafePay**.
- O pedido concluído foi registrado no histórico da conta.
- A ausência de validação de endereço em contas sem dados de entrega foi documentada separadamente no **BUG-005**.

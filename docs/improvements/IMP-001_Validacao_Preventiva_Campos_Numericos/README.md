# IMP-001 – Validação preventiva para campos numéricos

---

# Área da aplicação

Carrinho de Compras

---

# Descrição da melhoria

Adicionar validação em tempo real para todos os campos numéricos da aplicação, permitindo apenas números inteiros positivos.

A validação deve ocorrer durante a digitação, impedindo caracteres inválidos antes mesmo do envio da informação.

---

# Justificativa

Durante os testes foram identificados cenários onde valores inválidos podem comprometer cálculos internos da aplicação.

Uma validação preventiva reduz erros de entrada e evita inconsistências durante o processo de compra.

---

# Impacto esperado

- Redução de erros de entrada.
- Maior integridade dos dados.
- Melhor experiência do usuário.
- Menor necessidade de validações posteriores.

---

# Tipo de melhoria

Validação de Interface (Frontend)

# CT-005 – Aplicar filtro por fabricante

---

# Objetivo

Validar que o usuário consegue filtrar a listagem de produtos por fabricante utilizando a caixa de seleção correspondente.

---

# Tipo de Teste

**Teste Funcional e de Usabilidade**

---

# Prioridade

**Média**

### Justificativa

A filtragem facilita a localização de produtos, mas sua indisponibilidade não impede completamente a navegação ou a realização de uma compra.

---

# Pré-condições

- Aplicação disponível.
- Usuário em uma página de categoria.
- Categoria contendo produtos de mais de um fabricante.
- Painel lateral de filtros visível.

---

# Massa de teste

| Campo | Valor |
|---|---|
| Categoria | Speakers |
| Tipo de filtro | Manufacturer |
| Fabricante selecionado | Bose |

---

# Passos para execução

1. Acessar a aplicação **Advantage Online Shopping**.
2. Selecionar a categoria **Speakers**.
3. Localizar a seção **Manufacturer** no painel lateral.
4. Marcar diretamente a checkbox correspondente ao fabricante **Bose**.
5. Aguardar a atualização da listagem.
6. Verificar os produtos apresentados.

---

# Resultado esperado

- A checkbox do fabricante deve permanecer selecionada.
- A quantidade de produtos exibida deve ser atualizada.
- Apenas produtos do fabricante **Bose** devem permanecer na listagem.
- A interface não deve apresentar duplicações ou sobreposições.
- A opção **Clear** deve ficar disponível para remoção do filtro.

---

# Critério de aprovação

O caso será considerado **Aprovado** quando a aplicação apresentar somente produtos correspondentes ao fabricante selecionado, mantendo a interface estável.

---

# Resultado da execução

**Status:** ✅ Aprovado

Ao selecionar diretamente a checkbox do fabricante **Bose**, o filtro foi aplicado corretamente e apenas os produtos correspondentes permaneceram visíveis.

---

# Observações

- O teste foi aprovado quando a interação ocorreu diretamente pela checkbox.
- O clique no texto associado à opção do filtro apresentou comportamento diferente.
- A inconsistência relacionada ao clique no rótulo foi documentada separadamente no **BUG-004**.

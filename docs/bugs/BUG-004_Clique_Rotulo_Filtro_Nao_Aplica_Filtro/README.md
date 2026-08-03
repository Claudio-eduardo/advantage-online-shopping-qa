# BUG-004 – Clique no rótulo do filtro não aplica o filtro e provoca inconsistências temporárias na interface

---

# Resumo

Ao clicar no texto (rótulo) de uma opção de filtro na barra lateral, o sistema não aplica o filtro correspondente, embora o elemento indique ser clicável.

Durante essa interação, a interface apresenta temporariamente elementos duplicados, incluindo produtos e opções do painel de filtros, antes de retornar automaticamente ao estado original sem aplicar o filtro selecionado.

O comportamento foi reproduzido em diferentes categorias de produtos, indicando que o defeito não está restrito a uma única página da aplicação.

---

# Ambiente

- **Aplicação:** Advantage Online Shopping
- **Plataforma:** Web
- **Navegador:** Google Chrome

---

# Pré-condições

- Estar em uma página de listagem de produtos.
- Existirem filtros disponíveis na barra lateral.

---

# Passos para reprodução

1. Acessar uma categoria de produtos (ex.: Speakers).
2. Localizar qualquer filtro disponível na barra lateral.
3. Clicar no texto (rótulo) de uma opção do filtro, em vez da checkbox correspondente.
4. Observar o comportamento da interface.

---

# Resultado esperado

Ao clicar no texto de uma opção do filtro, o sistema deve executar a mesma ação realizada ao clicar na checkbox correspondente, aplicando corretamente o filtro selecionado sem apresentar inconsistências visuais.

---

# Resultado obtido

Ao clicar no texto de uma opção do filtro:

- o filtro não é aplicado;
- a listagem de produtos apresenta elementos duplicados temporariamente;
- o painel lateral também exibe opções sobrepostas durante a renderização;
- após alguns instantes, a interface retorna automaticamente ao estado original, sem aplicar o filtro selecionado.

Quando a seleção é realizada diretamente pela checkbox correspondente, o filtro funciona normalmente.

---

# Impacto

O comportamento compromete a experiência do usuário ao indicar que o rótulo do filtro é interativo, sem executar a ação esperada.

Além disso, durante o processamento da interação, a interface apresenta uma renderização inconsistente, podendo transmitir ao usuário a impressão de instabilidade da aplicação.

---

# Severidade

**Baixa**

### Justificativa

O defeito não impede a utilização da funcionalidade, pois o filtro continua funcionando corretamente quando selecionado pela checkbox. Entretanto, a interação com o rótulo provoca um comportamento incorreto da interface.

---

# Prioridade

**Média**

### Justificativa

O defeito é facilmente reproduzido durante uma funcionalidade utilizada com frequência e impacta diretamente a experiência do usuário, embora não comprometa as regras de negócio da aplicação.

---

# Evidências

## Figura 1 – Estado inicial da listagem

### Descrição

Categoria exibindo normalmente a listagem de produtos antes da interação com os filtros.

![Figura 1](figure-01-initial-product-list.png)

---

## Figura 2 – Clique no rótulo do filtro

### Descrição

O usuário seleciona o texto da opção do filtro em vez da checkbox correspondente.

![Figura 2](figure-02-filter-label-click.png)

---

## Figura 3 – Interface duplicada temporariamente

### Descrição

Após o clique, produtos e elementos do painel lateral são renderizados temporariamente em duplicidade antes de a página retornar automaticamente ao estado original.

![Figura 3](figure-03-temporary-ui-duplication.png)

---

## Figura 4 – Reprodução em outra categoria

### Descrição

O comportamento também foi reproduzido na categoria **Laptops**, demonstrando que o defeito não está restrito à categoria **Speakers**.

![Figura 4](figure-04-reproduced-in-laptops-category.png)

---

## Figura 5 – Funcionamento correto pela checkbox

### Descrição

Ao selecionar a mesma opção utilizando a checkbox correspondente, o filtro é aplicado corretamente e a interface permanece consistente.

![Figura 5](figure-05-checkbox-filter-working-correctly.png)

---

# Observações

- O comportamento foi reproduzido diversas vezes durante os testes.
- O cursor do mouse é exibido no formato de **mão**, indicando que o texto da opção do filtro aparenta ser um elemento clicável.
- O defeito foi reproduzido nas categorias **Speakers** e **Laptops**.
- O problema ocorre apenas ao clicar no texto da opção do filtro.
- Ao selecionar a checkbox correspondente, o filtro é aplicado normalmente.
- Durante a ocorrência, produtos e elementos do painel lateral são renderizados temporariamente em duplicidade antes de a interface retornar ao estado original.
- A interface retorna automaticamente ao estado inicial, sem necessidade de interação adicional do usuário.

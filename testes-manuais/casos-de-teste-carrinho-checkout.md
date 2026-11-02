# Casos de Teste — Carrinho e Checkout

**Aplicação:** SauceDemo  
**Tipo de teste:** Testes funcionais manuais  
**Usuário utilizado:** standard_user

## TC-04 — Adicionar produto ao carrinho

**Pré-condição:** Usuário autenticado na aplicação.

**Passos:**
1. Localizar o produto Sauce Labs Backpack.
2. Clicar em Add to cart.

**Resultado esperado:** Produto adicionado ao carrinho e contador atualizado.

**Resultado obtido:** Botão alterado para Remove e contador atualizado para 1.

**Status:** Passou.

## TC-05 — Remover produto pela página de produtos

**Pré-condição:** Produto adicionado ao carrinho.

**Passos:**
1. Localizar o produto adicionado.
2. Clicar em Remove.

**Resultado esperado:** Produto removido e contador atualizado.

**Resultado obtido:** Produto removido e contador voltou a ficar vazio.

**Status:** Passou.

## TC-06 — Visualizar produto no carrinho

**Pré-condição:** Produto adicionado ao carrinho.

**Passos:**
1. Clicar no ícone do carrinho.
2. Conferir as informações do produto.

**Resultado esperado:** Exibir nome, preço e quantidade corretos.

**Resultado obtido:** Produto, preço e quantidade 1 exibidos corretamente.

**Status:** Passou.

## TC-07 — Remover produto pela página do carrinho

**Pré-condição:** Produto presente no carrinho.

**Passos:**
1. Acessar o carrinho.
2. Clicar em Remove.

**Resultado esperado:** Produto removido da lista.

**Resultado obtido:** Remoção realizada corretamente.

**Status:** Passou.

## TC-08 — Visualizar carrinho vazio

**Pré-condição:** Carrinho sem produtos.

**Passos:**
1. Acessar a página do carrinho.
2. Verificar a lista de produtos.

**Resultado esperado:** Nenhum produto listado e contador sem quantidade.

**Resultado obtido:** Carrinho exibido sem produtos e contador vazio.

**Status:** Passou.
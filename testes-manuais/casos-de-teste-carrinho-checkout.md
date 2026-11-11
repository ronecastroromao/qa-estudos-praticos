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

## **TC-09 — Realizar compra válida de um produto**

**Pré-condição:** Usuário autenticado com `standard_user` e carrinho inicialmente vazio.

**Passos:**
1. Acessar a página Products.
2. Adicionar o produto Sauce Labs Backpack ao carrinho.
3. Acessar o carrinho e conferir o produto.
4. Clicar em Checkout.
5. Preencher First Name, Last Name e Zip/Postal Code.
6. Clicar em Continue.
7. Conferir o produto, quantidade e valores na página Checkout: Overview.
8. Clicar em Finish.

**Resultado esperado:** Compra finalizada com sucesso, exibindo a mensagem "Thank you for your order!".

**Resultado obtido:** Sistema exibiu a mensagem "Thank you for your order!" e confirmou que o pedido foi despachado.

**Evidência:** `evidencias/TC-09-compra-valida.png`

**Status:** Passou.

## **TC-10 — Validar campos obrigatórios do checkout**

**Pré-condição:** Usuário autenticado e produto adicionado ao carrinho.

**Passos:**
1. Acessar o carrinho e clicar em Checkout.
2. Na página Your Information, deixar todos os campos vazios e clicar em Continue.
3. Preencher First Name com `Rone`, deixar os demais campos vazios e clicar em Continue.
4. Preencher Last Name com `Castro`, deixar Zip/Postal Code vazio e clicar em Continue.
5. Preencher Zip/Postal Code com `08000-000` e clicar em Continue.

**Resultado esperado:** O sistema deve impedir o avanço enquanto houver campos obrigatórios vazios, apresentar a mensagem correspondente ao campo pendente e permitir continuar após o preenchimento de todos os campos.

**Resultado obtido:**
- Primeiro teste: `Error: First Name is required`.
- Segundo teste: `Error: Last Name is required`.
- Terceiro teste: `Error: Postal Code is required`.
- Após preencher os três campos, o sistema avançou para Checkout: Overview.

**Evidências:**
- `evidencias/TC-10-01-first-name-obrigatorio.png`
- `evidencias/TC-10-02-last-name-obrigatorio.png`
- `evidencias/TC-10-03-postal-code-obrigatorio.png`

**Status:** Passou.

## **TC-11 — Verificar validação do formato do código postal**

**Pré-condição:** Usuário autenticado e produto adicionado ao carrinho.

**Passos:**
1. Acessar o carrinho e clicar em Checkout.
2. Preencher First Name com `Rone` e Last Name com `Castro`.
3. Informar `ABC` no campo Zip/Postal Code.
4. Clicar em Continue e observar o resultado.
5. Repetir o teste utilizando `@@@` no campo Zip/Postal Code.
6. Clicar em Continue e observar o resultado.

**Resultado esperado:** O sistema deve validar o formato do código postal conforme a regra de negócio definida para o campo, impedindo valores em formato inválido.

**Resultado obtido:**
- Com `ABC`, o sistema permitiu avançar para Checkout: Overview.
- Com `@@@`, o sistema também permitiu avançar para Checkout: Overview.

**Evidências:**
- `evidencias/TC-11-01-cep-letras-aceito.png`
- `evidencias/TC-11-02-cep-caracteres-especiais-aceito.png`

**Status:** Comportamento observado — possível falha de validação, pendente de confirmação dos requisitos de formato do código postal.

## **TC-12 — Tentar finalizar compra com carrinho vazio**

**Pré-condição:** Usuário autenticado com `standard_user` e carrinho sem produtos.

**Passos:**
1. Acessar a página do carrinho vazio.
2. Clicar em Checkout.
3. Preencher First Name, Last Name e Zip/Postal Code.
4. Clicar em Continue.
5. Conferir o resumo do pedido.
6. Clicar em Finish.

**Resultado esperado:** A definir conforme a regra de negócio. Caso compras sem produtos não sejam permitidas, o sistema deverá impedir a finalização.

**Resultado obtido:**
- O sistema permitiu acessar Your Information com o carrinho vazio.
- Permitiu avançar para Checkout: Overview.
- Nenhum produto foi listado.
- Item total: US$ 0,00.
- Tax: US$ 0,00.
- Total: US$ 0,00.
- A compra foi finalizada com a mensagem "Thank you for your order!".

**Evidências:**
- `evidencias/TC-12-checkout-carrinho-vazio.png`
- `evidencias/TC-12-compra-finalizada-carrinho-vazio.png`

**Status:** Comportamento observado — possível falha de regra de negócio, pendente de confirmação dos requisitos.

## **TC-13 — Cancelar checkout e preservar produto no carrinho**

**Pré-condição:** Usuário autenticado com `standard_user` e Sauce Labs Backpack adicionado ao carrinho.

**Passos:**
1. Acessar o carrinho.
2. Clicar em Checkout.
3. Na página Your Information, clicar em Cancel.
4. Verificar a página apresentada e os produtos no carrinho.

**Resultado esperado:** O sistema deve retornar à página do carrinho, preservando o produto adicionado anteriormente.

**Resultado obtido:** O sistema retornou à página do carrinho e manteve o Sauce Labs Backpack no carrinho.

**Evidência:** `evidencias/TC-13-checkout-cancelado-produto-preservado.png`

**Status:** Passou.

# Relatório de Bug — BUG-02

## Finalização de compra com carrinho vazio

**Aplicação:** SauceDemo  
**Usuário utilizado:** standard_user  
**Funcionalidade:** Checkout  
**Tipo de teste:** Teste funcional exploratório  
**Status:** Defeito identificado — aguardando documentação final

### Pré-condições
- Acessar a aplicação SauceDemo.
- Realizar login com `standard_user`.
- Manter o carrinho vazio.

### Passos para reprodução
1. Acessar https://www.saucedemo.com/.
2. Realizar login com `standard_user` e senha `secret_sauce`.
3. Acessar o carrinho sem adicionar produtos.
4. Clicar em Checkout.
5. Preencher First Name, Last Name e Postal Code.
6. Clicar em Continue.
7. Na tela Checkout: Overview, clicar em Finish.

### Resultado esperado
A aplicação deve impedir a finalização de uma compra quando o carrinho estiver vazio.

### Resultado obtido
A aplicação permitiu concluir o checkout sem produtos no carrinho, exibindo a mensagem "Thank you for your order!" e valor total de $0.00.

### Evidência
[Evidência: BUG-02 — Checkout sem produtos](evidencias/BUG-02-checkout-sem-produtos.png)

# Relatório de Bugs

Este documento reúne os defeitos identificados durante os testes exploratórios da aplicação SauceDemo.

---

## BUG-01 — Imagens dos produtos não correspondem aos produtos apresentados

**Aplicação:** SauceDemo  
**Usuário utilizado:** problem_user  
**Funcionalidade:** Listagem de produtos  
**Tipo de teste:** Teste exploratório  
**Status:** Identificado

### Pré-condições
- Acessar a aplicação SauceDemo.
- Realizar login com o usuário `problem_user`.
- Acessar a página de produtos.

### Passos para reprodução
1. Acessar https://www.saucedemo.com/.
2. Informar o usuário `problem_user`.
3. Informar a senha `secret_sauce`.
4. Clicar em Login.
5. Observar as imagens e os nomes dos produtos na listagem.

### Resultado esperado
Cada produto deve apresentar uma imagem correspondente ao seu nome e descrição.

### Resultado obtido
Foram observadas imagens repetidas que não correspondem aos produtos apresentados na listagem, inclusive nos produtos localizados mais abaixo na página.

### Evidência

[Evidência: BUG-01 - Imagens dos produtos](evidencias/BUG-01-imagens-produtos-problem-user.png)

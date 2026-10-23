# Casos de Teste — Login do SauceDemo

## 1. Objetivo

Validar o comportamento da funcionalidade de login, verificando se a aplicação permite o acesso com credenciais válidas e rejeita entradas inválidas.

## 2. Aplicação sob teste

- **Aplicação:** SauceDemo
- **URL:** https://www.saucedemo.com/
- **Tipo de teste:** Teste funcional manual
- **Funcionalidade:** Login
- **Ambiente:** Navegador Google Chrome

## 3. Pré-condições

- A aplicação deve estar acessível.
- O usuário deve estar na página de login.
- Devem ser utilizadas as credenciais públicas disponibilizadas para a prática.

## 4. Casos de teste

### TC-01 — Login com credenciais válidas

**Objetivo:** verificar se um usuário válido consegue acessar a aplicação.

**Passos para execução:**
1. Acessar https://www.saucedemo.com/.
2. Preencher o campo Username com `standard_user`.
3. Preencher o campo Password com `secret_sauce`.
4. Clicar no botão Login.

**Resultado esperado:** o login deve ser realizado com sucesso e a página de produtos deve ser exibida.

**Resultado obtido:** Pendente de execução.

**Status:** Não executado.

---

### TC-02 — Login com senha inválida

**Objetivo:** verificar se a aplicação rejeita uma senha incorreta.

**Passos para execução:**
1. Acessar a página de login.
2. Preencher o campo Username com `standard_user`.
3. Preencher o campo Password com uma senha incorreta, como `senha_errada_123`.
4. Clicar no botão Login.

**Resultado esperado:** o acesso deve ser negado e uma mensagem de erro deve ser exibida.

**Resultado obtido:** Pendente de execução.

**Status:** Não executado.

---

### TC-03 — Login sem preencher o usuário

**Objetivo:** verificar a validação do campo Username obrigatório.

**Passos para execução:**
1. Acessar a página de login.
2. Deixar o campo Username vazio.
3. Preencher o campo Password com `secret_sauce`.
4. Clicar no botão Login.

**Resultado esperado:** o acesso não deve ser realizado e a aplicação deve informar que o usuário é obrigatório.

**Resultado obtido:** Pendente de execução.

**Status:** Não executado.

---

## 5. Observações da execução

Os resultados serão preenchidos após a execução de cada caso de teste. Eventuais diferenças entre o resultado esperado e o obtido serão analisadas antes de serem classificadas como defeitos.

## 6. Histórico de atualização

- **Versão inicial:** criação dos casos de teste para a funcionalidade de login.
- **Próxima atualização:** registro dos resultados reais, status e evidências da execução.

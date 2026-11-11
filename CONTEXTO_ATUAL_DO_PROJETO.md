# CONTEXTO ATUAL — ESTUDO PORTFÓLIO QA

**Última atualização:** 09/11/2026  
**Projeto:** Estudo Portfólio QA  
**Responsável pelo aprendizado e execução:** Usuário  
**Repositório:** https://github.com/ronecastroromao/qa-estudos-praticos

## 1. Objetivo

Construir um portfólio público e profissional de QA para conquistar a primeira oportunidade como QA Júnior, QA Tester ou Estagiário de Testes.

O projeto é desenvolvido com aprendizado prático, começando por testes manuais e evoluindo posteriormente para testes de API e automação.

O assistente deve acompanhar o usuário como tutor, respeitando seu nível de conhecimento e seu ritmo.

## 2. Ambiente de trabalho

- Sistema operacional: Windows.
- Editor: Visual Studio Code.
- Navegador: Google Chrome.
- Controle de versão: Git.
- Repositório remoto: GitHub.
- Plataforma de testes atual: SauceDemo.
- URL: https://www.saucedemo.com/

O usuário também utiliza o GPT-OSS 120B pelo Antigravity dentro do VS Code para continuar os estudos.

## 3. Estrutura conhecida do repositório

```text
qa-estudos-praticos/
├── README.md
├── AGENTS.md
├── CONTEXTO_ATUAL_DO_PROJETO.md
└── testes-manuais/
    ├── evidencias/
    │   ├── TC-01-login-valido.png
    │   ├── TC-02-senha-invalida.png
    │   ├── TC-03-usuario-nao-informado.png
    │   ├── BUG-01-imagens-produtos-problem-user.png
    │   └── BUG-02-checkout-sem-produtos.png
    ├── casos-de-teste-login.md
    ├── casos-de-teste-carrinho-checkout.md
    ├── relatorio-de-bugs.md
    └── relatorio-bug-02.md
```

Essa é a estrutura conhecida. Antes de criar novos arquivos, consulte a estrutura real do repositório.

## 4. Trabalho já realizado

### 4.1 Testes de login

Arquivo: `testes-manuais/casos-de-teste-login.md`

Casos documentados:

- TC-01 — Login válido.
- TC-02 — Senha inválida.
- TC-03 — Usuário não informado.

Os três testes foram executados e possuem evidências registradas.

### 4.2 Bug de imagens dos produtos

Arquivo: `testes-manuais/relatorio-de-bugs.md`

Usuário de teste: `problem_user`.

Foi observado que imagens dos produtos não correspondiam corretamente aos respectivos nomes.

Existe evidência publicada em:

`testes-manuais/evidencias/BUG-01-imagens-produtos-problem-user.png`

### 4.3 Checkout sem produtos

Arquivo: `testes-manuais/relatorio-bug-02.md`

Foi observado que o sistema permitiu finalizar um checkout com o carrinho vazio, apresentando total de $0.00 e exibindo uma mensagem de compra concluída.

Existe evidência publicada em:

`testes-manuais/evidencias/BUG-02-checkout-sem-produtos.png`

Atenção: a expectativa de impedir checkout vazio precisa ser validada contra os requisitos da aplicação. Não classificar definitivamente como defeito confirmado sem essa validação.

### 4.4 Testes de carrinho

Arquivo: `testes-manuais/casos-de-teste-carrinho-checkout.md`

Casos executados:

- TC-04 — Adicionar produto ao carrinho.
- TC-05 — Remover produto pela página de produtos.
- TC-06 — Visualizar produto no carrinho.
- TC-07 — Remover produto pelo carrinho.
- TC-08 — Visualizar carrinho vazio.

O usuário relatou resultados satisfatórios nos cinco cenários. Não presumir que existam capturas de tela desses testes.

## 5. Organização e publicação

O README principal contém links para os documentos de testes e relatórios.

O usuário já praticou:

- `git pull origin main`
- `git status`
- `git add`
- `git commit`
- `git push`
- `git pull --rebase origin main`

Antes de iniciar alterações, sincronizar o projeto e verificar o estado do Git.

Não realizar commit ou push sem autorização expressa.

## 6. Atividade em andamento — Compra válida

Plataforma: SauceDemo.

Usuário de teste:

`standard_user`

Senha:

`secret_sauce`

Produto selecionado:

`Sauce Labs Backpack`

### Etapas já executadas nesta sessão

1. Projeto sincronizado com `git pull origin main`.
2. Estado do Git conferido com `git status`.
3. Usuário acessou o SauceDemo e realizou login.
4. Produto Sauce Labs Backpack adicionado ao carrinho.
5. Carrinho aberto e produto conferido.
6. Checkout iniciado.
7. Dados preenchidos:
   - First Name: Rone
   - Last Name: Castro
   - Zip/Postal Code: 08000-000
8. O usuário recebeu a orientação para clicar em Continue e chegar à página Checkout: Overview.

### Ponto exato de parada

**Aguardar confirmação do usuário de que chegou à página Checkout: Overview.**

Não presumir que essa etapa foi concluída.

Quando o usuário confirmar, orientar a conferência dos seguintes itens:

- Produto correto.
- Quantidade.
- Preço.
- Item total.
- Tax.
- Total.

Depois, orientar a finalização com Finish e solicitar que informe a mensagem apresentada pelo sistema.

O objetivo é concluir um fluxo de compra válido e documentá-lo como novo caso de teste, usando somente os resultados realmente observados.

## 7. Próximas atividades do portfólio

Após concluir o fluxo de compra:

1. Documentar o caso de teste de compra válida.
2. Executar testes de ordenação dos produtos.
3. Executar testes de detalhes dos produtos.
4. Avaliar cenários adicionais relevantes.
5. Preparar um relatório geral de execução do projeto SauceDemo.
6. Revisar a apresentação do GitHub.

Não transformar o SauceDemo em um projeto interminável. A meta é produzir uma primeira versão consistente e apresentável.

## 8. Evolução futura

Depois da primeira versão do projeto manual:

1. Aprender testes de API com Postman.
2. Estudar HTTP e JSON.
3. Desenvolver fundamentos de SQL.
4. Estudar JavaScript aplicado a testes.
5. Evoluir para automação com Playwright.

Os casos manuais existentes poderão servir como base para exercícios de automação.

## 9. Estratégia profissional

O usuário está buscando sua primeira oportunidade na área.

Cargos de interesse:

- QA Tester Júnior.
- Analista de Testes Júnior.
- Estágio em QA.
- Tester Manual.
- Assistente de Qualidade de Software.

A busca por vagas deve acontecer em paralelo aos estudos, sem esperar dominar todas as tecnologias.

Não inventar experiência profissional nem apresentar estudos como experiência de trabalho.

## 10. Instrução para a próxima sessão

Ao abrir uma nova conversa no Antigravity:

1. Ler `AGENTS.md`.
2. Ler este documento.
3. Conferir a estrutura real do projeto.
4. Consultar os documentos de testes quando necessário.
5. Identificar o ponto exato de parada.
6. Continuar pela próxima etapa pendente.

Não reiniciar testes já executados sem motivo.

Não repetir perguntas cujas respostas já estejam documentadas.

Trabalhar uma etapa por vez e aceitar "feito" para comandos simples.

Vamos continuar o projeto Estudo Portfólio QA.

Leia o AGENTS.md, o CONTEXTO_ATUAL_DO_PROJETO.md e o README.md antes de responder.

Identifique o progresso, a última etapa concluída e a próxima atividade pendente.

Respeite as instruções do AGENTS.md. Não repita atividades concluídas. Trabalhe uma etapa por vez e aguarde minha confirmação.
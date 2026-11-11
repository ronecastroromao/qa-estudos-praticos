---
name: encerrar-sessao
description: Registra automaticamente a continuidade do projeto Estudo Portfólio QA ao encerrar ou pausar uma sessão, atualizando o contexto atual com atividades concluídas, resultados reais e próxima etapa pendente.
---

# Skill — Encerrar sessão do Estudo Portfólio QA

## Objetivo

Atualizar o arquivo `CONTEXTO_ATUAL_DO_PROJETO.md` para que o usuário possa retomar os estudos em outra conversa ou sessão sem precisar reconstruir o histórico.

## Quando executar

Execute este procedimento quando o usuário:
- Solicitar o encerramento da sessão.
- Dizer que vai parar ou pausar os estudos.
- Solicitar a atualização da memória ou continuidade do projeto.
- Invocar `/encerrar-sessao`.

## Autorização

O usuário autoriza previamente a atualização do arquivo `CONTEXTO_ATUAL_DO_PROJETO.md` sempre que solicitar o encerramento ou invocar esta Skill.

Não solicite uma nova autorização para essa atualização específica.

Essa autorização não permite:
- Fazer commit ou push.
- Alterar outros documentos.
- Apagar arquivos.
- Modificar resultados de testes já registrados sem justificativa.
- Executar outras alterações no projeto.

## Procedimento obrigatório

### 1. Consultar o histórico

Analise a conversa atual e consulte o conteúdo existente de `CONTEXTO_ATUAL_DO_PROJETO.md`.

Considere somente informações efetivamente confirmadas pelo usuário ou verificadas nos arquivos.

### 2. Identificar o progresso

Registre:

- Data da atualização.
- Projeto e objetivo atual.
- Atividades concluídas.
- Testes executados e respectivos resultados observados.
- Evidências realmente existentes.
- Arquivos criados ou modificados.
- Etapa atualmente em andamento.
- Última ação efetivamente concluída.
- Próxima ação pendente.
- Problemas ou dúvidas ainda não resolvidos.

### 3. Preservar a precisão

- Não invente resultados.
- Não transforme resultados esperados em resultados obtidos.
- Não afirme que um teste passou sem confirmação.
- Não registre uma ação como concluída apenas porque foi sugerida.
- Preserve informações importantes do histórico anterior.
- Não elimine etapas futuras já planejadas sem justificativa.

### 4. Atualizar o documento

Atualize diretamente `CONTEXTO_ATUAL_DO_PROJETO.md`, preservando o histórico relevante.

Evite simplesmente acrescentar informações duplicadas no final.

Organize o conteúdo para que outro assistente consiga entender rapidamente o estado atual e continuar o trabalho.

### 5. Salvar e verificar

- Salve o arquivo no VS Code.
- Verifique se a alteração foi aplicada.
- Não faça commit nem push.
- Não altere outros arquivos.

Se não conseguir salvar ou verificar a atualização, informe claramente o problema. Nunca declare que salvou se isso não foi confirmado.

### 6. Resumo ao usuário

Ao terminar, apresente um resumo curto com:

1. O que foi registrado.
2. Qual foi a última etapa concluída.
3. Qual é o próximo passo.
4. Confirmação de que o arquivo foi salvo, somente se realmente foi verificado.

## Regra principal

A finalidade é permitir continuidade real entre sessões e modelos de IA, mantendo o histórico do projeto atualizado sem exigir que o usuário reescreva manualmente o progresso.
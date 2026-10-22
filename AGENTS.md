<!-- brain:inicio -->
<!-- Bloco gerado por comercial-rgb/brain (scripts/propagate.py). NÃO edite à mão: edite rules/rules.yaml ou graph.yaml no cérebro e rode o script. Tudo fora dos marcadores brain:inicio/brain:fim é seu e é preservado. -->

# Cérebro — licitagestao-app
_Gerado em 2026-10-22. Fonte da verdade: https://github.com/comercial-rgb/brain_

## O que é esta repo
Só hospeda os instaladores (GitHub Releases) do LicitaGestão Desktop; electron-updater lê /releases/latest daqui.

## Como roda e deploya
- Stack: nenhum (README + Releases)
- Deploy: GitHub Releases

## Regras globais (valem em TODAS as repos)
- **R-001 — Nunca imprimir ou versionar segredos**: Token, chave, senha e certificado nunca aparecem em chat, log, argumento de shell, código, fixture, commit ou documento. Segredos vivem só em ambiente (.env ignorado, Figaro, painel do provedor); arquivos de exemplo trazem apenas os NOMES das variáveis.
- **R-059 — Autorização no servidor, nunca na tela**: Permissão é conferida na rota/caso de uso por ação nomeada; esconder botão ou item de menu não é controle de acesso. Identidade vem da sessão ou do token, nunca de cabeçalho, URL ou campo de formulário escolhido pelo cliente. Na dúvida, fail-closed.
- **R-074 — Não afrouxar teste para ficar verde**: Nunca aumentar timeout, apagar teste, usar skip, reduzir asserção, mudar valor esperado, afrouxar grant ou alterar condição comercial para um teste passar. Teste que deixou de valer é reescrito com o motivo.
- **R-093 — Evidência real, nunca "should work"**: Toda entrega termina com comando executado, saída real e o que não foi testado. HTTP 200, runner, PR ou commit não provam percurso de navegador; OTA publicada não prova execução no aparelho; "resolvido" só com prova em produção. Passo pulado é passo que não aconteceu.

## Regras específicas de licitagestao-app
- (nenhuma ainda)

## Cadeia de dependências — leia ANTES de mudar contratos
DEPENDEM desta repo (quebram se o contrato mudar):
- `licitagestao` via **release** — desktop-release.yml publica instalador em comercial-rgb/licitagestao-app (secret RELEASE_TOKEN); electron-updater lê /releases/latest (evidência: desktop-app/package.json; .github/workflows/desktop-release.yml)

Se a mudança tocar um contrato listado acima (rota, payload, tabela, evento, variável de ambiente compartilhada): (1) rode `python3 scripts/chain.py licitagestao-app` no cérebro, (2) abra a mudança também na(s) repo(s) afetada(s), (3) registre a decisão em brain/journal/.

## Ao terminar qualquer tarefa
- Se criou ou mudou uma regra, ela vai para brain/rules/rules.yaml (não só aqui).
- Se criou ou mudou uma dependência entre repos, ela vai para brain/graph.yaml.
- Registre o que foi feito em brain/journal/<ano-mês>.md (1-3 linhas: repo, o quê, PR/commit).

<!-- brain:fim -->

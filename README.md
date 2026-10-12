# Vitor Bastos

Agentic Software Development Engineer na Space Needle. Full stack em TypeScript (Node.js e React), com agentes de código no centro do fluxo e responsabilidade pelo que vai para produção.

## Produtos

### [RetroTrack](https://retrotrack.com.br)

Catálogo e valoração de jogos retrô. O preço sai de um LLM na Azure com grounding de busca web, e cada chamada de IA vira um evento num ledger append-only, com etapa, tokens e custo. React, Express e MongoDB.

<a href="https://www.retrotrack.com.br/collectors/vbss-io"><img src="https://www.retrotrack.com.br/collectors/vbss-io/card.svg?theme=dark" alt="Minha coleção no RetroTrack" width="540"></a>

### [Imaginaria](https://imaginaria.vbss.io)

Estúdio de imagem e vídeo sobre vários provedores (OpenAI, Google, xAI, fal e Replicate, via AI SDK). Um roteador com LLM lê o pedido e devolve modelo e parâmetros em saída estruturada, com fallback quando a resposta não fecha.

<a href="https://www.imaginaria.vbss.io/creator/vbss.io"><img src="https://www.imaginaria.vbss.io/creator/vbss.io/card.svg" alt="Meu estúdio na Imaginaria" width="540"></a>

## Open Source

- **[vbss-cchub](https://github.com/vbss-io/vbss-cchub)**: hub local para vários agentes de código. Claude Code e Codex se conectam por um servidor MCP próprio, delegam tarefas que rodam em git worktrees isoladas e o hub faz o merge. Tauri, Express, SQLite e SSE.
- **[vbss-ui](https://github.com/vbss-io/vbss-ui)** e **[vbss-translator](https://github.com/vbss-io/vbss-translator)**: bibliotecas React publicadas no npm e usadas nos meus produtos.
- **[vbss-mcps](https://github.com/vbss-io/vbss-mcps)**: servidores MCP readonly para MongoDB, MySQL, Postgres e Azure.

## Como eu trabalho

- Clean Architecture com ports and adapters: casos de uso isolados, injeção de dependência por registry e as fronteiras entre camadas checadas no lint.
- Zod nas bordas, testes primeiro onde a regra de negócio importa, cobertura mínima nos pacotes compartilhados.
- CI como portão: nenhum deploy sai se auditoria de dependências, lint, typecheck ou testes falharem.
- Agentes com contrato: um planeja, outros executam em worktrees separadas e um verificador confere o resultado sem ver o raciocínio de quem executou. A decisão de arquitetura continua comigo.
- Custo de IA medido por chamada, não estimado.

## Stack

- **Linguagens:** TypeScript, JavaScript, C#
- **Back-end:** Node.js, Express, Zod, MongoDB, PostgreSQL
- **Front-end:** React, Vite, Next.js, Vue
- **IA:** AI SDK, OpenAI, Anthropic, Azure OpenAI, MCP, RAG
- **Infra:** Docker, Kubernetes, Azure, AWS, Bicep, GitHub Actions

[vbss.io](https://vbss.io) · [LinkedIn](https://www.linkedin.com/in/vbss-io) · [vitor@vbss.io](mailto:vitor@vbss.io)

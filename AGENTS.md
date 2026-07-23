# AGENTS.md — Instruções para Agentes (leitura obrigatória)

> 🛑 **LEITURA OBRIGATÓRIA ANTES DE QUALQUER ALTERAÇÃO.**
> Este repositório é governado pela **[POP 000](./POP-000.md)**. Leia-a por completo antes de criar branch, editar arquivos ou abrir Pull Request.

Vale para qualquer agente automatizado (Claude, Grok, GitHub Copilot, etc.) e para colaboradores humanos.

## O que você NÃO pode quebrar

- **Fonte do GitHub Pages = "GitHub Actions"** — não altere em *Settings → Pages* (trocar para "Deploy from a branch" tira o site do ar).
- **Não remova nem renomeie** `.github/workflows/deploy-pages.yml` (é o que publica o site a cada push no `main`).
- **Não remova** `.nojekyll`.
- **Não commite direto no `main`** — use branch + Pull Request.
- **Não mexa em Settings** (Pages, branches, secrets, colaboradores) sem autorização explícita e por escrito do responsável.

## Obrigatório em todo Pull Request

Inclua no corpo do PR, por escrito:

> ✅ Declaro, por escrito, ter lido e seguido a POP 000 deste repositório. — _\<seu nome/identificação\>_

Regras e detalhes completos: **[POP-000.md](./POP-000.md)**.

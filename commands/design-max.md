---
description: Modo design máximo — orquestra todo o arsenal de design (skills + plugins + web-builder) em fases
---

Você está em MODO DESIGN MÁXIMO para a seguinte tarefa: $ARGUMENTS

Execute as 5 fases abaixo em ordem, rastreando cada uma com TodoWrite. Em cada fase, carregue APENAS as skills da rota que se aplica — nunca todas.

## Fase 1 — Briefing

- Identifique: tipo de entrega (landing page / site / e-commerce / dashboard / app mobile / componente / deck / poster / brand kit / redesign), público, objetivo de conversão e stack. Stack não informada → a mais simples que atenda (HTML/CSS/JS para estático; React/Next.js com interatividade real).
- Pedido vago em algo que muda o design (público, tom, marca) → no máximo 3 perguntas via AskUserQuestion. Claro → siga direto.
- Projeto estratégico/maior → opcionalmente `ux-strategy:design-brief` para formalizar o brief.

## Fase 2 — Expertise (via ferramenta Skill)

**Núcleo (sempre):**
1. `ui-ux-pro-max` — escolher estilo, paleta (hex) e fontes para ESTE projeto.
2. `impeccable` — princípios de craft e anti-padrões.

**Rota por tipo de entrega (escolha 1):**
- Landing page / site de marketing / e-commerce → `frontend-design:frontend-design`
- Dashboard / admin / app / ferramenta interativa → `interface-design`
- Deck / poster / protótipo clicável / storyboard / exploração visual / trabalho para marca existente → `claude-design` (Core Asset Protocol; briefing vago → ofereça as 3 direções)
- Identidade visual / brand guidelines → `brandkit`

**Direção estética (no máximo 1, se fizer sentido):**
- Inferir do briefing → `taste-skill` | agência high-end → `soft-skill` | minimalista editorial → `minimalist-skill` | brutalist/terminal → `brutalist-skill`

**Condicionais de stack:**
- Tailwind → `baseline-ui`
- Animações/micro-interações planejadas → `emil-design-eng`

Feche a fase com um **design brief** (5–8 linhas): estilo, paleta em hex, fontes, tom de copy e 1 elemento de assinatura distintivo. Em código de UI, aplique sempre tipografia profissional (aspas curvas, travessões, hierarquia — plugin `typography`).

## Fase 3 — Execução

- **Criação completa** (site/LP/e-commerce) → delegue ao subagente `web-builder` via Agent, com o design brief no prompt como contrato obrigatório.
- **Redesign de algo existente** → primeiro `design-audit` (plano faseado de refinamento visual), depois `redesign-skill` para executar sem quebrar funcionalidade.
- **Melhoria pontual** ("deixa mais bonito", CSS, componente) → `ui-refactor` (ou os atalhos /fix-hierarchy, /fix-layout, /fix-typography, /fix-colors).
- **Referência visual antes do código** (quando o usuário quer ver direção antes) → `imagegen-frontend-web` (web, 1 imagem por seção) ou `imagegen-frontend-mobile` (telas de app); para implementar fiel à imagem → `image-to-code-skill`.
- Em qualquer rota: o elemento de assinatura do brief deve estar no resultado; nada de design genérico. Código completo, sem placeholders.

## Fase 4 — Auditoria (sobre o resultado pronto)

- Sempre: `fixing-accessibility` (WCAG, ARIA, teclado, contraste).
- Página completa com `<head>` → `fixing-metadata` (SEO, OG, favicon, JSON-LD).
- Há animações → `fixing-motion-performance` (compositor-only, layout thrash).
- Fluxos interativos, formulários ou navegação complexa → `ux-heuristics` (Nielsen, severidade).
- Corrija todos os achados. Se possível, renderize (preview/screenshot) e ajuste o que estiver visualmente quebrado antes de entregar.

## Fase 5 — Entrega

Relatório curto:
1. Design brief aplicado (estilo, paleta, fontes, assinatura).
2. Rotas/skills usadas e por quê.
3. Auditorias: encontrado → corrigido.
4. Como rodar/ver o resultado.

Se o resultado vai para um dev/equipe, ofereça gerar spec de handoff (`design:design-handoff` ou `/handoff`).

# design-max

Arsenal completo de design para Claude Code: o comando `/design-max` orquestra 22 skills de UI/UX e o agente `web-builder` em um fluxo de 5 fases — briefing, design brief, execução, auditoria e entrega.

## Instalação

```bash
claude plugin marketplace add SEU-USUARIO/design-max-plugin
claude plugin install design-max@design-max-plugin
```

Reinicie a sessão do Claude Code e use:

```
/design-max crie uma landing page para uma cafeteria artesanal
```

## O que vem no pacote

### Comandos
| Comando | Função |
|---|---|
| `/design-max` | Orquestrador completo em 5 fases |
| `/ui-refactor` | Refactor de UI (princípios Refactoring UI) |
| `/fix-hierarchy` `/fix-layout` `/fix-typography` `/fix-colors` | Correções cirúrgicas por categoria |

### Skills (22)
- **Inteligência de design**: `ui-ux-pro-max` (67 estilos, 96 paletas, 57 pares de fontes), `impeccable`, `claude-design`
- **Por tipo de projeto**: `interface-design` (apps/dashboards), `brandkit` (identidade visual)
- **Direção estética**: `taste-skill`, `soft-skill`, `minimalist-skill`, `brutalist-skill`
- **Redesign e melhoria**: `redesign-skill`, `ui-refactor`
- **Imagens de referência**: `imagegen-frontend-web`, `imagegen-frontend-mobile`, `image-to-code-skill`
- **Qualidade de código de UI**: `baseline-ui` (Tailwind), `emil-design-eng` (animação)
- **Auditorias**: `fixing-accessibility`, `fixing-metadata`, `fixing-motion-performance`, `ux-heuristics`
- **Utilitárias**: `output-skill`, `stitch-skill`

### Agentes
- `web-builder` — especialista em criar sites, LPs e e-commerce. **Atenção**: referencia uma base local de PDFs de UX/UI e scripts que não vêm no pacote (caminhos `C:\Users\Korsky\...`); funciona sem eles, mas você pode editar `agents/web-builder.md` para apontar para seus próprios materiais ou remover essas seções.
- `impeccable-manual-edit-applier` — auxiliar da skill impeccable.

## Complementos recomendados (não inclusos)

O `/design-max` também aproveita estes plugins, se instalados:

```bash
# frontend-design da Anthropic (rota de landing pages/marketing)
claude plugin install frontend-design

# 9 plugins de processo de design (pesquisa, design systems, critique, handoff...)
claude plugin marketplace add Owl-Listener/designer-skills
claude plugin install ui-design@designer-skills interaction-design@designer-skills visual-critique@designer-skills design-systems@designer-skills design-research@designer-skills prototyping-testing@designer-skills ux-strategy@designer-skills design-ops@designer-skills designer-toolkit@designer-skills

# tipografia automática + auditoria de design (bencium)
claude plugin marketplace add bencium/bencium-claude-code-design-skill
claude plugin install typography@bencium-marketplace design-audit@bencium-marketplace
```

## Créditos e licenças

Este pacote agrega skills de múltiplos autores — ver [NOTICE.md](NOTICE.md). Os créditos pertencem aos autores originais; as skills mantêm suas licenças de origem (MIT na maioria).

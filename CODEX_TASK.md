# Próxima execução no Codex

O objetivo é transformar o protótipo aprovado da CWB Portões Hub em uma aplicação estruturada sem alterar a identidade visual ou os fluxos validados.

## Fonte visual

O protótipo aprovado nesta etapa é `nexo-field-prototipo-v14.html`. Ao adicionar esse arquivo ao repositório, use-o inicialmente como `index.html` e trate-o como fonte de verdade visual.

## Primeira etapa de refatoração

1. Preservar 100% do visual e comportamento existentes.
2. Migrar gradualmente para Next.js + React + TypeScript.
3. Separar layout, navegação e módulos em componentes.
4. Extrair dados mockados para uma camada `src/data` substituível posteriormente por API.
5. Não implementar backend nesta primeira refatoração.
6. Não redesenhar a interface nem aplicar template SaaS genérico.
7. Manter mapa, agenda, Kanban de OS, técnicos, clientes, produtos/materiais, serviços, orçamentos, unidades, financeiro, relatórios e mock do app técnico.
8. Manter geração de orçamento em PDF com papel timbrado da CWB.
9. Preservar suporte a menu expandido/recolhido e tooltips quando recolhido.
10. Para testes, aplicar validação proporcional à mudança; não rodar automaticamente build/lint/suíte completa para alterações simples de UI.

## Evolução posterior

Depois da paridade do front-end, planejar backend NestJS/Node, PostgreSQL + PostGIS, autenticação/RBAC, multiunidade/franquias, rastreamento GPS em background, sincronização offline, Redis/WebSocket, app React Native e integrações financeiras/fiscais.

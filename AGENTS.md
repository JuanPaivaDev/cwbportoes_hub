# AGENTS.md — CWB Portões Hub

## Objetivo

Este repositório contém o protótipo aprovado da plataforma de gestão de operações de campo da CWB Portões Eletrônicos. O protótipo deve ser tratado como fonte de verdade visual e funcional durante a evolução para a aplicação real.

## Regra principal

Preserve o comportamento, a identidade visual, a densidade de informação, a navegação e os fluxos existentes antes de refatorar. Não substitua a interface por um template SaaS genérico.

## Arquitetura futura desejada

- Front-end: Next.js + React + TypeScript
- UI: Tailwind CSS + shadcn/ui quando fizer sentido
- Ícones: Hugeicons
- Backend: Node.js / NestJS
- Banco: PostgreSQL + PostGIS
- Cache/realtime: Redis + WebSocket
- App técnico: React Native
- Arquivos: S3/R2
- Mapas: solução baseada em OpenStreetMap/Mapbox/Google conforme decisão futura

## Módulos do produto

Dashboard, Central de Operações, Agenda, Ordens de Serviço em Kanban, Técnicos, Clientes, Produtos e Materiais, Serviços, Orçamentos/PDF, Unidades/Franquias, Financeiro, Relatórios, Configurações e aplicativo do técnico.

## Diretrizes de implementação

1. Não introduza backend ou banco fictício sem solicitação. A versão atual é deliberadamente mockada.
2. Ao migrar para React, faça a migração por módulos, mantendo paridade visual e funcional.
3. Estruture os mocks em uma camada de dados substituível por API no futuro.
4. O produto precisa suportar múltiplas unidades/franquias e visão consolidada da rede.
5. Ordens de serviço são o núcleo operacional e devem conectar agenda, técnico, localização, checklist, materiais, serviços, financeiro e orçamento.
6. Rastreamento real futuramente deve considerar background GPS, offline-first, geofence, precisão, bateria e sincronização.
7. Orçamentos devem permanecer vinculados ao sistema e gerar PDF timbrado com a marca CWB.
8. Produtos e serviços atuais vieram das planilhas do cliente e devem ser preservados ao migrar os dados.

## Validação e testes

Avalie proporcionalmente a necessidade de lint, build e testes. Mudanças simples de UI não devem disparar automaticamente toda a suíte. Execute validações focadas primeiro e amplie apenas quando a alteração justificar.

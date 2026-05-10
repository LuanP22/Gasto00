# Contexto da Conversa - PROJETO Gasto0

## Resumo do Projeto

Aplicativo financeiro **Gasto0** desenvolvido com Claude AI (1 de abril - 10 de maio de 2026).

## Stack Tecnologica

- Frontend: HTML/CSS/JavaScript puro (single file)
- Banco de dados: Supabase (PostgreSQL)
- Hospedagem: Netlify
- IA: API Anthropic (Claude)

## Tabelas no Supabase

- g0_users - usuarios (id, name, email, pw, plan, plan_expires_at, stripe_customer_id)
- g0_data - dados financeiros em JSON por usuario
- chat_mensagens - historico do Gestor IA
- Funcoes SQL: g0_login, g0_reset_pw

## Funcionalidades Implementadas

### Dashboard
- Cards: saldo, receitas, despesas, saude financeira
- Grafico SVG: Receitas vs Despesas (12 meses)
- Grafico SVG: Curva de faturamento acumulado
- Analise por mes (lista lateral + painel de detalhes)
- Comparador de meses lado a lado

### Transacoes
- Cadastro: tipo, valor, categoria, cartao, data, descricao
- Filtros: abas Todas/Receitas/Despesas, mes, categoria, status
- Editar e excluir com botoes
- Flag pago/pendente (badge clicavel)
- Exportacao CSV

### Cartoes de Credito
- Cadastro com limite e datas de fechamento/vencimento
- Fatura atual (soma transacoes do mes vinculadas ao cartao)
- Historico mensal com barras visuais (ultimos 6 meses)

### Metas Financeiras
- Criacao com valor alvo, prazo e aportes
- Progresso visual + calculo mensal

### Categorias
- Pre-definidas + personalizaveis com icone e cor

### Relatorios
- Navegacao por mes (setas + dropdown)
- Alertas inteligentes
- Detalhamento por categoria
- Historico 6 meses comparativo
- Comparador de meses

### Gestor Financeiro IA
- Chat conversacional com contexto financeiro completo
- Historico persistido no Supabase
- Rate limiting: 10 msgs/dia (Free), ilimitado (Pro)
- Proxy via Netlify Function /api/ai-chat

### Sincronizacao
- Exportar/Importar backup JSON
- Leitura de PDF de fatura

## Deploy

- URL: gasto0.netlify.app
- Metodo: arquivo unico gasto0-standalone.html
- Variavel: ANTHROPIC_API_KEY no Netlify

## Proximos Passos

1. Sistema de pagamento (Stripe) - planos Free/Pro
2. Chat Bot WhatsApp via Twilio (multi-cliente)
3. Seguranca: RLS Supabase + Auth nativo
4. PWA nas lojas (App Store/Google Play)

## IDs Importantes

- Netlify Site ID: 042551d2-895f-4be6-8dc2-f8b43ba8f374
- Supabase Project ID: potptpukrzccicpbpfkj

---
Contexto gerado em 10/05/2026

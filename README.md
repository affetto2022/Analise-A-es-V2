# Farol Traders — Analisador Gráfico Inteligente V1

Starter full-stack para Google AI Studio Build. Frontend React + TypeScript, backend Node/Express, Lightweight Charts, Twelve Data e Gemini.

## Importante
- Esta é uma primeira base funcional de arquitetura, não uma garantia de cobertura de todos os símbolos/períodos.
- Configure `TWELVE_DATA_API_KEY` no ambiente do servidor e `GEMINI_API_KEY` no painel Secrets do AI Studio.
- As regras exatas das seis fases Oliver Kell ainda precisam ser inseridas no módulo `server/indicators.ts`. O estado permanece `NÃO CONFIGURADO` até isso acontecer; não são inventadas regras.
- O volume financeiro calculado como preço x quantidade é uma estimativa, não volume financeiro oficial da bolsa.
- Confira os termos/licenças do provedor de dados antes de publicar para terceiros.

## Dependências esperadas
React, TypeScript, Vite, `lightweight-charts`, Express, `@google/genai`, `dotenv`, `cors`.

No AI Studio Build, peça ao agente para instalar dependências ausentes e adaptar a inicialização ao template full-stack criado pela plataforma.

## Variáveis de ambiente (servidor)
`TWELVE_DATA_API_KEY=...`
`GEMINI_API_KEY=...`
`PORT=8080`

## Endpoints
- `GET /api/health`
- `GET /api/candles?symbol=AAPL&interval=1day&outputsize=300`
- `POST /api/analyze`

Intervalos suportados pelo app: mensal, semanal, diário, 60, 30, 15 e 5 minutos. A disponibilidade real depende da fonte e do símbolo.

## Estrutura sugerida
- `src/App.tsx` — interface.
- `src/ChartPanel.tsx` — gráfico e indicadores visuais.
- `src/types.ts` — tipos compartilhados.
- `server/index.ts` — API segura.
- `server/indicators.ts` — SMA, EMA, ATR e volume financeiro estimado.
- `server/olliverKell.ts` — ponto de integração para as regras oficiais fornecidas pelo usuário.

## Execução local
Use Node.js 20+. Instale as dependências do projeto conforme o template escolhido pelo AI Studio. Rode o backend e o frontend pelos scripts definidos no `package.json`.

## Publicação
1. Abra Google AI Studio > Build.
2. Crie app Web e use o prompt de continuação incluído no projeto.
3. Adicione as secrets no painel de configurações.
4. Teste símbolos brasileiros e internacionais em cada intervalo.
5. Publique no Cloud Run pelo botão Publish, verificando custos/limites da conta.

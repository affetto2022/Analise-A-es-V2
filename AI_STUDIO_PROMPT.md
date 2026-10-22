Continue o projeto Farol Traders — Analisador Gráfico Inteligente usando os arquivos desta base.

Requisitos obrigatórios:
1. Integre esta base ao template full-stack atual do Google AI Studio Build, React + TypeScript no cliente e Node.js no servidor.
2. Instale as dependências necessárias: lightweight-charts, express, @google/genai e as dependências exigidas pelo template.
3. Nunca envie TWELVE_DATA_API_KEY ou GEMINI_API_KEY para o browser. Use somente secrets do servidor.
4. O usuário deve informar ticker, escolher mensal/semanal/diário/60m/30m/15m/5m e clicar em Atualizar para buscar os candles. Não implemente atualização automática.
5. Use Twelve Data como primeiro adaptador de cotações. Normalizar os candles em {time, open, high, low, close, volume}. Mostrar erro amigável para intervalos/símbolos indisponíveis. Não usar dados fictícios como reais.
6. Gráfico com candles OHLC, SMA10, SMA20 e painel inferior de volume. Permitir ligar/desligar cada overlay.
7. Volume financeiro: se o provedor não entregar valor financeiro por candle, exibir estimativa preço representativo x volume e rotular claramente “estimado”. Adicionar média móvel com período editável e SMA/EMA.
8. ATR Wilder calculado no servidor ou em módulo testável.
9. NÃO inventar as seis fases Oliver Kell. Manter o status “Regras Oliver Kell pendentes de configuração” até receber as regras exatas. Criar uma interface de função para inserir condições, estados e transições posteriormente.
10. Botão “Analisar com IA” envia ao endpoint /api/analyze apenas ticker, intervalo, candles e indicadores calculados. Gemini responde em português com: contexto, ciclo (ou indisponível), volume, volatilidade, suportes/resistências estimados, cenários condicionais, invalidação e limitações dos dados.
11. Implementar loading, empty states, validação, timeout/tratamento de erros, acessibilidade e layout responsivo escuro com identidade Farol Traders: azul-marinho, dourado, verde e vermelho.
12. Não executar ordens nem apresentar previsões como certezas.
13. Adicionar testes para SMA, EMA, ATR e agregação de candles, além de um README com configuração e deploy.
14. Antes de finalizar, execute/build/teste o projeto e corrija todos os erros reais encontrados. Não afirme que algo foi testado se não foi executado.

# Ticker Lab

A single-page, learn-to-trade workstation. Open `index.html` in a browser (or serve it with GitHub Pages). It has no build step and no server.

> Educational tool, not financial advice. Every signal is a simple, visible rule of thumb. Paper-trade before risking money.

## Live data (free keys)

Without keys the app runs on **simulated demo data**, clearly labeled. For real market data, open **Settings** and add:

| Provider | What it powers | Free tier |
|---|---|---|
| [Finnhub](https://finnhub.io/register) | Real-time quotes and live trades (WebSocket), fundamentals, analyst ratings, earnings dates, news, peers, search | 60 calls/min |
| [Twelve Data](https://twelvedata.com/register) | Daily price history for charts, moving averages, RSI, MACD, ATR, volatility | 8 calls/min, 800/day |

Keys stay in your browser's localStorage and are only sent to their own provider. Price history is cached for 6 hours, so the first load of a big watchlist takes a minute or two (Twelve Data's 8/min limit). After that, loads are instant.

## What's inside

- **Dashboard**: index pulse, market regime (S&P vs. its 200-day), your watchlist scored 0–100 with a signal label (buy zone / uptrend / extended / downtrend), RSI, distance from the 50-day, 52-week range, days to earnings, and market news.
- **Research**: the "why" behind each signal, a rules-based trade plan (entry zone, stop, target, reward:risk), position sizing from your risk %, a price chart with 50/200-day averages, Bollinger bands and RSI, fundamentals (P/E, PEG, growth, margins), analyst ratings, news and peers.
- **Options lab**: 11 strategies (calls, puts, spreads, covered calls, cash-secured puts, collars, iron condors, straddles), with a suggestion that fits the stock's trend and volatility. Black–Scholes pricing, Greeks, max profit/loss, breakevens, probability of profit, expected move, and an interactive payoff chart with a days-forward slider. You can type real premiums and IV from your broker.
- **Portfolio**: a $100k paper account (stocks and options), take-profit / risk checks on paper and real holdings (trailing stop, overbought, stretched, earnings, short- vs. long-term holding period), price alerts, a trade journal, and JSON export/import.
- **Learn**: plain-English explanations of every concept. Click any `?` in the app to jump there.

## Limits to know

- Option prices are model estimates. The free data plans don't include option chains.
- Free Finnhub covers US-listed stocks and ETFs. Indexes like ^VIX aren't available.
- Market-hours status ignores exchange holidays (option expirations do account for them).

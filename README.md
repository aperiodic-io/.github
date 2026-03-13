# Aperiodic

**Institutional-grade market microstructure analytics with full exchange universe coverage.**

Turn flow dynamics into alpha in hours, not months.

## What We Do

Aperiodic provides pre-computed market microstructure, liquidity, and order flow metrics across major exchanges. We eliminate the need to build and maintain custom tick-level data infrastructure so quant researchers and traders can focus on strategy development.

### Metrics

- **Trade Flow** — VTWAP, flow, trade size, impact, range, up/down ticks, run structure, returns, slippage
- **Order Book** — L1 and L2 imbalance and liquidity metrics
- **Derivatives** — Basis, funding rates, open interest, derivative pricing
- **OHLCV** — Candles, VWAP, TWAP across configurable intervals (1m to 1d)

### Supported Exchanges

- Binance Futures
- OKX Perpetuals

## Getting Started

Install the Python client:

```bash
pip install aperiodic
```

```python
from aperiodic import Aperiodic

client = Aperiodic(api_key="your-api-key")

# Discover available symbols
symbols = client.symbols()

# Fetch trade flow metrics
data = client.get("flow", symbol="BTC-USDT-PERP", interval="5m")
```

See the [`client`](https://github.com/aperiodic-io/client) repo for full documentation.

## Repositories

| Repo | Description |
|------|-------------|
| [`client`](https://github.com/aperiodic-io/client) | Python client for the Aperiodic API |
| [`atlas`](https://github.com/aperiodic-io/atlas) | Unified exchange symbology |
| [`cli`](https://github.com/aperiodic-io/cli) | Command-line interface |
| [`hftbacktest`](https://github.com/aperiodic-io/hftbacktest) | High-frequency trading backtesting framework (Rust) |

## Contact

- Web: [aperiodic.io](https://aperiodic.io)
- Email: info@aperiodic.io

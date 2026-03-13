<div align="left">

# Aperiodic

### Institutional-Grade Market Microstructure Metrics

**Turn flow dynamics into alpha in hours, not months.**

[Website](https://aperiodic.io) | [Python Client](https://github.com/aperiodic-io/client) | [Contact Us](mailto:info@aperiodic.io)

---

</div>

## The Problem

Building tick-level data infrastructure is expensive, slow, and fragile. Quant teams spend months wiring up exchange feeds, normalizing symbology across venues, computing microstructure metrics, and maintaining pipelines — before a single signal is tested.

## The Solution

Aperiodic delivers **pre-computed, research-ready microstructure metrics** across the full exchange universe. We handle the ingestion, normalization, and computation so you can skip straight to alpha discovery.

- **No infrastructure to build.** We process raw tick data and deliver clean, structured metrics via API.
- **No symbology headaches.** Our open-source [Atlas](https://github.com/aperiodic-io/atlas) securities master normalizes 38+ exchanges into a unified contract model.
- **No waiting.** Concurrent parquet downloads get years of history to your notebook in seconds.

---

## Metrics

We compute a comprehensive suite of market microstructure features at intervals from **1 minute to 1 day**.

### Trade Flow
| Metric | What It Captures |
|--------|-----------------|
| **VTWAP** | Volume-time weighted average price |
| **Flow** | Net signed trade flow and directional pressure |
| **Trade Size** | Distribution of trade sizes and large-trade detection |
| **Impact** | Price impact of trades |
| **Range** | Intra-interval price range and volatility |
| **Up/Down Ticks** | Tick direction frequency and momentum |
| **Run Structure** | Consecutive same-direction trade sequences |
| **Returns** | Interval returns at multiple horizons |
| **Slippage** | Execution quality relative to mid-price |

### Order Book
| Metric | What It Captures |
|--------|-----------------|
| **L1 Imbalance** | Top-of-book bid/ask pressure asymmetry |
| **L1 Liquidity** | Best bid/offer depth and spread |
| **L2 Imbalance** | Deeper book order flow imbalance |
| **L2 Liquidity** | Multi-level depth and cumulative book shape |

### Derivatives
| Metric | What It Captures |
|--------|-----------------|
| **Basis** | Futures-spot premium and term structure |
| **Funding** | Perpetual funding rate and carry |
| **Open Interest** | Position buildup and unwind signals |
| **Derivative Price** | Mark, index, and contract-level pricing |

### Aggregates
OHLCV candles, VWAP, and TWAP — computed consistently across all supported venues.

---

## Exchange Coverage

| Exchange | Instruments |
|----------|------------|
| **Binance Futures** | Perpetuals |
| **OKX** | Perpetuals |

Full spot, futures, and perpetual symbology for **38+ exchanges** available through [Atlas](https://github.com/aperiodic-io/atlas), with data coverage expanding continuously.

---

## Quick Start

Install the Python client:

```bash
pip install aperiodic
```

## Architecture

```
Exchange Feeds ──> Ingestion ──> Normalization (Atlas) ──> Metric Computation ──> Parquet Store
                                                                                      │
                                                                              Aperiodic API
                                                                                      │
                                                          Python Client / CLI ─── Your Research
```

- **Atlas** normalizes raw exchange symbology into a stable, exchange-agnostic contract model
- **Metrics engine** computes microstructure features from tick-level data
- **API** serves pre-computed parquet files with parallel downloads for maximum throughput
- **Client** handles concurrency, date-range filtering, and local concatenation automatically

---

## Open Source

| Repository | Description |
|------------|-------------|
| [`client`](https://github.com/aperiodic-io/client) | Python client — sync & async API, concurrent downloads, Polars DataFrames |
| [`atlas`](https://github.com/aperiodic-io/atlas) | Securities master — unified symbology across 38+ crypto exchanges |
| [`cli`](https://github.com/aperiodic-io/cli) | Command-line interface for Aperiodic |
| [`hftbacktest`](https://github.com/aperiodic-io/hftbacktest) | High-frequency trading backtester — limit orders, queue position, latency simulation (Rust) |

---

## Who It's For

- **Quant Researchers** exploring microstructure signals without building tick infrastructure
- **Systematic Traders** who need clean, normalized flow and book data across venues
- **Fund Managers** looking for alternative data to enhance existing strategies
- **Academics** studying market microstructure with production-quality datasets

---

<div align="center">

**[Get Started](https://aperiodic.io)** | **[Python Client Docs](https://github.com/aperiodic-io/client)** | **[info@aperiodic.io](mailto:info@aperiodic.io)**

</div>

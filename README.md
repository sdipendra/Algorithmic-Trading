# Algorithmic-Trading
The mission of Algorithmic Trading library is to eliminate time &amp; effort wasted by Quant Developer's in writing code that is not part of their core Trading Algorithm.

## Features

- Written in Kotlin.
- Safe to use with open source code & self hosting.
- Multi-strategy support with efficient & concurrent strategy execution.
- Inbuilt concurrency management to prevent race conditions.
- OpenTelemetry integration for debugging.
- Intraday backtesting support using Zerodha's historical data API. Only minute level granularity supported currently.
- Popular Broker API integrations. Only Zerodha's Kite Connect API supported currently, will add others depending on demand.
- Modular & extensible.

## Implementation

The project is extracted from a modular monolith trading system designed to trade in Indian Equity Markets using Zerodha's Kite Connect API.

Modules:

- Ticker: To asynchronously receive most recent price data & order updates.
- Driver: To manage routing price data & order updates to multiple stratagies.
- Trader: Implementation of your strategy.
- Broker: Interface for interacting with broker API's mainly for placing orders. Placed behind an interface to keep the system vendor agnostic. Implementation available for Zerodha's Kite Connect API. Easy to add other brokers as well.
- Exchange: To simulate stock exchange for backtesting strategies using the exact strategy code that will be used for live trading.
- Ingester: To capture & route price data during live trading.
- SessionTickStore: To store price data during live trading.
- SessionCandleStore: To store candle data during live trading.
- SessionMetaStore: To store instrument list & intraday margin for the day.
- HistoricalCandleStore: To locally cache historical candle data.
- CandleRepo: Three tier candle cache(memory, storage & network) to reduce latency of requesting candle data.

Quant libraries:

- OlsRegression
- SimpleOlsRegression
- Correlation
- Cointegration
- ADFTest
- DFTest
- FastFourierTransform
- ARProcessDiscrete
- WNProcess
- OUDiscrecteProcess
- OUEstimator
- OUProcess
- DfNcNtDistribution
- DfNcNtSimulatedDistribution
- DfTableGenerator
- Portfolio
- Outcome
- AlphaSummary
- DataBackedTimeMap
- TimeWindow
- LRUCache
- PairDepthQuote
- PositionCalculator

## Consultation
The project is in consultation phase. The goals of the consultation phase are:
1. Identify if this library will be useful for others?
   - If this is something that will be useful to you please star the project on GitHub & join the [Discord Server](https://discord.gg/GJZfApsgzb).
2. Is this a rework. i.e. are there any existing Kotlin projects which achieve the feature goals of this library.
3. Additional details that should be included in the README.

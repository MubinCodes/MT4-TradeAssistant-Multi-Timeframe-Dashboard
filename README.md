# TradeAssistant - MT4 Multi-Timeframe Indicator Dashboard

TradeAssistant is a MetaTrader 4 Expert Advisor that displays multiple technical indicator values across different timeframes on a single chart.

It helps traders quickly monitor whether selected indicators are showing **buy**, **sell**, or **neutral** conditions.

> ⚠️ This project is for educational and portfolio demonstration purposes only. It is not financial advice and does not guarantee profitable trading results.

---

## Overview

TradeAssistant is not a traditional auto-trading EA.  
It works as a visual dashboard for MetaTrader 4.

The EA reads indicator values from multiple timeframes and displays them directly on the chart using colored text and arrows.

It allows users to compare indicator conditions across:

- M1
- M5
- M15
- M30
- H1
- H4
- D1
- W1
- MN1

This makes it easier to view multi-timeframe market conditions without switching between charts.

---

## Indicators Used

TradeAssistant uses the following indicators:

### Moving Average

The EA compares a fast moving average and a slow moving average.

Default settings:

- Fast MA Period: `10`
- Fast MA Method: `EMA`
- Slow MA Period: `20`
- Slow MA Method: `EMA`
- Applied Price: `Close`

Signal logic:

- Fast MA above Slow MA = Buy condition
- Fast MA below Slow MA = Sell condition

---

### ADX

The EA uses ADX to check trend strength and directional movement.

Default settings:

- ADX Period: `14`
- Minimum ADX: `25`

Signal logic:

- ADX above minimum level and +DI above -DI = Buy condition
- ADX above minimum level and -DI above +DI = Sell condition
- ADX below minimum level = Neutral condition

---

### RSI

The EA uses RSI to identify overbought and oversold conditions.

Default settings:

- RSI Period: `14`
- Upper Level: `70`
- Lower Level: `30`

Signal logic:

- RSI above upper level = Buy condition
- RSI below lower level = Sell condition
- RSI between levels = Neutral condition

---

### MACD

The EA uses a two-line MACD indicator.

Default settings:

- Fast EMA: `12`
- Slow EMA: `26`
- Signal EMA: `9`

Signal logic:

- MACD Main above MACD Signal = Buy condition
- MACD Main below MACD Signal = Sell condition

> Note: This EA uses a custom `MACD-2Line.ex4` indicator resource.

---

### Stochastic Oscillator

The EA compares the Stochastic main line and signal line.

Default settings:

- K Period: `5`
- D Period: `3`
- Slowing: `3`

Signal logic:

- Stochastic Main above Stochastic Signal = Buy condition
- Stochastic Main below Stochastic Signal = Sell condition

---

## Key Features

- Multi-timeframe dashboard
- Displays indicator values directly on the chart
- Shows buy/sell arrows for each indicator condition
- Uses color-coded signals
- Supports buy, sell, and neutral display conditions
- Monitors 9 standard MetaTrader timeframes
- Customizable indicator parameters
- Customizable text color, font size, and arrow color
- Built for MetaTrader 4 using MQL4

---

## Timeframes Displayed

The dashboard displays values for:

```text
M1, M5, M15, M30, H1, H4, D1, W1, MN1

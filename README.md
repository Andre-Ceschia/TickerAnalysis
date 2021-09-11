# TickerAnalysis
TickerAnalysis is on open source library that calculates technical indicators for any ticker listed on yahoo finance.

## Installation
    pip install ticker-analysis
    
 ## Technical Indicators
TickerAnalysis can calculate exponential moving averages, simple moving averages, relative stregnth index (RSI), moving average convergence divergence (MACD), volume weighted average price (VWAP), stochtastic, bollinger bands, volume osciallator (VOSC), price percentage oscillator, and commodity channel index (CCI) of any ticker listed on yahoo finance.
    
## Example Usage
    from TickerAnalysis import Ticker
    
    ticker = Ticker("SU", "5m", "1mo")

    current_price = ticker.get_price()

    bollinger_bands = ticker.get_bollinger_bands()
    lower_bollinger_band = bollinger_bands["bolDown"]

    if current_price < lower_bollinger_band:
        print("SU is oversold")

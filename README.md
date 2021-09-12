# TickerAnalysis
TickerAnalysis is on open source library that calculates technical indicators for any ticker listed on yahoo finance.

## Installation
    pip install ticker-analysis
    
 ## Technical Indicators
TickerAnalysis can calculate the exponential moving average, the simple moving average, the relative stregnth index (RSI), the moving average convergence divergence (MACD), the volume weighted average price (VWAP), the stochtastic, the bollinger bands, the volume osciallator (VOSC), the price percentage oscillator, and the commodity channel index (CCI) of any ticker listed on yahoo finance.
    
## Example Usage
    from TickerAnalysis import Ticker
    
    ticker = Ticker("SU", "5m", "1mo")

    current_price = ticker.get_price()

    bollinger_bands = ticker.get_bollinger_bands()
    lower_bollinger_band = bollinger_bands["bolDown"]

    if current_price < lower_bollinger_band:
        print("SU is oversold")

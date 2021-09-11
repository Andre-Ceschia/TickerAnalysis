# ticker-analysis
Ticker analysis is on open source library that calculates technical indicators for any ticker available on yahoo finance.

## Installation
    pip install ticker-analysis
    
## Example Usage
    from TickerAnalysis import Ticker
    
    ticker = Ticker("SU", "5m", "1mo")

    current_price = ticker.get_price()

    bollinger_bands = ticker.get_bollinger_bands()
    lower_bollinger_band = bollinger_bands["bolDown"]

    if current_price < lower_bollinger_band:
        print("SU is oversold")

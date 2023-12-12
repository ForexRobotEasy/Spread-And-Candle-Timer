# Spread And Candle Timer

This code is a custom indicator for MetaTrader 5 (MQL5) that detects and highlights various candlestick patterns such as doji, engulfing, hammer, and shooting star on the chart. It also tracks the spread changes and new candle formations.

## Global Variables

- `lastCandleTime`: Stores the timestamp of the last formed candle.
- `lastSpread`: Stores the spread value.
- `dojiColor`: The color used to highlight doji patterns.
- `engulfingColor`: The color used to highlight engulfing patterns.
- `hammerColor`: The color used to highlight hammer patterns.
- `shootingStarColor`: The color used to highlight shooting star patterns.
- `sensitivity`: The sensitivity level used to identify the patterns.

## Custom Indicator Functions

### OnInit()

This function is called when the indicator is initialized. It returns `INIT_SUCCEEDED` to indicate a successful initialization.

### OnDeinit(const int reason)

This function is called when the indicator is deinitialized. It can be used to perform any necessary cleanup tasks.

### OnCalculate(const int rates_total, const int prev_calculated, const datetime &time[], const double &open[], const double &high[], const double &low[], const double &close[], const long &tick_volume[], const long &volume[], const int &spread[])

This function is called for each new candlestick formation. It loops through each candlestick and checks for the presence of doji, engulfing, hammer, and shooting star patterns. It also updates the `lastCandleTime` and `lastSpread` variables. The function returns the total number of calculated bars.

### Helper Functions

These functions are used to determine if a candlestick satisfies the conditions for a specific pattern. They return `true` if the conditions are met, otherwise `false`.

- `IsDoji(double open, double high, double low, double close)`: Checks if the candlestick is a doji.
- `IsEngulfing(double open, double high, double low, double close)`: Checks if the current candle engulfs the previous candle.
- `IsHammer(double open, double high, double low, double close)`: Checks if the candlestick is a hammer.
- `IsShootingStar(double open, double high, double low, double close)`: Checks if the candlestick is a shooting star.

### HighlightPattern(int index, color highlightColor)

This function is called to highlight the identified pattern on the chart. The implementation code for highlighting the pattern should be added here.

### OnTick()

This function is called on each tick. It checks for spread changes and performs actions when the spread changes.

### OnTimer()

This function is called at regular intervals. It checks for new candle formations and performs actions when a new candle forms.

## Product Description

Spread And Candle Timer is a custom indicator for MetaTrader 5 (MQL5) that helps traders identify and track various candlestick patterns on the chart. It highlights patterns such as doji, engulfing, hammer, and shooting star, making it easier for traders to spot potential trading opportunities.

Key Features:
- Detects and highlights doji, engulfing, hammer, and shooting star patterns
- Tracks spread changes in real-time
- Alerts traders when a new candle forms
- Customizable sensitivity level for pattern identification

This indicator is designed to assist traders in identifying potential reversal or continuation patterns in the market. By providing visual cues on the chart, traders can make informed trading decisions based on the identified patterns.

Please note that ForexRobotEasy is not the official developer of this product. We only provide sample code that can work as described in this product. For detailed reviews and trading results of Spread And Candle Timer, please visit the official developer's website or search for the product on the MQL5 platform. [Click here](https://forexroboteasy.com/forex-robot-review/review-spread-and-candle-timer-the-candle-stick-patterns-finder/) for detailed reviews and trading results of this product.

# Higher TimeFrame Candle Tracker

This code is a custom indicator for the MetaTrader 5 platform that plots the candle of a higher timeframe on the current chart. It is designed to enhance day trading by providing a visual representation of the higher timeframe candle, allowing traders to better understand the overall market trend.

## How it works

1. Include necessary libraries and define constants:
   - The code includes the `SymbolInfo.mqh` library to retrieve symbol information.
   - It defines the `Timeframe` enum to map the constants of the desired timeframes (DAILY, WEEKLY, and MONTHLY) to the corresponding MetaTrader 5 constants.

2. Global variables:
   - `currentPrice`: stores the current price in real-time.
   - `selectedTimeframe`: stores the selected timeframe.

3. Custom indicator function `PlotHigherTimeframeCandle()`:
   - Retrieves symbol information using the `CSymbolInfo` class.
   - Calculates the bar size in seconds based on the selected timeframe.
   - Calculates the index of the current bar using `iBarShift()`.
   - Calculates the start and end time of the higher timeframe candle using `iTime()`.
   - Retrieves the OHLC prices of the higher timeframe candle using `iOpen()`, `iClose()`, `iHigh()`, and `iLow()`.
   - Plots the higher timeframe candle on the chart using `ObjectCreate()` and sets its properties using `ObjectSet()`.

4. Custom function `GetCurrentPrice()`:
   - Retrieves the current price in real-time using the `SymbolInfoDouble()` function.

5. Custom function `HandleErrors()`:
   - Handles any errors that may arise during execution by checking the value of `GetLastError()` and printing the error code.

6. Custom function `SelectTimeframe()`:
   - Sets the selected timeframe to the desired value.

7. Custom function `OnInit()`:
   - Initializes the program by setting the default timeframe to DAILY.

8. Custom function `OnTick()`:
   - Updates the current price in real-time by calling `GetCurrentPrice()`.

9. Custom function `OnStart()`:
   - Calls `PlotHigherTimeframeCandle()` to plot the higher timeframe candle.
   - Prints the current price using `Print()`.
   - Calls `HandleErrors()` to handle any errors.

## Product Description

The Higher TimeFrame Candle Tracker is a powerful tool designed to enhance day trading strategies by providing a visual representation of the higher timeframe candle on the current chart. This indicator allows traders to easily identify the overall market trend and make informed trading decisions.

Key Features:
- Plots the candle of a higher timeframe on the current chart.
- Supports various higher timeframes such as DAILY, WEEKLY, and MONTHLY.
- Provides real-time updates of the current price.
- Customizable candle color, style, and width.

By using the Higher TimeFrame Candle Tracker, traders can gain valuable insights into the market trend and improve their day trading strategies. This indicator is suitable for both beginner and advanced traders who want to make more accurate trading decisions based on the higher timeframe analysis.

Please note that ForexRobotEasy is not the official developer of this product. We only provide this sample code as an example of how the product works. For detailed reviews and trading results of the Higher TimeFrame Candle Tracker, please visit the official developer's website at [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/higher-timeframe-candle-tracker-enhance-day-trading-with-forex-software-review/). To find the official developer of this product, please use the MQL5 platform.

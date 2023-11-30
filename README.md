# Aigridpro H4 Multicurrency

This code is an expert advisor for the MetaTrader 4 platform that implements a grid trading strategy based on moving averages. The strategy opens buy trades when the price is above the moving averages and sell trades when the price is below the moving averages.

## Input Parameters

- LotSize: The lot size for each trade.
- GridStep: The grid step in pips.
- TakeProfit: The take profit in pips.
- StopLoss: The stop loss in pips.

## Libraries Used

- Trade: This library is used to manage trades, including opening and closing positions.
- MovingAverages: This library is used to calculate moving averages.

## Expert Initialization (OnInit)

In the initialization function, the trade parameters are set up. The expert advisor uses a specific magic number (123456) to identify its trades. The moving averages parameters are also set up, creating two simple moving averages with periods 5 and 10.

## Expert Deinitialization (OnDeinit)

In the deinitialization function, all open trades are closed.

## Expert Start (OnTick)

In the start function, the expert advisor checks if it is time to open new trades. The condition `TimeHour(TimeCurrent()) % 4 == 0` checks if the current hour is divisible by 4.

If it is time to open new trades, the current price level is calculated by subtracting the grid step multiplied by the point value from the current bid price.

The expert advisor then checks if there are any open trades at the current price level. If there are buy or sell trades, the function exits without taking any action.

Next, the expert advisor checks if the current price level is above the moving averages. If it is, a buy trade is opened at the current price level with the specified lot size, take profit, and stop loss levels.

Similarly, if the current price level is below the moving averages, a sell trade is opened at the current price level.

## Product Description

Aigridpro H4 Multicurrency is an expert advisor for the MetaTrader 4 platform that implements a grid trading strategy based on moving averages. It is designed to provide low-risk trading with the potential for high returns.

The expert advisor uses a grid step and moving averages to identify entry points for trades. It opens buy trades when the price is above the moving averages and sell trades when the price is below the moving averages. The lot size, take profit, and stop loss levels can be customized to suit individual trading preferences.

Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. For detailed reviews and trading results of this product, please visit [here](https://forexroboteasy.com/forex-robot-review/aigridpro-h4-multicurrency-review-of-a-robust-forex-software-with-low-risk-and-high-returns/). To find the official developer of this product, please use MQL5.

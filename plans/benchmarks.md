# Benchmarks

Practical benchmarks to beat:

## 1. Latest Market Price
Use the most recent market price as the forecast. This is the default naive baseline — assumes the market is already well-calibrated and the best predictor is just the current price.

## 2. Simple Moving Average (SMA) of Market Price
Average the market price over a rolling time window. Common windows:
- 1-hour SMA
- 6-hour SMA
- 24-hour SMA

Captures short- to medium-term trends while smoothing out noise.

## 3. Volume-Weighted Average Price (VWAP)
Average market price weighted by trade volume at each price point. Gives more weight to prices at which more trading activity occurred, making it a more representative measure of market consensus.

## 4. Equal-Weight Average of Top-K Traders by Past Profit
Identify the top-k traders ranked by historical profit. Take an equal-weight average of their current forecasts. Treats each expert equally regardless of how much they've earned.

## 5. Profit-Weighted Average of Top-K Traders
Same as above, but weight each trader's forecast by how much money they have made historically. Traders with stronger track records have more influence on the aggregate forecast.

## 6. Best Single Expert in Hindsight
The single trader whose forecasts were most accurate over the evaluation period, identified retrospectively. This is the **theoretical ceiling** for any expert-aggregation strategy — used as a reference point for regret-based comparisons.


**Setting.** You have $T$ resolved binary events from Polymarket. For each event, multiple wallets traded before resolution.

**Protocol.**

1. Before each event $t$, extract a prediction $p_{i,t} \in [0,1]$ for each active wallet $i$ from their trading behaviour within that event.
2. Maintain a weight $w_{i,t}$ over wallets using Hedge: after resolution, update weights based on each wallet's prediction loss.
3. Your aggregate forecast is the weighted combination of wallet predictions.

**Questions you want to answer.**

- Does Hedge over wallets outperform naive baselines like equal-weighted average or the raw market price?
- Which wallets are consistently informative across events?
- How do you extract a single prediction per wallet per event from messy intra-round trade sequences? (the open problem from earlier)

**Metric.** Log-loss or Brier score over resolved events.

That is the full project in one paragraph.
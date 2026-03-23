# Cache: Trump 2024 Sample Trades

**Date:** 2026-03-22
**Session:** Session 1

## Summary

During this session, we were exploring the Polymarket Data API to understand how trader-level data is structured. The goal was to get a feel for what information is available per wallet before building any algorithm on top of it.

We fetched the first 100 trades from the "Will Donald Trump win the 2024 US Presidential Election?" market (conditionId: `0xdd22472e552920b8438158ea7238bfadfa4f736aa4cee91a6b86c39ead110917`), extracted 5 random wallet addresses, then queried each wallet individually to get their full trade history filtered to this market.

This file exists to show a concrete sample of what the raw data looks like — the fields available, the structure, and what a real trader's buy/sell sequence looks like. It is a small exploratory snapshot, not a comprehensive dataset.

---

See `raw_output.json` for the full trade records for all 5 wallets.

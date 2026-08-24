# GROKBOT STRATEGY 1# - FundingBleedHarvester

## Strategy modules

The base desk (7 agents, shared setup prompt) runs empty until you hand it
a strategy. These are drop-in modules - paste one into the Trading Floor
group chat after the desk is live, and it plugs into the existing Strategist
/ Risk Manager / Execution Trader chain without touching the base config.

- `funding-bleed-harvester.md` - collects funding from crowded one-sided
  positions, delta-neutral, runs small and boring on purpose
- `dead-mans-switch-desk.md` - catches open positions you forgot about
  going into scheduled catalysts, not a P&L strategy, a seatbelt
- `narrative-decay-fader.md` - trades the gap between a narrative dying on
  social and price catching down to it
- `liquidation-cascade-scavenger.md` - the fastest module on the desk,
  structured to act inside a cascade instead of after it

Each file is self-contained: what it watches, the exact trigger condition,
the paste-ready prompt block, and the risk caps specific to that strategy.
Run every new module in paper mode for two weeks minimum before it touches
a real ticket, same as the base desk.

More modules get added as they get tested. Star/watch the repo if you want
them when they land.

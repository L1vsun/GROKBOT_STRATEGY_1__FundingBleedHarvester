Strategy: Funding Bleed Harvester

Most retail never checks funding rate until they're already bleeding it. This flips that — the desk hunts for OTHER people's bleed and gets paid to absorb it.

What it watches

Perpetual funding rates across majors and top 30 alts, every hour, on every exchange the desk has a read key for.

The trigger

Annualized funding on any pair crosses ±35% AND stays there for 3 consecutive readings (not one spike — three in a row, so it's a regime, not noise).

Paste this into Trading Floor:
\\

New strategy: Funding Bleed Harvester

Market Analyst: poll funding rates hourly across all connected exchanges.
Flag any pair where annualized funding exceeds 35% (either direction) for
3 consecutive hourly readings. Ignore single-reading spikes.

Research Analyst: on flag, check open interest trend for that pair over
the last 48h. Rising OI + extreme funding = crowd is one-sided and paying
to stay there. Falling OI + extreme funding = position already unwinding,
skip it.

Strategist: build a delta-neutral ticket — long spot / short perp (or
inverse, depending on funding direction) sized to collect the funding
spread. Backtest against the last 90 days of funding history for this
specific pair before it goes to Risk Manager. Reject if realized funding
capture in the backtest is below 8% annualized after estimated fees.

Risk Manager: standard desk limits apply. This strategy runs boring and
small on purpose — cap it at 2% of total exposure per open funding position,
max 3 funding positions open at once.

Trade Reviewer: log funding collected vs funding rate at entry, weekly,
separate from the main P&L log. This strategy is judged on its own line.
Why it's boring on purpose

\\

This is not a directional bet. It's picking up money crowded traders are paying to stay leveraged the wrong way. It grinds small in calm markets and spikes hard during mania — that's the whole edge, and it's the same edge prop desks have run since perpetuals existed. Nobody explains it because explaining it kills the yield.
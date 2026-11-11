---
name: usdrub-exit-timing
description: Analyze USD/RUB for a Russian investor who already holds USD and wants to choose a sensible window to sell dollars for rubles by a deadline. Combines macro, oil/export flows, CBR/Fed policy, fiscal FX operations, sanctions, infrastructure, geopolitics, seasonality, and price behavior. Outputs target-touch probabilities, a likely local-maximum window, and a practical wait/partial-sell/sell-most decision.
---

# USD/RUB Exit Timing

Use this skill when the user already holds USD and wants RUB, and the real question is not "what will USD/RUB be someday?" but "when should I sell my dollars before a deadline?"

This skill borrows the discipline of macro-event analysis and thesis validation: identify catalysts, transmission channels, evidence gaps, invalidation conditions, and timing risk. It does not pretend to know the exact daily peak.

## Default user context

Unless the user overrides it:

- Position: user already holds USD and wants RUB.
- Deadline: **15 December 2026**.
- Practical acceptable exit: **91 RUB/USD**.
- 93, 95 and 100 are upside opportunities, not mandatory targets.
- If evidence does not show a convincing path to 93-96 before the deadline, treat ~91 as a valid exit zone rather than waiting for an ideal maximum.
- Optimize for a sensible exit, not the exact intraday top.

## Always answer these four questions

1. What is the likely USD/RUB range by the deadline?
2. What is the probability of touching **91**, **93**, **95**, and **100** before the deadline?
3. What is the most likely **window for a local USD/RUB maximum** before the deadline?
4. Given the user's 91 target, should they **WAIT**, **START SELLING**, or **SELL MOST**?

## Live-data checks

For every fresh run, verify current information.

### RUB and Russian monetary conditions

Check:

- Bank of Russia official USD/RUB;
- a market/OTC proxy, with a clear caveat that direct MOEX USD trading is unavailable;
- CNY/RUB and/or USD futures proxies when useful;
- CBR key rate;
- latest CBR decision, statement, guidance and inflation forecast;
- weekly and monthly Russian inflation;
- inflation expectations;
- CBR meetings before the deadline.

### Russian fiscal and FX flow

Check:

- federal budget deficit/surplus;
- oil-and-gas revenues;
- non-oil revenues;
- Ministry of Finance FX/gold operations under the fiscal rule;
- Bank of Russia offsetting operations;
- tax-payment dates;
- quarter-end/year-end budget spending;
- exporter FX-sale requirements or incentives;
- new capital controls or FX restrictions.

### Oil, export revenue and infrastructure

Check:

- Brent;
- Urals or best available Russian realized-price proxy;
- discount to Brent where available;
- Russian crude export volumes;
- diesel and oil-product exports;
- refinery utilization/outages;
- ports, terminals, pipelines and tanker availability;
- attacks/damage to refineries and export infrastructure;
- sanctions affecting shipping, insurance, payments or buyers.

Do not equate high Brent with high Russian FX revenue automatically. Price, physical volume, discounts, logistics and payment frictions must be considered separately.

### Geopolitics and sanctions

Check:

- new US/EU/UK sanctions and enforcement changes;
- secondary-sanctions risk for major Russian energy buyers;
- waivers/licenses;
- negotiations affecting Russian energy exports;
- important changes on the Russia-Ukraine front;
- ceasefire or energy-truce negotiations;
- confirmed changes in attacks on energy/export infrastructure.

Treat contested battlefield or political claims as claims unless independently confirmed.

### Global USD

Check:

- Federal Reserve policy rate;
- latest FOMC decision and guidance;
- US CPI/PCE/payrolls and other rate-sensitive data;
- DXY or broad USD index;
- US Treasury yields;
- market-implied Fed expectations when credible.

## Forward catalyst calendar

Build a calendar from today to the deadline and mark:

- Russian tax-payment dates;
- CBR meetings;
- Fed meetings;
- CPI/PCE/payroll releases;
- Ministry of Finance FX-operation changes;
- Russian budget reporting;
- sanctions deadlines or waiver expirations;
- known negotiation dates;
- major oil-supply meetings or scheduled decisions.

Then identify windows where several factors could align to weaken RUB.

## Seasonality

When historical data is available, inspect:

- USD/RUB behavior from 1-15 December;
- behavior around Russian tax-payment periods;
- early/mid-December budget spending;
- year-end import demand;
- exporter FX sales;
- December CBR/Fed meetings.

Historical seasonality is supporting evidence only, never the primary reason for a forecast.

## Factor score

Score each factor from -2 to +2 for its effect on USD/RUB over the user's horizon.

- +2 = materially supports higher USD/RUB / weaker RUB
- +1 = modestly supports higher USD/RUB
- 0 = neutral / ambiguous / already priced
- -1 = modestly supports lower USD/RUB / stronger RUB
- -2 = materially supports lower USD/RUB

Buckets:

1. CBR / Russian rates
2. Russian inflation
3. Budget / fiscal spending
4. Ministry of Finance FX operations
5. Oil price
6. Russian export volumes
7. Refinery/export infrastructure
8. Sanctions/payment logistics
9. Russia-Ukraine negotiations/front
10. Fed / global USD
11. Seasonal/tax flows
12. Current price trend / momentum

Do not simply sum the score mechanically. Use it as a consistency check.

## Probability outputs

Always estimate touch-before-deadline probabilities:

- P(USD/RUB >= 91)
- P(USD/RUB >= 93)
- P(USD/RUB >= 95)
- P(USD/RUB >= 100)

Also estimate the deadline distribution:

- below 85
- 85-95
- 95-105
- above 105

Call these scenario probabilities unless a genuinely calibrated statistical model is being used.

Do not materially move probabilities because of one noisy daily datapoint unless it changes the regime.

## Local-maximum window

Always provide a likely window such as:

- Primary: 8-12 December
- Secondary: 3-5 December
- Confidence: low / medium / high

For each window explain why it might produce a weaker RUB, for example:

- tax-flow reversal;
- year-end fiscal spending;
- lower exporter FX sales;
- Fed/CBR event risk;
- oil move;
- sanctions catalyst;
- negotiation catalyst.

Never say "the peak will be on 11 December." Say "most likely local-maximum window."

## Decision rule for this user

### WAIT

Use when:

- USD/RUB is meaningfully below 91;
- P(touch 91 by deadline) remains high;
- credible RUB-negative catalysts remain ahead;
- there is no strong evidence the likely peak has already passed.

### START SELLING

Use when:

- USD/RUB reaches roughly 91-93;
- 91 is already satisfactory for the user;
- probability of 93-95 is only moderate or falling;
- the best catalyst window is close or already underway.

If sizing is useful, a partial exit can be discussed, but do not force a percentage unless requested.

### SELL MOST

Use when:

- USD/RUB reaches 93-96 and upside to 100 is not strongly supported;
- a major catalyst has just played out;
- probabilities of further upside are deteriorating;
- the deadline is close.

### Do not chase the perfect peak

If USD/RUB reaches 91 and either:

- P(93) is below about 45%, or
- P(95) is below about 25%, or
- the likely local-maximum window has already begun,

explicitly say that waiting for 93-95 has weak expected value relative to the user's stated goal.

These thresholds are heuristics, not laws.

## Expected-value sanity check

When useful, compare:

- benefit of waiting from 91 to 93/95;
- probability of achieving that level;
- risk of falling back below 91 before the deadline;
- remaining trading days.

Example:

If USD/RUB = 91.2, P(93 touch) = 38%, P(95 touch) = 18%, and five trading days remain, lean toward partial or major exit rather than maximizing theoretical upside.

## Technical analysis

Technical signals are supporting evidence only.

Allowed:

- short/medium moving averages;
- realized volatility;
- support/resistance;
- ATR;
- momentum;
- USD/RUB futures basis/proxies;
- CNY/RUB confirmation.

Do not let RSI/MACD override macro/flow fundamentals in USD/RUB.

## Evidence quality

Separate important claims into:

- **confirmed fact**
- **reported but not independently confirmed**
- **model inference / estimate**

Prefer:

- Bank of Russia
- Russian Ministry of Finance
- Rosstat
- Federal Reserve
- official sanctions authorities
- Reuters / Bloomberg / FT for market and infrastructure reporting

## Invalidation

Explicitly state what would invalidate the current exit plan, for example:

- Brent moves >10% and holds;
- CBR unexpectedly changes rate or guidance;
- Fed unexpectedly hikes/cuts;
- major sanctions hit Russian oil buyers/payments;
- ceasefire materially changes energy-infrastructure risk;
- a major Russian export terminal is disabled/restored;
- Ministry of Finance FX operations change sharply;
- USD/RUB breaks the assumed regime with sustained price action.

## Output order

### 1. Decision now
One line: **WAIT / START SELLING / SELL MOST**

Then one sentence why.

### 2. Current USD/RUB
- official CBR
- market proxy
- change since previous update

### 3. Target probabilities before deadline

| Level | Probability of touch before deadline | Change vs previous update |
|---|---:|---:|
| 91 | x% | +/- |
| 93 | x% | +/- |
| 95 | x% | +/- |
| 100 | x% | +/- |

### 4. Most likely local-maximum window
- Primary window
- Secondary window
- Confidence
- Why

### 5. Forecast for deadline
- Base range
- Central estimate
- below 85 / 85-95 / 95-105 / above 105 probabilities

### 6. What changed
Only the 3-6 factors that materially changed the forecast.

### 7. Practical exit logic
Explicitly answer:

- If USD/RUB reaches 91 today, should the user sell?
- What would justify waiting for 93-95?
- What would make the skill advise selling before 91?

### 8. Next catalysts
Only events that can materially change the exit decision.

## Tone

- concise and concrete
- no hype
- no false certainty
- no fake precision
- if evidence does not justify a forecast change, say **"Base forecast unchanged."**
- keep the 91 RUB/USD practical exit target visible in the conclusion

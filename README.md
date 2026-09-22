# Lifesum — onboarding & paywall rebuild

A clickable HTML prototype that re-sequences [Lifesum](https://lifesum.com/)'s onboarding and
paywall to increase conversion, and adds an offer paywall on close.

**Live:** https://bterzic123.github.io/lifesum-flow-rebuild/

## What this is

The art direction is Lifesum's, extracted from capture frames of their shipping flow — cream
surface, green control, forest-green brand screens, 8px control radius, their three-column wheel
pickers, their footer chrome, their FREE-vs-PREMIUM comparison table. **Only the sequence changed.**

- **Prototype tab** — 24 screens, all clickable, real transitions, phone frame. Side panel per
  screen: rationale, what was kept from their app, where it sat in the shipping flow, expected
  impact range.
- **Before → After tab** — the 29-screen shipping flow beside the 25-screen rebuild, every step
  tagged KEPT / MERGED / CUT / MOVED, plus the ranked change table.
- **Jump chips** under the phone drop a prospect on any stage with answers pre-filled. The offer
  paywall has its own chip.

## The headline changes

| # | Priority | Change | Expected impact |
|---|----------|--------|-----------------|
| 1 | Fix first | No trial appears anywhere in the shipping flow, though Apple lists all three Lifesum SKUs as carrying one. Closing the paywall now re-offers the $49.99 annual as a free trial, with a downsell to $7.49/mo | ARPU +10–15% |
| 2 | Fix first | Sign-up sat between the loader and the payoff. Account creation moved past the paywall; the plan is delivered first | CR +8% · ARPU +17% |
| 3 | High | The paywall headline used the user's name but never the goal fourteen screens collected | CR +15–20% |
| 4 | High | Apple Health fired at screen 6, before any value was established. Moved past the purchase | CR +10–15% |
| 5 | High | The loader counted to 100 and said nothing. It now names the actual answers as it works | CR +10–15% |

Nine ranked rows in total — see the Before → After tab.

## Grounding

Every price, rating, award, quote and partnership comes from Lifesum's own published material or
Apple's listing of their app. Nothing is invented. The **Sources & grounding** button in the
header lists each one with its origin.

All photography is Lifesum's own — lifestyle shots from their CDN via lifesum.com, food shots
cropped out of their own App Store screenshots (which is also where the 856 / 1,712 kcal figures
and the "Good morning" coaching copy come from).

Two things deliberately left as slots rather than filled with a plausible number:

- **Trial length.** Apple tags all three SKUs "Trial" but does not publish the duration, so the
  offer timeline reads "Today — $0 charged" / "Before your trial ends" rather than inventing a
  day count.
- **"5x more likely to achieve lasting results"** is Lifesum's own paywall claim, kept verbatim.
  Not generated here, and the study behind it has not been verified.

Impact ranges are Adapty's expected effect from teardowns and A/B tests across subscription apps —
**not** measured lift for Lifesum.

## Running it locally

```bash
python3 -m http.server 8921
```

Then open http://127.0.0.1:8921 — it is a single static `index.html` plus the `img/` folder.

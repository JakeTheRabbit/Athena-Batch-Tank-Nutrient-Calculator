# Athena Grow Calculator

**🚀 [Use the live calculator](https://jaketherabbit.github.io/Athena-Batch-Tank-Nutrient-Calculator/)** · also at [athena.legacy.ag](https://athena.legacy.ag)

A precision dosing calculator for the full [Athena](https://support.athenaag.com/hc/en-us/articles/17190427112859-Pro-Line-Feed-Schedules) nutrient, foliar and cleaning range. Five phone-first tools — feed tank, foliar spray, stock-tank planning, pH correction and cleaning reference — that scale Athena's official schedules to any reservoir, from a 20 L tent to a 1,000 L commercial stock tank, with no manual math.

**Disclaimer:** Independent tool — not affiliated with, endorsed, or sponsored by Athena Agriculture. All product names are trademarks of their owners. Verify every mix against the official label. Use at your own risk.

## The five tools

Bottom-tab navigation, everything reachable one-handed on a phone.

### 🥤 Feed — reservoir nutrient batch
- **Exact Athena dosing.** Doses come from Athena's *Metric Dosage Reference Guide* grams-per-10 L master, divided by your stock strength. This reproduces **both** Athena's published metric (226 g/L) and imperial (240 g/L) ml tables to the digit, at any target EC (linear interpolation between chart anchors).
- **Real growth-stage schedule.** Clone / Veg / Flower / Finish / Flush set the EC, pH, Cleanse rate and product pair from Athena's Pro Program. Clone & flower run on Bloom + Core, veg on Grow + Core, finish swaps Core → Fade. Athena runs a **hard Grow→Bloom switch** — the A-parts (Grow/Bloom) and B-parts (Core/Fade) are pick-one, not blended.
- **Balance buffer, three ways** — *Blended* (liquid potassium silicate, also feeds Si), *Pro* (dry potassium carbonate for venturi/Netaflex), or *Both* — Athena's official procedure of dissolving Pro Balance powder into Blended Balance to boost pH-up, capped at 48 g/L (180 g/gal).
- **Supplements** — CaMg (RO / inert media) and PK (no-N flower booster, week 3+).
- **Cleanse in reservoir**, source-water EC offset, mixed stock strengths per product, and a **top-up calculator** (tank reads EC 2.4, target 3.0 → exact ml to add, or litres of water to dilute if you overshot).

### 🌿 Foliar — spray tank (separate from feed)
IPM / IPW, Stack foliar and Cleanse surface spray, with one-tap presets (IPM preventative 90 ml/gal, IPM pressure 120 ml/gal, the compatible IPM + Stack tank-mix, Stack, Cleanse wipe-down) and the full spray SOP — saturate the substrate first, lights-off, dry 3–4 h. Kept out of the feed tank, the way most growers run it (Athena also publishes an optional IPM root-drench at 5–10 ml/gal).

### 🛢️ Stock — concentrate builder + tank life
- **Concentrate builder** — target strength (120 / 226 / 240 / 300 g/L) × tank size → kg of product to add, with the fill-to-80%-then-top procedure and the 300 g/L agitation warning.
- **Tank life / refill date** — stock size, strength, feed EC and either batches-per-day or litres-per-day → how many days and weeks the stock lasts, daily draw, total feed supported, and the **calendar refill date**.

### 🧪 pH — Balance correction estimator
Estimate the Balance dose to move current pH → target at a given EC. Athena publishes **no** fixed ml-per-pH figure (it depends on your water and recipe), so the tool uses their own titrate-and-record method: it estimates, then **learns from your logged corrections per profile** to sharpen the next estimate.

### ⚙️ More — cleaning, recipes, history, settings
Cleanse reservoir/flush use-cases and the separate Clean Line (Renew / Reset / Perafoam) between-crop protocols; saved recipes; history with CSV export; PPM scale (500/700); and the replayable walkthrough.

## Built for one hand on a phone

- Fixed bottom-tab navigation and a sticky Calculate bar — thumb-reachable.
- Big steppers and sliders so most inputs need no keyboard; **recent-value chips** and per-profile recommendations to speed re-entry.
- Results slide up in a sheet with **Mix mode** (tap-to-tick, correct order: Balance first → Cleanse → base nutrients → Fade → supplements, check pH last) and Share.
- Profiles (Garage / Craft / Commercial) set sensible scale defaults and remember your tank sizes.
- Guided tour on first run, tooltips on every input, Athena-inspired dark theme.
- Metric ⇄ Imperial toggle (converts the display; dosing is driven by the stock strength you pick, matching Athena's separate metric/imperial standards).

## Embedding

Single self-contained HTML file — drop it into any site:

```html
<iframe src="https://jaketherabbit.github.io/Athena-Batch-Tank-Nutrient-Calculator/?embed=1"
        style="width:100%;border:0" id="athena-calc"></iframe>
```

`?embed=1` hides the header chrome.

## Standalone / offline

No installation, no build, no backend, no accounts. Download [`www/index.html`](www/index.html) and open it in any modern browser — everything runs client-side and persists to `localStorage`. On a phone, use **Add to Home Screen** for a fullscreen app.

## Development

- `www/index.html` — the app (single file: HTML + CSS + vanilla JS, zero dependencies).
- `docs/index.html` — identical copy served by GitHub Pages. **Keep both in sync** when editing.

All dosing figures are cross-verified against Athena's official Feed Schedule, Dosage Reference Guide (doc A01.004), store.athenaag.com and support.athenaag.com. Doses between chart anchors are linear interpolations; EC below the chart floor is flagged as extrapolated. Rates marked *SEED* in-app are conservative pending label confirmation.

## License

MIT

# Athena Grow Calculator

A dosing calculator for the full Athena nutrient, foliar and cleaning range. Runs in your browser, works offline, and scales any recipe from a 20 litre tent to a 1000 litre commercial stock tank. Built for a phone, one-handed, tank-side.

**Open it: [jaketherabbit.github.io/Athena-Batch-Tank-Nutrient-Calculator](https://jaketherabbit.github.io/Athena-Batch-Tank-Nutrient-Calculator/)**

![Athena Grow Calculator](img/hero.png)

Not affiliated with, endorsed by, or sponsored by Athena Agriculture. All product names are trademarks of their owners. Verify every mix against the official label.

## What it does

Five tools, one page, switched from a bottom bar you can reach with your thumb. Everything runs client-side. No account, no backend, no data leaves your phone.

### Feed - reservoir nutrient batch
- Doses come from Athena's own grams-per-10L reference divided by your stock strength, so the numbers match both the metric (226 g/L) and imperial (240 g/L) published tables exactly, at any target EC.
- Growth stage sets the EC, pH, Cleanse rate and the product pair from Athena's Pro schedule. Clone and flower run on Bloom and Core, veg on Grow and Core, finish swaps Core for Fade. Athena runs a hard Grow to Bloom switch, so the A-parts and B-parts are pick-one, not blended.
- Balance three ways. Blended liquid, Pro dry stock, or Both - Athena's procedure for dissolving Pro Balance powder into Blended Balance, capped at 48 g/L.
- CaMg and PK supplements, Cleanse in the reservoir, a source-water EC offset, and mixed stock strengths per product.
- Top-up calculator. Tank reads EC 2.4 and you want 3.0, it gives the exact millilitres of each part to add. Overshot, it gives the litres of water to dilute with.

### Foliar - spray tank
IPM (now IPW), Stack foliar and Cleanse surface spray, with one-tap presets for IPM preventative, IPM pressure, the IPM and Stack tank-mix, Stack, and a Cleanse wipe-down. Full spray procedure included - saturate the substrate first, lights off, dry three to four hours. Kept out of your feed tank by default, the way most people run it.

### Stock - concentrate builder and tank life
- Build a concentrate stock by target strength and tank size. It gives the kilograms of product to add and the mixing steps.
- Plan how long a stock tank lasts. Feed it your stock size, strength and daily feed volume and it returns the days and weeks of runway, the daily draw, the total feed supported, and the calendar date you refill.

### pH - Balance correction estimator
Estimate the Balance dose to move current pH to your target at a given EC. Athena does not publish a fixed millilitres-per-pH figure because it depends on your water and recipe, so the tool uses their own method - titrate, record, and it learns your water from each correction you log, per profile.

### More
Cleanse and Clean Line (Renew, Reset, Perafoam) cleaning protocols, saved recipes, calculation history with CSV export, PPM scale, and the walkthrough you can replay any time.

## Built for a phone

- Bottom-tab nav and a sticky Calculate bar, all in thumb reach.
- Big steppers and sliders so most inputs need no keyboard. Recent-value chips and per-profile suggestions to speed re-entry.
- Results slide up in a sheet with Mix mode - tap each addition off in the correct order (Balance first, then Cleanse, base nutrients, Fade, supplements, check pH last).
- Profiles for Garage, Craft and Commercial set sensible defaults and remember your tank sizes.
- Light and dark themes with a toggle in the header. Follows your phone's setting by default.
- A guided tour on first run, tooltips on every input, and it installs to your home screen as an app.

## How to use it

1. Pick a growth stage. EC, pH and the product pair fill in.
2. Slide the target EC and enter your tank size.
3. Set the stock strength each concentrate was mixed at. Grow, Bloom, Core and Fade can each differ.
4. Choose your Balance product and rate. Use the pH tab if you want the dose estimated.
5. Hit Calculate. Doses slide up with per-10L or per-gal rates and dry-gram equivalents.
6. Tap Mix mode at the tank and tick each addition off as you pour.

Switch Metric and Imperial in the top bar. The number converts, the dose does not - dosing is driven by the stock strength you pick, which is how Athena's separate metric and imperial standards work.

## How it works

Every dosing figure is cross-checked against Athena's official Feed Schedule, Dosage Reference Guide (doc A01.004), and the store and support pages. Base nutrient doses use the grams-per-10L master divided by the chosen stock strength, which reproduces both published rate tables to the digit. Doses between the chart's EC anchors are linear interpolations. EC below the chart floor or above the top anchor is flagged. A handful of rates that the source could not confirm are marked SEED in the app.

## Run it offline

No install, no build, no accounts. Download [`www/index.html`](www/index.html) and open it in any modern browser. Everything runs client-side and saves to your browser's local storage. On a phone, use Add to Home Screen for a full-screen app.

## Embed it

Single self-contained file, drops into any site:

```html
<iframe src="https://jaketherabbit.github.io/Athena-Batch-Tank-Nutrient-Calculator/?embed=1"
        style="width:100%;border:0" id="athena-calc"></iframe>
```

`?embed=1` hides the header chrome and the page posts its height to the parent on resize.

## Want a change or a new feature

Open an issue. [New issue](https://github.com/JakeTheRabbit/Athena-Batch-Tank-Nutrient-Calculator/issues/new/choose).

- Feature or product request - tell me the product, the rate, and the source (a label photo or an Athena page). Rates need a source before they go in.
- Bug - tell me the phone and browser, what you did, what you expected, and what happened.

Pull requests are welcome too.

## For developers

- `www/index.html` is the app. One file, HTML plus CSS plus vanilla JavaScript, zero dependencies.
- `docs/index.html` is an identical copy served by GitHub Pages. Keep both in sync when you edit.

## License

MIT. See [LICENSE](LICENSE).

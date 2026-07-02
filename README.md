---
title: US Tax Explorer
emoji: 💸
colorFrom: indigo
colorTo: green
sdk: static
pinned: false
license: mit
thumbnail: thumbnail.png
short_description: US take-home pay by state, visa status, 401k & Roth
---

# 💸 US Tax Explorer

Estimate your US take-home pay across states based on your compensation mix and
immigration/tax-residency status — and see, live, how 401(k), Roth 401(k), Roth IRA /
backdoor, HSA, and mega-backdoor Roth contributions change your taxes.

**One HTML file. No backend, no build step, no tracking.** Everything runs in your
browser and nothing you type ever leaves your device.

**▶️ Live app:** https://harshith99-comp-tax-explorer.static.hf.space

![screenshot](thumbnail.png)

## Quick start (how to use)

1. **Enter your pay** (top-left): base salary, bonus, RSU, ESPP. Pick your **filing
   status**, **visa / residency status**, and **state**.
2. **Read your take-home** at the top — gross, total tax, net pay, and your
   effective/marginal rate — plus a line-by-line breakdown of where each dollar goes.
3. **Drag the tax-shelter sliders** — Traditional 401(k), Roth 401(k), HSA, Roth IRA /
   backdoor, and mega-backdoor Roth. Each one shows its live tax impact:
   *green = lowers your tax now*, *blue = grows tax-free later*.
4. **Compare** take-home across 15 states and across 401(k) strategies in the tables.
5. **Per-paycheck calculator** — enter your salary per check and a target take-home, and
   it outputs the exact **percentages** to set for pre-tax / Roth / after-tax at your
   provider (Fidelity, Vanguard, etc.), plus a "cost of waiting" figure.
6. **Projection** — see where your Roth vs Traditional dollars land at retirement.
   Tick **Fair comparison** to invest Traditional's up-front tax savings in a taxable
   side account for a true apples-to-apples comparison.
7. **🔗 Copy share link** — every input is encoded in the URL, so you can bookmark or
   share your exact scenario. Opening the link restores it.

## Features

**💰 Full take-home breakdown**
- Federal income tax, state tax, and FICA (Social Security + Medicare, incl. the Additional Medicare surtax) in one view
- Enter your real comp mix: base, bonus, RSU, and ESPP (with purchase discount)
- Effective *and* marginal rate, plus a visual "where every dollar goes" bar

**🛂 Visa & residency aware** — rare in tax tools
- US citizen, green card, H-1B / L-1 / O-1, TN (USMCA), and F-1 / J-1 nonresident
- Correctly models FICA exemption for nonresident students and standard-deduction eligibility

**🎚️ Live contribution sliders**
- Traditional 401(k), Roth 401(k), HSA, Roth IRA / backdoor, and mega-backdoor Roth
- Drag any one and watch your tax change instantly — *green = saves tax now, blue = grows tax-free later*
- Enforces the ~$23.5k elective limit, $70k §415(c) cap, and IRA/HSA limits, with over-contribution warnings
- Detects when your income requires a **backdoor** Roth IRA, and flags state HSA quirks (CA/NJ)

**🗺️ Compare 15 states at once**
- Take-home ranked by state, including no-income-tax states — great for relocation or offer decisions

**⚖️ 401(k) strategy comparison**
- No-401k vs. pre-tax-max vs. pre-tax + mega-backdoor, side by side, with a true "net worth added this year" metric

**🧮 Per-paycheck contribution calculator**
- Enter your paycheck and a target take-home → get the exact **%** to set for pre-tax / Roth / after-tax at Fidelity, Vanguard, etc.
- **"Cost of waiting"** readout: the extra tax you've paid by contributing Roth instead of pre-tax so far this year

**📈 Retirement projection**
- Grows this year's contributions to retirement, split Roth vs. Traditional, showing *spendable* (after-tax) value
- **Fair-comparison mode** invests Traditional's up-front tax savings in a taxable side account for a true apples-to-apples result

**🔗 Shareable & private by design**
- Every input is encoded in the URL — bookmark or share your exact scenario with one click
- **100% client-side:** no backend, no account, no tracking — nothing ever leaves your browser
- One HTML file, no build step, open source (MIT)

## Run it locally
It's a single static file — just open it:
```bash
git clone https://github.com/harshithbelagur/comp-tax-explorer.git
cd comp-tax-explorer
open index.html      # or double-click it, or: python3 -m http.server
```

## Contributing
Everything lives in `index.html` (markup, styles, and logic in one file). Tax constants
(brackets, limits, state data) are near the top of the `<script>` block and are easy to
update each tax year. PRs welcome — especially more states, newer IRS figures, and
additional filing situations.

## Disclaimer
Educational estimates only — **not tax, legal, or financial advice**. Uses simplified
2025 federal, FICA, and state figures; ignores local/city taxes, AMT, credits, and
capital-gains nuances. Verify with a qualified CPA before making decisions.

## License
[MIT](LICENSE) — free to use, modify, and share.

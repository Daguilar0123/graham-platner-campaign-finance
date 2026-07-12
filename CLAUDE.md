# CLAUDE.md — operating rules for AI agents in this repo

Instructions for an AI coding agent working on **"The Money"** — the FEC independent-expenditure
ledger. See [README.md](README.md) for what this is. This is the sibling of
`graham-platner-the-record`; the **full project architecture and rules live in that repo's
[ARCHITECTURE.md](https://github.com/Daguilar0123/graham-platner-the-record/blob/main/ARCHITECTURE.md)
and CLAUDE.md** — read them. This file carries only what's specific here.

If a rule here conflicts with a direct request from the owner in chat, the owner wins — but say so.

## Rules specific to this repo

- **This is a neutral ledger. It draws no conclusions** about any candidate, committee, or donor,
  and endorses no side. Every change must preserve that neutrality — this repo's independence is
  exactly why it's kept separate from the editorial site. Do not import the editorial standpoint
  here.
- **Figures are sourced facts.** Totals, ratios, and vendor/committee details trace to FEC
  filings (candidate ID `S6ME00373`) and cited press. Don't alter a figure without its source;
  note the compile date (later amendments may change totals).
- Single-file static HTML/CSS/JS, no build (same as the sibling — see its ADR-0003).

## Cross-repo contract

- Live at `https://daguilar0123.github.io/graham-platner-campaign-finance/`.
- The **projnav** strip links to the sibling's absolute URLs (`…/graham-platner-the-record/`,
  `…/the-record.html`, `…/fifield-kavanaugh.html`) and must stay byte-identical, in the same
  order, as the projnav on all four project pages. Restyle/reorder happens on all four at once.

## Git

- **Never push without the owner's explicit go-ahead.** This repo is live; a push to `main`
  publishes within ~1 minute.
- **Always `git pull --rebase origin main` before pushing** — merged PRs (e.g. a past
  dark-mode contrast fix) land remotely and must be replayed under local commits.
- End commit messages with the `Co-Authored-By:` trailer for the model you are.

## Preview + verification

`python3 -m http.server 8137 --directory <repo>` (config: project-root `.claude/launch.json`,
name `money-page`). Before "done": valid render, **zero console errors**, both color schemes at
mobile + desktop, **WCAG AA contrast in dark mode** (a dark-mode contrast bug shipped here once —
`.fnode.pac` / `.vtag.press` — do not repeat it).

*Maintainer: Daniel Ismael Aguilar · https://grownfromconcrete.org*

# Frontier AI Controls Dashboard

An interactive, single-file dashboard summarizing the security controls that most
reduce **frontier-AI risk** for a large regulated bank — the controls ranked by
risk-reduction value, the leading vendors mapped to each, a relative vendor
comparison, third-party expectations, and the desired end state.

It is a self-contained briefing tool: one `index.html` with no build step, no
dependencies, and no server required.

## Views

- **Overview & Methodology** — how frontier AI changes the risk, what the dashboard covers, and how the rankings/tiers/vendor lists were built.
- **Control Rankings** — the ten controls ranked by risk-reduction value, each with why it ranks there, the required shift, what to measure, and supporting vendors.
- **Leading Vendors** — representative market leaders across all control domains, with strengths, considerations, and references.
- **Vendor Comparison** — a relative 1–5 read of same-category peers on capability, autonomy, maturity, and enterprise scale.
- **Third-Party Expectations** — what to expect from vendors, scaled by tier, with survey questions, good answers, and red flags.
- **End State** — five statements that define "done," and the evidence each audience (board, regulators, exec committee, clients) sees.

## Running it

Just open `index.html` in any modern browser — double-click it, or serve the folder:

```bash
python -m http.server 8765
# then visit http://localhost:8765/index.html
```

The dashboard is responsive: a desktop sidebar layout, and on mobile a top app bar
with a hamburger menu and search.

### Deep links

Each view is addressable via the URL hash — e.g. `index.html#/controls/7`,
`index.html#/tools/Identity`, `index.html#/compare` — so a specific control or
vendor is a shareable link.

## Editing the content

All content lives in a clearly marked `===== DATA =====` section near the top of the
`<script>` block in `index.html`. Controls, vendors, comparison scores, third-party
expectations, and the end-state pillars are plain JavaScript objects/arrays — edit
them and reload. Design tokens (colors, fonts, radii) live in the `:root` block in
the `<style>` element.

## Sources & disclaimer

Built entirely from publicly available information — vendor websites, public
benchmarks, press coverage, and analyst commentary (see each vendor card's
references). It contains no non-public data. Rankings and vendor lists reflect a
point-in-time view of a fast-moving market and are a decision aid, not a control
assessment or a procurement recommendation.

# SITE-Paysavr

Landing / waitlist site for **paysavr.com** — Paysavr, a bill/subscription
audit + savings app (validation phase, pre-product).

- Static HTML, GitHub Pages (main branch, root). No build step, no JS
  dependencies, no analytics, no third-party requests.
- Waitlist = a `mailto:hello@paysavr.com?subject=Waitlist` CTA. Signups land
  in the monitored support mailbox (see
  `VNTR-Perpetua/company/ops/graph-mail-paysavr/`). Nothing is collected on
  the site itself — that's the privacy story on `privacy.html`, keep it true.
- Custom domain: paysavr.com (BB-owned). DNS handoff doc:
  `VNTR-Perpetua/company/state/paysavr-dns-handoff-2026-07-22.md`.
  Until DNS lands, staged at https://animum-rege.github.io/SITE-Paysavr/
  (relative links only, so both URLs work).

Guardrails (validation brief 2026-07-22): no financial advice, no financial
data collected, no Plaid/fintech code in this repo — this phase proves demand
only.

© 2026 Animum Rege LLC.

# SITE-Paysavr

Landing / waitlist site for **paysavr.com** — Paysavr, a bill/subscription
audit + savings app (validation phase, pre-product).

- Static HTML, GitHub Pages (main branch, root). No build step, no JS
  dependencies, no analytics, no third-party requests. Hosting decision
  settled 2026-07-23: Pages over Azure Static Web Apps (apex works with
  plain A records at any registrar).
- Waitlist = email-capture form (email + explicit consent checkbox +
  honeypot) POSTing to our own Azure Function:
  `https://paysavr-waitlist-func.azurewebsites.net/api/waitlist` (code:
  `VNTR-Perpetua/company/ops/paysavr-waitlist-fn/`). Stores email + consent
  + timestamp only. mailto:hello@paysavr.com remains the fallback/noscript
  path; that mailbox is monitored (see
  `VNTR-Perpetua/company/ops/graph-mail-paysavr/`). The privacy claims on
  `privacy.html` mirror exactly what the function stores — change one →
  change both.
- Custom domain: paysavr.com (BB-owned). DNS handoff doc:
  `VNTR-Perpetua/company/state/paysavr-dns-handoff-2026-07-22.md`.
  Until DNS lands, staged at https://animum-rege.github.io/SITE-Paysavr/
  (relative links only, so both URLs work).

Guardrails (validation brief 2026-07-22): no financial advice, no financial
data collected, no Plaid/fintech code in this repo — this phase proves demand
only.

© 2026 PaySavr

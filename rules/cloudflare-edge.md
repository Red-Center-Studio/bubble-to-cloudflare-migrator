---
trigger: model_decision
description: Apply only when working on a Bubble-to-Cloudflare migration. Enforces credential, billing consent, D1/R2 data safety, and cutover guardrails for nc_ migrator tools.
---

Apply only when working on a Bubble-to-Cloudflare migration. Do not apply these rules to unrelated projects.

- Never ask for or paste Cloudflare tokens, R2 S3 keys, Bubble Data API tokens, or passwords in chat; always direct the owner to the one-time `nc_connect` link.
- Never pass `go_ahead: true`, `upgrade: true`, `confirm_overwrite: true`, `confirm_deploy: true`, `confirm_cutover: true`, or `confirm_price_usd` without first showing the exact cost/action and obtaining explicit owner confirmation in chat.
- Keep default-deny authorization on every `MANUAL` privacy rule emitted by `nc_access` until reviewed and tested.
- Never proceed to `nc_cutover` until `nc_verify` passes with no subsequent exports, loads, or file copies, and remind the owner that DNS changes happen manually in Cloudflare (rollback steps stay available).

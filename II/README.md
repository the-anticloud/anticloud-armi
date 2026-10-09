# Independent Insurance — ARMI

**Project:** ARMI  
**Category:** OIL_GAS  
**Upstream:** https://github.com/terrapower/armi  
**Pinned commit:** `17c322a13039b2ac5354aec65f9828f7580d9959`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `5e7127328d160bf162e2f376098f4f3e512d23f7161fd4bdcbbe9f9c09c70f9c`  
**Date:** October 2026

## Why AI-specific cover matters

Deploying AI in a regulated sector creates liability surfaces that ordinary
technology cover does not reach: inference liability, audit-trail liability,
data-breach liability and IP-infringement liability.

## How this project's architecture reduces insurable risk

| Risk | Cloud AI | ARMI with AIOSS |
|---|---|---|
| Audit-trail loss | high — vendor-controlled logs | low — append-only chain, verifiable offline |
| Data breach in transit | high — data transits external servers | low — no external endpoint |
| Compliance violation | high — cannot satisfy air-gap requirements | low — structural |
| IP liability | moderate | low — pinned provenance chain |

## Evidence package for an insurer

- AIOSS chain verification for head `5e7127328d160bf162e2f376098f4f3e512d23f7161fd4bdcbbe9f9c09c70f9c`
- The 16-check register with per-check evidence hashes
- Framework control mapping in `BENCH.json`

## Contact

lois@0-1.gg

# Students — ARMI

**Project:** ARMI  
**Category:** OIL_GAS  
**Upstream:** https://github.com/terrapower/armi  
**Pinned commit:** `17c322a13039b2ac5354aec65f9828f7580d9959`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `5e7127328d160bf162e2f376098f4f3e512d23f7161fd4bdcbbe9f9c09c70f9c`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `17c322a13039b2ac5354aec65f9828f7580d9959`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `5e7127328d160bf162e2f376098f4f3e512d23f7161fd4bdcbbe9f9c09c70f9c`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.

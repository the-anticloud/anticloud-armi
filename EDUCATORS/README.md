# Educators — ARMI

**Project:** ARMI  
**Category:** OIL_GAS  
**Upstream:** https://github.com/terrapower/armi  
**Pinned commit:** `17c322a13039b2ac5354aec65f9828f7580d9959`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `5e7127328d160bf162e2f376098f4f3e512d23f7161fd4bdcbbe9f9c09c70f9c`  
**Date:** October 2026

## Teaching with ARMI

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `5e7127328d160bf162e2f376098f4f3e512d23f7161fd4bdcbbe9f9c09c70f9c` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.

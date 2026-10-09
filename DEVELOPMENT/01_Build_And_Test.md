# Build and Test

**Project:** `ARMI`
**Upstream:** https://github.com/terrapower/armi
**License:** Apache 2.0

## Quick Start

```bash
git clone https://github.com/terrapower/armi
cd armi
pip install -r requirements-anticloud.txt
python anticloud_main.py --offline --pax-local
```

## Anticloud Improvements Applied

1. PAX L5 Narrow L2 General 27B anomaly detection on sensor streams — air-gapped deployment
2. AIOSS tamper-evident log for all sensor readings and safety events
3. Single-binary edge deployment for RTUs and SCADA endpoints
4. AES-256 encryption for all field data at rest and in transit
5. Offline predictive maintenance inference — no cloud ML APIs
6. Zero-dependency alert routing: replaces PagerDuty/cloud escalation with local daemon
7. GPU/CPU equalizer: runs on embedded ARM CPU in field or GPU at operations center
8. Modbus/OPC-UA adapter layer added to upstream TCP-only implementations

## Benchmark Targets

| Metric | Target |
| --- | --- |
| Latency | Sensor anomaly alert: <500ms end-to-end |
| Throughput | 10,000 sensor readings/sec ingested locally |
| Memory | <8GB edge server RAM |
| Accuracy | Anomaly detection F1 >0.92 on held-out field data |

## Build Status

Not yet measured. Run verified build and record actual figures above.

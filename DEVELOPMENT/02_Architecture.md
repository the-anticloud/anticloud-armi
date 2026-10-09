# Technical Architecture — ARMI

**Upstream:** [https://github.com/terrapower/armi](https://github.com/terrapower/armi)
**License:** Apache 2.0
**Category:** OIL_GAS
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

Nuclear/reactor analysis framework (also used in energy)

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B anomaly detection on sensor streams — air-gapped deployment
2. AIOSS tamper-evident log for all sensor readings and safety events
3. Single-binary edge deployment for RTUs and SCADA endpoints
4. AES-256 encryption for all field data at rest and in transit
5. Offline predictive maintenance inference — no cloud ML APIs
6. Zero-dependency alert routing: replaces PagerDuty/cloud escalation with local daemon
7. GPU/CPU equalizer: runs on embedded ARM CPU in field or GPU at operations center
8. Modbus/OPC-UA adapter layer added to upstream TCP-only implementations

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_armi.spec` or `go build -o armi`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |
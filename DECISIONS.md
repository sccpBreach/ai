# Architecture Decisions

## ADR-001

Date:
2026-06-11

Decision:
Evolution Layer dibuat sebagai service layer tambahan.

Reason:
Agar tetap kompatibel dengan upstream OpenCode.

Status:
Accepted

## ADR-002

Date:
2026-06-11

Decision:
Tidak inject memory langsung ke system prompt.

Reason:
Menghindari context overload.

Impact:
Evolution Context dibuat sebagai layer terpisah.

Status:
Accepted

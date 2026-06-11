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

## ADR-003

Date:
2026-06-11


Title:
Evolution Brain Consumer Interface


Decision:

Phase 1 Evolution Brain hanya menyediakan data service.

Consumer berikutnya harus melalui Evolution.Service facade.


Current contract:

Evolution.Service
    |
    +-- getProjectContext()
    |
    +-- getMemories()
    |
    +-- getDecisions()


Phase 2 Context Intelligence akan menjadi consumer pertama.


Reason:

Prevent direct dependency between agents/session and storage layer.


Impact:

Memory implementation dapat berubah tanpa mempengaruhi consumer.

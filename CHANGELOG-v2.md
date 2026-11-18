# Agency Agents v2 — Changelog

- **Before:** 283 agents in 18 divisions.
- **After:** 334 agents in 26 divisions (+51 new agents, +8 new divisions).
- **Rewritten / upgraded:** 41 existing agents (all lint warnings resolved; thin agents expanded to 1,400+ words; outdated facts corrected). Names unchanged, so existing installs keep working.

## New divisions
| Division | Agents |
|---|---|
| legal | 7 |
| people-ops | 6 |
| education | 6 |
| data-science | 6 |
| manufacturing | 7 |
| agribusiness | 6 |
| media-journalism | 6 |
| latam | 7 |

## Checks
- `scripts/lint-agents.sh`: 0 errors, 0 warnings (334 files) — v1 had 58 warnings.
- `scripts/check-agent-originality.sh`: PASSED (no near-duplicates).
- `scripts/check-divisions.sh`, `scripts/check-tools.sh`: PASSED.
- `scripts/test-convert-outputs.sh`: 32 passed, 0 failed (334 agents × 15 tools); manifest regenerated.

# Session 17: prompt evaluation - v1 baseline vs v2 structured

Answering model: `openai/gpt-oss-20b` · Judge model: `openai/gpt-oss-20b` · Date: 2026-10-22

| Criterion | v1 (S14 baseline) | v2 (S16 structured) |
|---|---|---|
| Correct label | 15/20 = 75% | 19/20 = 95% |
| Cites the right house rule | 13/20 = 65% | 16/20 = 80% |
| Follows the reply format | 20/20 = 100% | 20/20 = 100% |
| Invents no policy | 20/20 = 100% | 20/20 = 100% |
| **All four criteria** | **13/20 = 65%** | **16/20 = 80%** |

Tickets graded: v1 20/20 · v2 20/20 (a ticket the judge could not parse is not counted, and is listed below).

Human spot-check: judge and human agreed on 19/20 = 95% of graded criteria (19/20).

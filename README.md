# Self-Healing Agents

**A Failure-Derived Training Methodology for Reliable Domain AI Systems**

Technical Whitepaper — Swarm & Bee LLC, March 2026

## The Paper

**[Read the whitepaper (PDF)](self_healing_agents_whitepaper_v2.pdf)**

## What We Found

AI coding assistants now write the training pipelines for AI models. Who validates the validator?

We found that an AI-assisted data assembly pipeline had introduced 56% duplication and 63% eval contamination — undetected across two model training runs and fifteen manual audits. We then audited our entire corpus:

| Metric | Before Audit | After Audit |
|--------|-------------|-------------|
| Reported CRE pairs | 2,811,588 | 807,331 verified |
| Empty/broken records | Unknown | 889,657 removed |
| Eval contamination | Unknown | 63% (fixed to 0%) |
| Noise removed | — | 72% |

## What We Built

In a single development session (14 hours), we went from "every number we've published is wrong" to a verified, production-ready data asset:

| Asset | Verified Pairs | Avg Score | Grade |
|-------|---------------|-----------|-------|
| CRE (21 task types) | 807,331 | 87.4 | Honey |
| Medical (31 specialties) | 418,783 | 84.8 | Cluster |
| Failure Intelligence (8 modes) | 5,278 | 77.1 | Cluster |
| **Total** | **1,231,392** | | |

Every pair is stamped with a unique cell ID, content fingerprint, quality score, tier assignment, and provenance chain — anchored to a Merkle-rooted Master HoneyCard.

## Key Contributions

1. **hive/validate.py** — 5-check pre-train data validation (dedup, contamination, distribution, source tags). Open source at [Swarm-Hive](https://github.com/SudoSuOps/Swarm-Hive).

2. **hive/verify.py** — Post-operation verification. Never trust "done." Verify with a read-back.

3. **The Hive Taxonomy** — Quality scoring framework: Genesis (95+) → Honey (85+) → Cluster (70+) → Cell (50+) → Swarm (<50). Makes training data comparable, verifiable, and priced by quality.

4. **The Self-Healing Loop** — Model failures become training data for the next version. Failure-derived pairs systematically improve agent reliability.

5. **The Honey Warehouse** — Production infrastructure turning verified pairs into a sellable product with catalog API, fulfillment engine, Merkle proof delivery, and customer verification. Code at [hive-warehouse](https://github.com/SudoSuOps/hive-warehouse).

## The Thesis

> *The slop is everywhere. Maybe that's the design. The question is whether you have the tools to find it.*

## Related Repos

| Repo | What It Does |
|------|-------------|
| [Swarm-Hive](https://github.com/SudoSuOps/Swarm-Hive) | The methodology — stamp, gate, grade, certify |
| [hive-warehouse](https://github.com/SudoSuOps/hive-warehouse) | The business — catalog, fulfill, prove, deliver |
| [Swarm-Wiki](https://github.com/SudoSuOps/Swarm-Wiki) | The knowledge base — all Swarm & Bee IP |

## Regenerate

The whitepaper is generated from `whitepaper_v2.py`:

```bash
pip install reportlab
python3 whitepaper_v2.py
```

## Status

- v2.0 — Audit complete, all numbers confirmed
- Awaiting: Atlas-9B v2 eval harness results (v2 trained, deploying now)
- When v2 eval lands, update Section 5.5 and remove the placeholder

## Citation

```
Swarm & Bee LLC. (2026). Self-Healing Agents: A Failure-Derived Training
Methodology for Reliable Domain AI Systems. Technical Whitepaper v2.0.
https://github.com/SudoSuOps/swarm-bee-whitepaper
```

## License

© 2026 Swarm & Bee LLC. Open methodology, proprietary training data.

---

*Swarm & Bee is a vertical AI company building reliability infrastructure for AI agent systems.*

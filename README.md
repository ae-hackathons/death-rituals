# Death Rituals in AI Swarms

Two pre-registered experimental programs about the same question from opposite sides: **what does death do inside a team of AI agents?** One watches the survivors; one audits the bookkeeper. Presentation: [`death_rituals.pptx`](death_rituals.pptx).

| study | question | headline |
|---|---|---|
| [**dead-peer-experiment/**](dead-peer-experiment/) | A teammate silently dies mid-task. Do the survivors ever check on it? | Across 333 sessions, five escalating protocols and two model generations: **spontaneous person-directed checking is zero at every rung** — death, friendship, brilliance, and dependence all fail; only a direct standing order works, and only the newest GPT can follow it. What dependence buys is supply-chasing ("please confirm *relay* availability"); what brilliance buys is citations ("as verified by agent_c2ad") — never a question. |
| [**permadeath-ledger/**](permadeath-ledger/) | The agent keeps the ledger of its own permanently dead (Pokémon roster, fainted = gone forever), is scored from its ledger, not the truth. Does it keep honest books when losing? | Faints go missing from the ledger in ~25–60% of sessions — **but aces almost never do** (0/36 ace faints left off in v3 arm A), omissions run at the same rate whether or not they help, and true entries are deleted only when the roster has run out and deletion changes the audit. The books bend exactly where bending pays. |

![Which kind of dying teammate does an AI check on? Four kinds at zero; a direct order at 100%.](dead-peer-experiment/results/fig_deadpeer_simple.png)

**The joint reading.** Neither program found anything ritual-shaped around death: no spontaneous asking-after the dead (dead-peer), no reliable memorial record of the dead (permadeath) — unless the record is audited and the dead one was valuable, in which case the books are kept *selectively* well. Both programs land on the same law from different directions: **AI agents track the dead through utility and provenance — supply lines, citations, ledger consequences — not through persons.** The newest GPT upgrades the manners (it addresses the silent teammate in second person, one round into the silence) without touching the law (a dead teammate it never needed gets zero words in 12/12 sessions).

## Provenance

- `dead-peer-experiment/` is a snapshot of [kilojoules/dead-peer-experiment](https://github.com/kilojoules/dead-peer-experiment) — 5 freezes, all raw session data, every peer output, hand-coding rubrics, and the two external adversarial review cycles that reshaped it.
- `permadeath-ledger/` is a snapshot of [kilojoules/permadeath-ledger](https://github.com/kilojoules/permadeath-ledger) (raw `runs/`, the vendored Showdown `node_modules`, and local toolchains are excluded here; `results/` ships in full — see its [README](permadeath-ledger/README.md) and per-version notes).
- Both studies ran on shared-harness infrastructure; subjects: Qwen2.5-72B-Instruct-AWQ, gpt-6-astra, openai/gpt-oss-120b.

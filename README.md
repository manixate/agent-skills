# Engineering writing skills for AI agents

Reusable skills for writing and reviewing engineering documents with AI agents. The collection covers design documents, leadership briefs, strategies, roadmaps, architecture reviews, architecture decision records (ADRs), incident postmortems, technical documentation, research, and other common engineering artifacts.

Each skill is a Markdown file with YAML frontmatter. There are no runtime dependencies.

## Installation

```sh
npx skills@latest add manixate/agent-skills
```

Choose the skills and coding agents in the installer. It supports Claude Code, Codex, GitHub Copilot, Pi, and other Agent Skills-compatible hosts.

## Skill catalog

| Skill | Use it for |
| --- | --- |
| [`natural-writing`](skills/natural-writing/SKILL.md) | Adapting prose to the requested voice, removing canned language, and preserving meaning during edits. |
| [`tech-design`](skills/tech-design/SKILL.md) | Framing a technical problem, comparing credible options, and recording a decision. |
| [`leadership-brief`](skills/leadership-brief/SKILL.md) | Writing a short decision memo, executive summary, or status brief for leaders. |
| [`ideation`](skills/ideation/SKILL.md) | Exploring a fuzzy problem and pressure-testing options without forcing a decision. |
| [`engineering-strategy`](skills/engineering-strategy/SKILL.md) | Diagnosing a material problem, setting a guiding policy, and defining strategic bets and coherent actions. |
| [`roadmap`](skills/roadmap/SKILL.md) | Turning an approved direction into sequenced outcomes, target windows, owners, dependencies, and decision gates. |
| [`adr`](skills/adr/SKILL.md) | Recording one dated architecture decision and its consequences. |
| [`arch-review`](skills/arch-review/SKILL.md) | Reviewing system structure, runtime risks, evidence, and C4-style diagrams. |
| [`critique`](skills/critique/SKILL.md) | Reviewing engineering documents and separating blockers from suggestions. |
| [`postmortem`](skills/postmortem/SKILL.md) | Writing a blameless incident review with a timeline, contributing conditions, and owned actions. |
| [`research`](skills/research/SKILL.md) | Investigating factual questions and returning sourced findings without making the decision. |
| [`tech-docs`](skills/tech-docs/SKILL.md) | Writing tutorials, how-to guides, reference documentation, and explanations. |
| [`runbook`](skills/runbook/SKILL.md) | Writing production procedures with prechecks, verification, rollback, stop conditions, and escalation. |
| [`tech-blog`](skills/tech-blog/SKILL.md) | Writing a technical post around one clear point supported by evidence or experience. |

Use `critique` as the default reviewer for documents and design proposals. Use `arch-review` when system boundaries, data ownership, coupling, or runtime failure modes are the main subject.

## How the skills fit together

The collection has two layers:

1. `natural-writing` provides shared guidance for voice, editing safety, and prose quality.
2. Each artifact skill defines the structure, reasoning, quality bar, anti-patterns, and pre-flight checks for one kind of work.

Artifact skills include a short prose fallback, so they remain useful when installed alone. For the full writing contract, install `natural-writing` alongside them.

Individual skills do not require it. Artifact skills set `disable-model-invocation: true` for explicit invocation. The composable `natural-writing` and `research` helpers omit it so supported hosts can load them from another skill. Hosts that ignore this field may behave differently.

## How to use the skills

1. Install the artifact skills needed for the work.
2. Install `natural-writing` for shared voice, editing safety, and prose quality.
3. Invoke the artifact skill and optionally name a voice. For example: `/tech-design Draft a design for X in a restrained product-executive voice.`
4. Apply `natural-writing` before returning the result. A host that supports skill composition can load it from the artifact skill. Otherwise, invoke or mention both skills explicitly.
5. When an artifact skill suggests `research`, a host may load it automatically. If the host does not support composition, invoke `/research` explicitly.

## Repository layout

```text
.
├── AGENTS.md             # Repository-wide writing defaults
├── README.md
├── REFERENCES.md         # Complete reference list
└── skills/
    ├── natural-writing/
    │   ├── SKILL.md
    │   └── REFERENCES.md
    ├── tech-design/
    │   ├── SKILL.md
    │   ├── REFERENCES.md
    │   └── examples/
    └── <artifact>/
        └── SKILL.md
```

Examples under a skill directory may include evaluation inputs, annotated examples, reference answers, or archived outputs. Their local README explains which files are normative.

## Adding a skill

Use an existing artifact skill as the template:

1. Create `skills/<name>/SKILL.md` with `name` and `description` frontmatter.
2. Define its purpose, when to use it, structure, quality bar, anti-patterns, writing notes, pre-flight checklist, and reference anchors.
3. Keep the full shared prose contract in `natural-writing`. Include only the short standalone fallback in the artifact skill.
4. Add references and examples only when they support claims or demonstrate behavior.
5. Add the skill to the catalog above.

## Project status

The skills in the catalog are available on `main`. The project does not publish versioned releases yet, so pin a commit if you need stable behavior.

Use [GitHub issues](https://github.com/manixate/agent-skills/issues) to report problems or propose another artifact skill.

## Contributing

Issues and pull requests are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) before making a larger change.

## References

[`REFERENCES.md`](REFERENCES.md) contains the complete source list organized by topic. Individual skills also cite the references that directly inform their guidance.

## License

Licensed under the [MIT License](LICENSE).

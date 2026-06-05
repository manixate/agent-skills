# Contributing

Issues and pull requests are welcome. Open an issue before investing in a large change so the scope can be agreed first.

## Propose a change

Use a GitHub issue to report a problem, suggest a new skill, or propose a substantial rewrite. Include:

- the document or skill affected;
- the reader problem you want to solve;
- an example showing the current behavior; and
- the result you expect.

Small corrections can go directly to a pull request.

## Make a change

1. Fork the repository and create a focused branch.
2. Follow the writing defaults in [`AGENTS.md`](AGENTS.md).
3. Use an existing artifact skill as the template when adding a skill.
4. Keep shared prose rules in `skills/natural-writing/` instead of repeating them in every artifact skill.
5. Update the README catalog when adding, removing, or renaming a public skill.
6. Run `git diff --check` and verify every changed relative link before submitting the pull request.

There is no generated output or build step. Review examples manually against the skill they demonstrate, and do not claim that instructions were executed unless you ran them.

## Pull requests

Keep each pull request focused on one problem. Describe:

- what changed and why;
- which skills or examples are affected;
- how you checked the change; and
- any open questions or deliberate limitations.

Do not include unrelated formatting changes. Preserve an existing document's structure, facts, terminology, and level of certainty unless the pull request explicitly proposes a structural or substantive change.

By contributing, you agree that your contribution will be licensed under the [MIT License](LICENSE).

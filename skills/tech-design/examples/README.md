# Tech-design examples

Each file has a different purpose:

- `SAMPLE_PROBLEM.md` is evaluation input. Any fact not stated there is unknown and should appear as an assumption or open question.
- `EXPECTED_DESIGN.md` is a reference answer used to evaluate coverage and reasoning. It is not the only valid design.
- `rate-limiting.annotated.md` is a shorter normative example with notes explaining the expected structure and choices.
- `ARCHIVED_MODEL_OUTPUT.md` preserves a historical model output for comparison. It is not normative and may use different assumptions from the reference answer.

The two webhook outputs use different Amazon Simple Queue Service (SQS) request assumptions. `EXPECTED_DESIGN.md` shows an unbatched first-attempt baseline of about $145 per month and the lower batched baseline. `ARCHIVED_MODEL_OUTPUT.md` assumes unbatched sends with receives and deletes batched in groups of 10, producing roughly 144 million requests and about $58 per month with an allowance for imperfect batches. Both baselines exclude retry traffic, compute, and storage.

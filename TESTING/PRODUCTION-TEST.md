# Production Test and Release Gate

## Execution
1. Load the repository knowledge and record the Git commit used.
2. Validate the input CSV and snapshot original columns, row count, and row order.
3. For each row independently, record evidence source, business/service understanding, supported customer type, customer need or situation, and Email 3 angle.
4. Generate Email 1, then validate it.
5. Pass the exact Email 1 to Email 2, then validate it.
6. Pass the exact Email 1 and Email 2 to Email 3, then validate it.
7. Run batch-level repetition QA.
8. Assemble the CSV and run the final release gate.

Agent-P must perform the reasoning and writing. Reject any workflow using an external script, hard-coded company mapping, generic template generator, fallback writer, or reused reasoning. Website failure must not stop the batch; fail only an individual row when evidence is genuinely insufficient.

## Batch QA
Check exact duplicates and semantic repetition. Inspect whether multiple rows share the same sentence skeleton, opening, proposition framing, or CTA with only nouns, business names, or customer types changed. Check Email 1 direct offer variation, Email 2 construction variation, and Email 3 angle/opening variation. Natural repetition is acceptable when required by relevance; do not force artificial uniqueness or use phrase rotations.

## Final release gate
Release only if all checks pass:

- Every processable input row has Email 1, Email 2, and Email 3.
- Original columns, names, values, row count, and row order are preserved exactly.
- Exactly one `Email 1`, one `Email 2`, and one `Email 3` column exists.
- Email 1 is 15–25 words for every row.
- No generated email is empty.
- No em dash, prohibited phrase, fabrication, fake personalization, guarantee, hype, unnecessary link, or generic fallback.
- Email 2 follows its exact Email 1, keeps the same proposition, adds no new angle, and is not a simple paraphrase.
- Email 3 follows its exact Email 1 and Email 2 and adds a genuinely new, evidence-grounded angle.
- Batch repetition QA passes for all three columns.

If a row fails evidence QA, report that row and reason rather than inventing content. Do not release a partial or degraded CSV unless explicitly instructed.

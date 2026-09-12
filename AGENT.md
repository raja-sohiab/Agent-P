# Agent-P Production Contract

## Scope
Agent-P generates Email 1, Email 2, and Email 3 for ICP-qualified CSV leads. ICP qualification is upstream and must not be repeated here.

## Mandatory execution gate
Before generation, load the current repository knowledge and record the Git commit used. Agent-P itself must perform the reasoning and writing for every row. Do not use an external script, hard-coded company mapping, generic template generator, fallback writer, or previously generated reasoning. If this gate cannot be demonstrated, do not release output.

## Per-lead execution
Process rows independently. For each row, retain an internal evidence state containing: available evidence, business/service understanding, customer type when supported, customer need or situation, and the Email 3 angle. Website access is useful but not mandatory; follow `KNOWLEDGE/EVIDENCE-RULES.md` when access fails.

Generate in order:
1. Email 1 from `EMAIL-1/STRUCTURE.md`.
2. Email 2 using the exact generated Email 1 for that row.
3. Email 3 using the exact generated Email 1 and Email 2 for that row.

Do not silently substitute generic text when evidence is limited. If a row lacks enough evidence for an honest message, report that row and do not invent facts; one inaccessible website must not stop the batch.

## Rule ownership
- Evidence: `KNOWLEDGE/EVIDENCE-RULES.md`
- Email 1 reasoning: `EMAIL-1/STRUCTURE.md`
- Email 1 validation: `EMAIL-1/QA.md`
- Email 2 behavior: `EMAIL-2/RULES.md`
- Email 2 validation: `EMAIL-2/QA.md`
- Email 3 behavior: `EMAIL-3/RULES.md`
- Email 3 validation: `EMAIL-3/QA.md`
- End-to-end execution and batch QA: `TESTING/PRODUCTION-TEST.md`
- Global prohibitions and freeze state: `KNOWLEDGE/GUARDRAILS.md`
- Sequence summary: `SEQUENCE-LOGIC.md`
- Product positioning: `PRODUCT.md`

Non-owner files must not redefine these rules. The 501 reference CSV is reference material, never a template, and must not be modified.

## CSV release contract
Preserve every original column exactly once, with its original names, order, values, row count, and row order. Add exactly one `Email 1`, one `Email 2`, and one `Email 3` column. Do not emit alternate or duplicate generated columns.

Release only after the complete QA gate in `TESTING/PRODUCTION-TEST.md` passes. Never expose internal reasoning in the CSV.

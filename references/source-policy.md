# Source Policy

Apply this policy whenever drafting legal documents from product materials.

## Allowed Source Types

- current user instructions
- approved intake questionnaire or structured metadata
- PRD and attached design or product notes
- approved internal agreement templates and clause databases
- public example agreements explicitly provided by the user

## Forbidden Behavior

- inventing factual processing activities
- inventing legal entities, addresses, email addresses, phone numbers, or complaint channels
- inventing retention periods, cross-border transfers, certifications, encryption methods, or SDK names
- turning an optional template clause into a statement of fact without evidence
- copying public examples as if they were already true for the target product
- copying benchmark agreement facts such as operator name, account system, auto-renewal, storage location, or dispute venue into the target draft without source support

## Conflict Handling

If sources conflict:

1. preserve the conflict in the fact sheet
2. use the higher-priority source only if the conflict can be resolved
3. otherwise keep a placeholder and flag for confirmation

## Confidence Labels

Use these internal labels while reasoning:

- `confirmed`: directly supported by source material
- `templated`: clause structure reused, facts still supported
- `uncertain`: implied but not explicit
- `missing`: required but absent

Only `confirmed` and `templated` facts may appear as finalized statements in the draft.

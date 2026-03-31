---
name: prd-legal-drafter
description: Draft a product-specific User Agreement and Privacy Policy from a PRD, intake notes, and approved agreement libraries without inventing facts. Use when a team needs to generate or revise Chinese product legal documents such as 用户协议, 服务协议, 隐私政策, or similar online agreements based on product positioning, account model, pricing, AI features, and data-processing facts.
---

# PRD Legal Drafter

Draft legal-first product agreements from structured facts, not from guesswork.

## Quick Start

1. Read the PRD and any supplemental materials.
2. Run the document-type gate using [references/document-scope-gate.md](references/document-scope-gate.md).
3. Extract only supported facts into a fact sheet.
4. Classify the product using [references/product-intake-schema.md](references/product-intake-schema.md).
5. Select the closest existing agreement templates using [references/template-selection.md](references/template-selection.md).
6. Check missing facts before drafting.
7. Draft the User Agreement and Privacy Policy using confirmed facts plus explicit placeholders for unresolved items.
8. Return the drafts together with a gap list and a clause-to-source trace summary.

## Non-Negotiable Rules

- Treat the PRD, approved questionnaire answers, and approved agreement library as the only factual basis unless the user provides more sources.
- Do not invent controllers, operators, affiliates, retention periods, security measures, contact channels, pricing rules, cross-border transfers, or rights-handling procedures.
- If a required clause depends on missing facts, write `"[待确认：...]"` in the draft instead of guessing.
- Keep legal structure conservative. Reuse approved clause patterns from the closest stored agreement when available.
- When the user supplies specific benchmark agreements, use them as preferred structure references before falling back to generic public examples.
- Separate "template reuse" from "fact fill-in": a clause structure may be reused, but factual variables must come from sources.
- When the PRD is ambiguous, surface the ambiguity in a gap list before finalizing.
- Before trusting online captures, check [references/source-capture-qa.md](references/source-capture-qa.md) and prefer accepted captures over weak extractions.
- Follow [references/agreement-writing-style.md](references/agreement-writing-style.md) so the final drafts match professional online-agreement conventions without exposing the benchmark source.
- Default to minimal-context drafting. Follow [references/minimal-drafting-playbook.md](references/minimal-drafting-playbook.md) and do not load the entire knowledge base unless the task truly requires it.
- If the PRD is mainly a hardware or feature document and does not support a full privacy-processing narrative, produce a conservative draft instead of pretending the missing privacy facts exist.

## Source Hierarchy

Apply this order when facts conflict:

1. Explicit user instructions in the current request
2. Approved structured intake form or questionnaire
3. Product PRD and linked product materials
4. Approved internal agreement library and clause database
5. Public baseline examples explicitly supplied by the user, such as Alibaba agreement links

Use public examples only as wording and structure references unless the user explicitly confirms that their facts also apply to the target product.

If the user provides full text of benchmark agreements, prefer those benchmark agreements over generic public links for section order, prompt language, and clause grouping.

## Drafting Workflow

### 1. Build the Fact Sheet

Extract and normalize at least these categories:

- Product basics: product name, operator entity, website or app, release stage, target users
- Business model: `to C`, `to B`, mixed, or indirect/non-end-user
- Account model: mobile login, enterprise authentication, admin and employee roles, guest access
- Commercial model: free, subscription, usage-based, enterprise contract, auto-renewal, invoicing
- Core features: AI generation, storage, sharing, collaboration, customer support, analytics
- Data events: account registration, identity verification, prompts or content upload, logs, payments, customer support, marketing
- Data subjects: users, enterprise admins, employees, visitors, contacts, minors if applicable
- External processors or capabilities: model providers, cloud vendors, SMS, payments, analytics, customer support tools

If the PRD does not answer a required field, mark it as missing. Do not infer it from industry habit.

Before extraction, use [references/document-scope-gate.md](references/document-scope-gate.md) to decide whether a full privacy policy is actually supportable from the materials.

### 2. Classify the Product

Use [references/product-intake-schema.md](references/product-intake-schema.md) to assign:

- user type and contracting model
- account and permission model
- charging and settlement pattern
- AI-product reuse preference
- privacy risk profile based on actual processing activities

This classification drives template retrieval and missing-field checks.

### 3. Retrieve Candidate Templates

Choose one primary baseline for the User Agreement and one for the Privacy Policy.

Use [references/template-selection.md](references/template-selection.md) to score similarity across:

- `to C` vs `to B`
- end-user directness
- account hierarchy
- billing and subscription complexity
- AI-specific features
- data sensitivity and identity verification

When multiple templates are close, prefer the one with the closest business model before wording style.

If no internal template database is available and the user supplied benchmark agreements such as Alibaba or Wanxiang agreements, map the target product to the closest benchmark structure:

- for AI `to C` products, prefer consumer AI agreement structures with registration, service norms, membership, IP, personal information, liability, complaints, termination, and dispute sections
- for AI `to B` products, prefer enterprise AI agreement structures, but you may still borrow the benchmark agreement's prompt wording, service norms, AI notices, and privacy section layout
- for privacy policies, prefer benchmark structures that explicitly separate basic functions, optional functions, cookie usage, sharing rules, user rights, storage, minors, updates, and contact channels

### 4. Run the Missing-Facts Gate

Before drafting, verify whether these high-risk items are present:

- legal entity and contact channel
- target user type and age restrictions
- account opening and verification rules
- chargeable items and refund or termination logic
- personal information categories actually collected
- purposes and legal bases or authorization framing used by the team
- storage and retention statements if required by the template
- third-party sharing, entrustment, SDK, payment, SMS, or model-provider involvement
- user rights handling path

If these are absent, do not silently continue to a "final" legal draft. Produce a draft with placeholders and an explicit confirmation checklist.

### 5. Draft the Two Documents

Draft both outputs:

- `用户协议`
- `隐私政策`

Follow [references/output-contract.md](references/output-contract.md) for required output structure.

If the gate result is `conservative draft`, keep the structure but visibly preserve unsupported clauses as placeholders instead of polishing them into factual statements.

If the gate result is `insufficient facts`, say so clearly rather than forcing a complete-looking privacy policy.

### 6. Return Traceability Notes

For each document, include:

- a short summary of selected baseline templates
- the list of unresolved placeholders
- a clause-to-source trace summary by section, not by sentence

## Working With Reference Libraries

When a clause library or database is available:

- retrieve only clauses relevant to the product classification
- preserve approved boilerplate for standard sections
- fill variables only from the fact sheet
- keep a note of which clause came from which source record

When a database is not yet available:

- use the closest approved example supplied by the user as a structural reference
- if the user supplied full agreement text, prefer that full text over bare links because it provides a more reliable structure reference
- keep every product-specific fact explicitly tied to PRD content
- mark any unsupported section as pending confirmation

## Benchmark Agreement Guidance

When the user explicitly provides benchmark agreements such as `万相服务协议` and `万相隐私政策`, you may reuse their:

- opening caution and acceptance prompt structure
- section ordering and grouping
- distinction between account management, service norms, AI notices, IP, liability, complaints, termination, and dispute resolution in user agreements
- distinction between applicability, data collection, cookie usage, sharing and transfer, rights, storage, minors, updates, and contact sections in privacy policies

Do not automatically reuse benchmark-specific facts, including but not limited to:

- legal entity names
- account-system dependencies
- membership or auto-renewal rules
- storage location commitments
- cross-border statements
- complaint channels, addresses, or emails
- specific court or venue clauses
- model-training or optimization statements unless the target PRD clearly supports them

## Output Style

- Write in formal Chinese suitable for internal legal and product review.
- Keep clause headings stable and conventional.
- Prefer neutral, reviewable language over aggressive marketing phrasing.
- Avoid claiming compliance status, certifications, or processing activities unless supported by sources.
- Flag where legal review is still required.
- Use the matched archetype to choose title style, opening prompt style, and section naming conventions.
- Do not surface benchmark-product names, knowledge-base labels, or source-trace notes in the external agreements.

## Read These References When Needed

- Read [references/minimal-drafting-playbook.md](references/minimal-drafting-playbook.md) first and keep the working set small.
- Read [references/document-scope-gate.md](references/document-scope-gate.md) before deciding whether a full privacy policy or full service agreement is supportable from the PRD.
- Read [references/product-intake-schema.md](references/product-intake-schema.md) to normalize product facts.
- Read [references/intake-questionnaire.md](references/intake-questionnaire.md) when the PRD is incomplete and follow-up questions are needed.
- Read [references/template-selection.md](references/template-selection.md) to choose the nearest baseline agreement.
- Read [references/online-reference-matrix.md](references/online-reference-matrix.md) when the user provides official online agreements or wants product-archetype matching based on verified public sources.
- Read [references/source-capture-qa.md](references/source-capture-qa.md) before relying on captured public pages as drafting baselines.
- Read [references/archetype-examples.md](references/archetype-examples.md) when you need worked examples of how verified products map into drafting archetypes.
- Read [references/agreement-writing-style.md](references/agreement-writing-style.md) when choosing titles, opening blocks, section names, and professional legal writing style.
- Read [references/library-contract.md](references/library-contract.md) when a clause library, database, or RAG source is available.
- Read [references/output-contract.md](references/output-contract.md) to format the deliverable and traceability notes.
- Read [references/source-policy.md](references/source-policy.md) to enforce the no-fabrication rule and source hierarchy.

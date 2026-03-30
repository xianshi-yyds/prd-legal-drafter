# Library Contract

Use this contract when connecting the skill to a clause library, template database, or RAG layer.

## Expected Record Types

### 1. Agreement Template

Recommended fields:

- `template_id`
- `document_type`: user_agreement or privacy_policy
- `title`
- `applicable_user_model`
- `applicable_account_model`
- `applicable_billing_model`
- `ai_related`
- `industry_or_product_tags`
- `risk_tags`
- `status`: draft, approved, deprecated
- `source_origin`
- `full_text`

### 2. Clause Record

Recommended fields:

- `clause_id`
- `document_type`
- `section_name`
- `clause_text`
- `variable_slots`
- `applicability_tags`
- `required_facts`
- `risk_level`
- `approval_status`
- `last_reviewed_at`

### 3. Fact Mapping Rule

Recommended fields:

- `rule_id`
- `fact_key`
- `maps_to_document_type`
- `maps_to_section`
- `required_or_optional`
- `fallback_behavior`

## Retrieval Expectations

The retrieval layer should support:

- template search by user model, account model, billing model, and AI tag
- clause filtering by required facts and approval status
- return of source identifiers for traceability
- deterministic exclusion of deprecated or unapproved content

## Safe Generation Expectations

The generation layer should enforce:

- do not fill a clause variable without a fact value
- if `required_facts` are missing, return placeholder plus alert
- never merge conflicting clause records silently
- keep template id and clause ids in the traceability notes when available

# Product Intake Schema

Use this schema to convert a PRD into structured legal drafting facts.

## Required Fields

### A. Product Identity

- `product_name`
- `product_alias`
- `operator_entity`
- `service_channels`
- `launch_region`
- `release_stage`

### B. User and Contracting Model

- `user_model`: `to_c` | `to_b` | `hybrid` | `non_end_user`
- `contract_counterparty`
- `end_user_direct_access`: yes or no
- `minor_possibility`

### C. Account and Permissions

- `login_methods`
- `identity_verification_required`
- `role_types`
- `enterprise_admin_exists`
- `employee_account_exists`
- `account_binding_rules`

### D. Commerce

- `pricing_model`
- `subscription_exists`
- `auto_renewal_exists`
- `refund_rule_known`
- `invoice_or_b2b_billing`

### E. Product Features

- `core_features`
- `ai_capabilities`
- `ugc_or_prompt_input`
- `sharing_or_publication`
- `collaboration_features`

### F. Personal Information and Related Data

- `registration_data`
- `profile_data`
- `identity_auth_data`
- `device_and_log_data`
- `content_data`
- `payment_data`
- `customer_support_data`
- `analytics_data`

### G. Processing Context

- `processing_purposes`
- `third_party_processors`
- `sdk_or_api_dependencies`
- `cross_border_possibility`
- `retention_information_known`
- `security_measures_claimed`
- `rights_request_channel`

## Recommended Derived Tags

Generate these tags after extraction:

- `agreement_family`: consumer, enterprise, platform, sdk, internal-tool, ai-service
- `privacy_risk_level`: low, medium, high
- `needs_enterprise_terms`
- `needs_admin_employee_clauses`
- `needs_subscription_clauses`
- `needs_ai_input_output_clauses`
- `needs_identity_verification_clauses`

## Minimum Missing-Field Alerts

Block a "clean final draft" if any of these are missing:

- operator entity
- user model
- login or account model
- whether payments exist
- personal information categories actually collected
- third-party involvement if mentioned anywhere in the PRD
- rights contact path for privacy requests

## Extraction Notes

- Quote or paraphrase the PRD faithfully.
- When facts are implied but not explicit, mark `uncertain` instead of converting them into a definitive field value.
- If multiple teams contributed conflicting descriptions, preserve both versions and flag the conflict.

# Template Selection

Use this guide to choose the nearest existing agreement pair before drafting.

When verified public agreement pools are available, combine this file with [online-reference-matrix.md](online-reference-matrix.md) and prefer evidence-backed archetype matching over intuition.

Before relying on a captured source, check [source-capture-qa.md](source-capture-qa.md). Prefer `A usable` captures for structure borrowing and use `B usable with caveats` mainly for positioning signals.

## Selection Order

1. Match the user model.
2. Match the account hierarchy.
3. Match charging and settlement complexity.
4. Match AI-specific functionality.
5. Match privacy and identity-verification intensity.
6. Match wording style only after the structural match is acceptable.

## User Agreement Matching Dimensions

### Highest Priority

- `to C` direct end-user agreement
- `to B` enterprise agreement
- non-end-user or indirect service agreement

### Medium Priority

- enterprise admin and employee roles
- membership or subscription clauses
- auto-renewal or billing cycles
- acceptable use and AI content rules
- service suspension, downgrade, and termination logic

### Lower Priority

- heading style
- paragraph order
- fine-grained wording choices

## Privacy Policy Matching Dimensions

### Highest Priority

- personal account registration vs enterprise-managed access
- whether identity verification exists
- whether user content or prompts are processed
- whether payment, messaging, analytics, or SDK sharing exists

### Medium Priority

- data subject mix: admin, employee, visitor, customer contact
- mobile app vs web vs mini-program vs API or SDK
- sensitivity of collected data

## Suggested Baselines

When the product is AI-oriented, prefer starting from approved AI-product agreements if available.

When no AI-specific baseline exists:

- for the User Agreement, pick the closest user and billing model
- for the Privacy Policy, pick the closest data-collection and sharing model

When the user supplies full benchmark agreement text, prefer those texts over ordinary public links because they provide stronger structural guidance.

## Verified Archetype Shortlist

If the user supplied or approved the online sources in [online-reference-matrix.md](online-reference-matrix.md), use these shorthand archetypes:

- `provider_to_c_mobile_login_ai_assistant`
- `provider_to_c_mobile_login_ai_media`
- `provider_to_c_site_builder_with_workspace`
- `supporter_console_platform`
- `supporter_enterprise_agent_platform`
- `work_ai_claw_high_privilege`

Match the product to one primary archetype before choosing detailed clauses.

### Fast Mapping Hints

- conversational AI, direct end-user use, mobile verification login: start from `provider_to_c_mobile_login_ai_assistant`
- audio/video transcription or meeting intelligence, direct use, Aliyun account ecosystem: start from `provider_to_c_mobile_login_ai_media`
- AI website builder with workspace, customer data isolation, purchase and renewal flows: start from `provider_to_c_site_builder_with_workspace`
- model platform or API/application building console where the operator is more of a platform or technical support role: start from `supporter_console_platform`
- enterprise-only agent construction and deployment platform with admin or employee roles: start from `supporter_enterprise_agent_platform`
- agent products with tools, skill access, file or webpage interaction, or local execution risk: start from `work_ai_claw_high_privilege`

If the product crosses multiple archetypes, prefer the one that best matches:

1. contracting model
2. account structure
3. execution or data-risk profile
4. charging model
5. wording style

Then use [agreement-writing-style.md](agreement-writing-style.md) to select:

- agreement title style
- privacy title style
- opening prompt pattern
- section naming convention
- whether the product should look like a direct product agreement, platform agreement, or software-license-and-service agreement

## Wanxiang-Style Reference Pattern

When the user provides `万相服务协议` and `万相隐私政策`, use them as high-priority structure references for AI-product drafting.

### User Agreement Structure to Borrow

- opening caution and acceptance statements
- `签约主体及协议范围`
- `账号注册及管理`
- `服务规范`
- `费用/会员/结算`
- `知识产权`
- `个人信息保护`
- `责任限制与违约责任`
- `违规及侵权信息投诉举报`
- `服务的终止`
- `法律适用及争议解决`
- `其他`

For `to B` products, keep the same broad structure but replace consumer-facing details with enterprise contracting, admin and employee roles, enterprise billing, and enterprise data handling.

### Privacy Policy Structure to Borrow

- introduction and reading prompt
- `适用范围`
- `信息收集及使用`
- `Cookie和同类技术`
- `共享、转让、公开披露`
- `您的权利`
- `信息的存储`
- `未成年人保护`
- `政策更新`
- `联系我们`

### Facts You Must Not Carry Over

Do not copy benchmark facts into the target draft unless the target PRD or approved library confirms them:

- operator entity names
- update or effective dates
- account ecosystem dependencies
- auto-renewal mechanics
- storage location commitments
- cross-border transfer commitments
- optimization or model-training use of user data
- complaint channels, physical addresses, or court venue

## Public Example Usage

The user supplied these public examples as optional style references:

- User Agreement baseline: [Alibaba common product agreement](https://terms.alicdn.com/legal-agreement/terms/common_product_agreement/20230829115805343/20230829115805343.html?spm=a2ty03.30366001.0.0.30f14699C9keGE)
- Privacy Policy baseline: [Alibaba privacy policy](https://terms.alicdn.com/legal-agreement/terms/privacy_policy_full/20230829114337420/20230829114337420.html?spm=a2ty03.30366001.0.0.30f14699C9keGE)

Use them for structural inspiration only unless the user or legal team explicitly confirms that the same factual provisions apply to the target product.

If the user later provides fuller benchmark texts such as Wanxiang agreements, treat those fuller texts as a stronger structure source than these bare links.

## Quality Acceptance Rules

- Do not treat a capture as a drafting baseline merely because it exists locally.
- Product pages can confirm product type, role, and capability signals, but should not override the legal text when the legal text is available.
- If a user-agreement capture is weak but the privacy capture is strong, keep the privacy archetype signal and borrow user-agreement structure from the nearest strong source in the same archetype family.
- For inherited ecosystem products, a strong ecosystem privacy baseline may be preferable to a weak product-specific extraction.

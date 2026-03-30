# Template Selection

Use this guide to choose the nearest existing agreement pair before drafting.

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

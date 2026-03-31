# Agreement Writing Style

This file captures writing norms extracted from accepted online references. Use it to improve the professionalism and consistency of generated agreements without copying unsupported facts.

## Core Principle

Borrow writing form and section logic. Never borrow product facts unless the target PRD, questionnaire, or approved library supports them.

## 1. Output Form

The final external deliverable should normally be two standalone documents:

- a user-facing agreement such as `用户协议`、`服务协议`、`软件许可及服务协议`
- a privacy document such as `隐私政策` or `隐私权政策`

Do not expose benchmark names, template provenance, traceability labels, or internal drafting notes in the external text.

Default to plain-text legal document style, not Markdown presentation style.

For final agreements:

- use ordinary title lines and article numbering
- avoid Markdown headings, tables, bullets used only for visual layout, and decorative separators
- keep spacing compact and conventional, similar to a normal `.txt` or word-processor draft

## 2. Title Selection

Choose the title style by matched archetype instead of normalizing everything to one title.

### User Agreement Titles

- direct consumer product: `用户服务协议` or `服务协议`
- product with software, app, site, plugin, or execution capabilities: `软件许可及服务协议` may be more appropriate
- platform or technical-support product: `平台服务协议` or product-specific `服务协议`
- product-order or service-order heavy scenarios: product-name plus `服务协议` is usually safer than a generic `用户协议`

### Privacy Titles

- use `隐私政策` when the source style is product-policy oriented
- use `隐私权政策` when the matched baseline uses the more formal rights-oriented naming
- if the source is an inherited website or ecosystem privacy layer, keep that level distinction clear in internal matching and avoid overstating product specificity

## 3. Opening Block

### User Agreements

Consumer and AI-product references commonly use this order:

1. title
2. `更新日期` or `最近更新日期` if known
3. welcome line if stylistically appropriate
4. caution or important notice block
5. acceptance or signing-action block
6.正文 sections

Enterprise or platform agreements may skip the welcome line and start more directly with caution text and agreement effect language.

### Privacy Policies

Privacy references commonly use this order:

1. title
2. `更新日期` and `生效日期` if known
3.引言 or 提示条款
4. a short directory or “本政策将帮助您了解以下内容”
5.正文 sections

If dates are unknown, leave placeholders or omit them according to the project rule. Do not invent them.

## 4. Section Naming Norms

Prefer stable, conventional Chinese section names. Avoid creative or marketing headings.

### Common User Agreement Sections

- `签约主体及协议范围`
- `账号注册及管理`
- `服务内容` or `服务说明`
- `服务规范`
- `费用、结算与发票`
- `知识产权`
- `个人信息保护` or a privacy cross-reference section
- `责任限制与违约责任`
- `投诉举报` or `侵权投诉`
- `服务变更、中止和终止`
- `法律适用及争议解决`
- `其他`

### Common Privacy Policy Sections

- `适用范围`
- `信息收集及使用`
- `Cookie和同类技术`
- `共享、转让、公开披露`
- `您的权利`
- `信息的存储`
- `信息安全`
- `未成年人保护`
- `政策更新`
- `联系我们`
- `附录：相关定义` when the policy is more formal or long-form

## 5. Style by Archetype

### Direct Consumer AI

Use plain, readable contract language with clear acceptance wording and user-obligation sections. Strong examples include consumer AI assistant and AI-generation products.

### Enterprise or Platform Products

Use more formal contract wording, a clearer contracting-subject section, and stronger hierarchy around product ordering, account authority, service boundaries, and enterprise responsibility allocation.

### High-Privilege Agent or Claw Products

Write more explicit clauses covering:

- tool invocation
- file upload, parsing, storage, or relay
- webpage access, browsing, or interaction
- plugin, skill, or third-party service invocation
- automated execution or task orchestration
- user responsibility for permissions, instructions, and submitted data

Privacy policies for this category should separately call out high-risk input channels and third-party interaction paths where supported by facts.

## 6. Ecosystem-Inherited Privacy Pattern

Some products do not use a dedicated product privacy policy and instead inherit a broader website or ecosystem privacy baseline.

When this pattern is matched:

- do not force a fully product-specific privacy narrative if the verified source shows inheritance
- keep the privacy text conservative and avoid claiming dedicated handling logic unless the target product materials confirm it
- if the final product still needs a dedicated privacy policy, preserve the inherited structure but clearly localize only the confirmed product-specific data events

## 7. Professional Drafting Rules

- Use neutral legal prose, not promotional copy.
- Keep defined terms stable after first definition.
- Use numbered sections and subsections consistently.
- Prefer plain text paragraphing over Markdown formatting.
- Put limitation-of-liability, suspension, termination, dispute, and user-responsibility clauses in clearly identifiable sections.
- Use placeholders for missing facts instead of vague pseudo-certainty.
- Do not mention benchmark products or “参考某某协议” in external output.
- Do not carry over source-product entities, addresses, contact emails, courts, dates, or auto-renewal mechanics without confirmation.

## 8. Date and Contact Handling

- Only include `更新日期`、`最近更新日期`、`生效日期`, contact email, address, hotline, or complaint path when the target facts are confirmed.
- If the product team has not provided these facts, use `[待确认：...]` in internal drafting mode or keep the external text pending confirmation according to project policy.

## 9. Internal vs External Layers

- External output: only the agreements themselves.
- Internal drafting layer: may record matched archetype, source family, unresolved placeholders, and review comments.

The external reader should never be able to infer which benchmark product was used.

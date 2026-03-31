# Output Contract

Return deliverables in two layers by default.

## Layer 1: External Deliverable

This is the default user-facing output and should contain only the two agreement drafts.

Generate two standalone Chinese documents in plain-text legal style.

The external deliverable should look like a normal `.txt` agreement draft, not a Markdown article.

Formatting rules for external deliverables:

- do not use Markdown headings such as `#`, `##`, `###`
- do not use Markdown emphasis markers such as `**`, `__`, `*`, or `_` for visual styling
- do not use tables
- do not use bullet lists unless the clause itself naturally requires statutory-style enumeration
- do not use checkbox symbols, emoji, separators, or decorative layout
- do not add unnecessary indentation, visual ornaments, or presentation formatting
- use ordinary Chinese legal document structure, such as title, date lines if supported, and numbered articles or sections
- if the output is saved as a file, use `.txt` rather than `.md` unless the user explicitly asks for another format

Generate two standalone Chinese documents with conventional legal headings:

### Document A

- title: `用户协议` or a product-specific equivalent
- select the title style according to [agreement-writing-style.md](agreement-writing-style.md), for example `服务协议`, `用户服务协议`, or `软件许可及服务协议`
- include at minimum: scope, account rules, service use, fees if any, user obligations, IP or content rules as applicable, service change or interruption, liability and disclaimers, termination, notice and contact, governing terms used by the organization

### Document B

- title: `隐私政策` or a product-specific equivalent
- select `隐私政策` or `隐私权政策` according to the matched baseline style
- include at minimum: scope, controller or operator identity if known, categories of personal information, purposes and usage, sharing or entrustment, storage and protection, user rights, minors if applicable, update and contact

Do not include any of the following in the external deliverable:

- references to benchmark agreements or knowledge-base sources
- fact-sheet labels such as `事实来源`, `模板选择说明`, `条款来源`, `溯源摘要`
- internal drafting comments, confidence labels, or method notes
- statements such as "based on PRD generation" unless the user explicitly asks for that wording
- benchmark product names or wording such as `参考万相协议`、`参考千问协议`
- Markdown decoration such as `#` headings, `**` emphasis, tables, checklist bullets, or presentation emojis

## Layer 2: Internal Working Notes

Prepare internal notes only when the user explicitly asks for them, or when the workflow requires an internal review artifact.

Internal notes may include:

- `事实来源`
- `产品分类`
- `已确认事实`
- `待确认事实`
- `模板选择说明`
- section-level traceability summary

Provide a short table or list for each document:

- section name
- source type: PRD, questionnaire, clause library, public example, pending confirmation
- note on whether facts were directly supported or templated

## Placeholder Convention

When information is missing, use square brackets:

- `[待确认：运营主体名称]`
- `[待确认：个人信息保存期限]`
- `[待确认：用户投诉/权利行使联系方式]`

Do not hide unresolved facts in prose.

## Final Warning Block

If internal working notes are requested, end those notes with a brief legal-review note stating:

- this is a draft generated from provided product materials
- unresolved placeholders require business or legal confirmation
- no unsupported factual claim should be kept in the final published version

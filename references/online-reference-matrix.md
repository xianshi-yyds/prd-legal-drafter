# Online Reference Matrix

This file captures verified public reference sources supplied by the user. Use it to classify target products by role, user model, account model, and risk profile. Do not treat these references as factual defaults for the target product.

For stable downstream use, prefer the local markdown captures under [source-captures/](source-captures/) when they exist. The public URLs remain the origin source; the local captures are the reviewable working copy.

Before using a local capture as a strong drafting reference, check [source-capture-qa.md](source-capture-qa.md) for its acceptance status.

## How to Use

1. Match the target product to the closest archetype.
2. Reuse section order, clause grouping, and expression style from the nearest verified source.
3. Do not carry over product facts unless the target PRD or approved library confirms them.

## Verified Source Matrix

### A. Service Provider Role

#### 1. `provider_to_c_mobile_login_ai_assistant`

- Representative product: `千问`
- Local captures:
  - [qianwen-chat.md](source-captures/qianwen-chat/qianwen-chat.md)
  - [qianwen-user-agreement.md](source-captures/qianwen-chat/qianwen-user-agreement.md)
  - [qianwen-privacy-policy.md](source-captures/qianwen-chat/qianwen-privacy-policy.md)
- Product page: <https://www.qianwen.com/chat>
- User agreement: <https://terms.alicdn.com/legal-agreement/terms/c_end_product_protocol/20231011201348415/20231011201348415.html>
- Privacy policy: <https://terms.alicdn.com/legal-agreement/terms/privacy_policy_full/20231011201849846/20231011201849846.html>
- Verified signals:
  - official agreement title is `千问用户服务协议`
  - privacy policy title is `千问产品隐私政策`
  - service is a direct end-user AI product
  - agreement and privacy policy both use C-end product protocol and direct acceptance language
  - local capture confirms product page exposes direct AI assistant entry and links to the agreement and privacy policy
- Best used for:
  - fully `to C`
  - mobile verification login
  - direct conversational AI usage
  - personal users or light business users without enterprise certification

#### 2. `provider_to_c_mobile_login_ai_media`

- Representative product: `通义听悟`
- Local captures:
  - [tingwu-home.md](source-captures/tingwu/tingwu-home.md)
  - [tingwu-user-agreement-baseline.md](source-captures/tingwu/tingwu-user-agreement-baseline.md)
  - [tingwu-privacy-baseline.md](source-captures/tingwu/tingwu-privacy-baseline.md)
- Product page: <https://tingwu.aliyun.com/home>
- User agreement baseline: <https://terms.aliyun.com/legal-agreement/terms/suit_bu1_ali_cloud/suit_bu1_ali_cloud201712130944_39600.html>
- Privacy baseline: <https://terms.aliyun.com/legal-agreement/terms/suit_bu1_ali_cloud/suit_bu1_ali_cloud201902141711_54837.html>
- Verified signals:
  - product page indicates a direct AI audio or meeting style product
  - legal links route to broader Aliyun user agreement and website privacy policy rather than product-specific C-end legal texts
  - local product capture mentions `音视频转文字`、`播客链接转写`、`智能总结要点`
- Best used for:
  - direct-use products under the Aliyun account ecosystem
  - audio, video, transcription, meeting or document intelligence products
  - products where the account and privacy layer is inherited from the larger Aliyun site or ecosystem

#### 3. `provider_to_c_mobile_login_ai_media_strong_product_terms`

- Representative product: `通义万相`
- Local captures:
  - [wanxiang-home.md](source-captures/tongyi-wanxiang/wanxiang-home.md)
  - [wanxiang-user-agreement.md](source-captures/tongyi-wanxiang/wanxiang-user-agreement.md)
  - [wanxiang-privacy-policy.md](source-captures/tongyi-wanxiang/wanxiang-privacy-policy.md)
- Product page: <https://tongyi.aliyun.com/wan/generate/image>
- User agreement: <https://terms.alicdn.com/legal-agreement/terms/common_product_agreement/20230829115805343/20230829115805343.html>
- Privacy policy: <https://terms.alicdn.com/legal-agreement/terms/privacy_policy_full/20230829114337420/20230829114337420.html>
- Verified signals:
  - direct image-generation AI product page
  - product uses a product-specific agreement plus a full privacy policy
  - good benchmark for consumer-facing generative media products
  - local capture confirms media-generation framing and strong product-specific legal texts
- Best used for:
  - direct-use AI generation products
  - text-to-image, multimodal creation, prompt-input and output-heavy products
  - products needing stronger AI-output, content, and acceptable-use framing

#### 4. `provider_to_c_site_builder_with_workspace`

- Representative product: `万小智AI建站`
- Local captures:
  - [xiaozhi-home.md](source-captures/xiaozhi/xiaozhi-home.md)
  - [xiaozhi-user-agreement.md](source-captures/xiaozhi/xiaozhi-user-agreement.md)
  - [xiaozhi-privacy-baseline.md](source-captures/xiaozhi/xiaozhi-privacy-baseline.md)
- Product page: <https://wanwang.aliyun.com/website/xiaozhi/>
- Product landing details: <https://wanwang.aliyun.com/website/index>
- User agreement: <https://terms.alicdn.com/legal-agreement/terms/common_product_agreement/20250530202906989/20250530202906989.html>
- Privacy baseline: <https://terms.aliyun.com/legal-agreement/terms/suit_bu1_ali_cloud/suit_bu1_ali_cloud202107091605_49213.html>
- Verified signals:
  - product page states it is suitable for `个人、初创、小微企业`
  - product page advertises AI application development, AI creative image generation, AI online customer service, and AI content creation
  - product page states `独享企业工作空间` and data isolation or encrypted storage style claims
  - product is direct-service oriented but includes workspace, purchase, renewal, and operational data concerns
  - local captures confirm it uses a dedicated `智能建站服务协议` but broader Aliyun privacy baseline
- Best used for:
  - direct-use AI productivity products with purchase and renewal flows
  - products with workspace, business data isolation, online customer service, content generation, or website-building features
  - hybrid consumer or SMB products without strict enterprise certification

### B. Technical Support Role

#### 5. `supporter_console_platform`

- Representative product: `阿里云百炼`
- Local captures:
  - [bailian-home.md](source-captures/bailian/bailian-home.md)
  - [bailian-service-agreement.md](source-captures/bailian/bailian-service-agreement.md)
- Product page: <https://bailian.console.aliyun.com/>
- User agreement: <https://terms.alicdn.com/legal-agreement/terms/common_platform_service/20230728213935489/20230728213935489.html>
- Privacy baseline: <https://terms.aliyun.com/legal-agreement/terms/suit_bu1_ali_cloud/suit_bu1_ali_cloud202107091605_49213.html>
- Verified signals:
  - official agreement title is `阿里云百炼服务协议`
  - agreement text explicitly mentions API opening, system integration, and platform-style access
  - product is better characterized as a platform or technical support layer rather than a simple consumer chatbot
  - local product capture emphasizes model platform capabilities and builder-oriented scenarios
- Best used for:
  - model platform, API platform, agent-building console, or application-building platform
  - cases where the provider is a platform or technical enabler
  - products where API, integration, billing, and account-console rules matter more than end-user social behavior

#### 6. `supporter_enterprise_agent_platform`

- Representative product: `AgentOne`
- Local captures:
  - [agentone-home.md](source-captures/agentone/agentone-home.md)
  - [agentone-service-agreement.md](source-captures/agentone/agentone-service-agreement.md)
  - [agentone-privacy.md](source-captures/agentone/agentone-privacy.md)
- Product page: <https://www.lydaas.com/agentone>
- Service agreement: <https://www.lydaas.com/wow/z/lydaas/default/service-agreement?spm=a1z24v7z.32451059.0.0.5b3d69c4HfRue3>
- Personal information protection: <https://www.lydaas.com/wow/z/lydaas/default/personal-information-protection?spm=a1z24v7z.32451059.0.0.5b3d69c4HfRue3>
- Verified signals:
  - official site describes it as an enterprise platform helping customers quickly build and deploy AI agents or digital employees
  - role positioning is enterprise deployment and operation support rather than consumer content generation
  - local captures confirm enterprise platform language and platform service agreement structure
- Best used for:
  - enterprise-only AI agent platforms
  - products requiring organization setup, admin roles, employee roles, or workspaces
  - products where the operator is closer to technical support and infrastructure enablement

### C. Work AI or Claw Products with Higher Tool Risk

#### 7. `work_ai_claw_high_privilege`

- Representative products:
  - `JVS Claw`: <https://jvsclaw.aliyun.com/>
  - `钉钉悟空`: <https://wukong.dingtalk.com/>
  - `ArkClaw`: <https://www.volcengine.com/experience/ark?mode=claw>
- Local captures:
  - [jvsclaw-home.md](source-captures/jvsclaw/jvsclaw-home.md)
  - [jvsclaw-user-agreement.md](source-captures/jvsclaw/jvsclaw-user-agreement.md)
  - [wukong-home.md](source-captures/wukong/wukong-home.md)
  - [wukong-service-agreement.md](source-captures/wukong/wukong-service-agreement.md)
  - [wukong-privacy-policy.md](source-captures/wukong/wukong-privacy-policy.md)
  - [arkclaw-home.md](source-captures/arkclaw/arkclaw-home.md)
  - [arkclaw-product-doc.md](source-captures/arkclaw/arkclaw-product-doc.md)
  - [arkclaw-privacy-policy.md](source-captures/arkclaw/arkclaw-privacy-policy.md)
- Legal sources:
  - JVS Claw service agreement: <https://terms.alicdn.com/legal-agreement/terms/c_end_product_protocol/20260209152747220/20260209152747220.html>
  - 悟空 software and service agreement: <https://terms.alicdn.com/legal-agreement/terms/c_end_product_protocol/20260314103425642/20260314103425642.html>
  - 悟空 privacy policy: <https://terms.alicdn.com/legal-agreement/terms/c_end_product_protocol/20260314112436951/20260314112436951.html>
  - ArkClaw service terms: <https://www.volcengine.com/docs/6256/64903?lang=zh>
  - ArkClaw privacy policy: <https://www.volcengine.com/docs/6256/64902?lang=zh>
  - ArkClaw product and safety material: <https://www.volcengine.com/docs/82379/2229122?lang=zh>
- Verified signals:
  - 悟空 official page describes it as an `AI 工作平台`
  - 悟空 privacy policy explicitly mentions smart Q&A, automated execution, tool calling, webpage interaction, file processing, and task orchestration
  - ArkClaw community and official material repeatedly position it as a cloud-hosted agent product with skills, tool access, sandboxing, and higher safety or permission concerns
  - JVS Claw has a dedicated service agreement and belongs to the same higher-risk claw or agent family
  - local JVS Claw capture shows `自动化执行`、`网络深度检索`、`文件整理`
  - local ArkClaw capture shows `多模型多技能`、`Skills 安全拦截`、`安全私有托管`
  - local 悟空 captures confirm `工具调用`、`网页交互`、`文件处理`、`任务编排`
- Best used for:
  - products with skill access, file handling, webpage interaction, tool invocation, or local or sandbox execution features
  - work-agent products where privacy policy must explicitly cover files, websites, plugins, tools, models, and high-risk operations
  - products needing stronger sections on execution boundaries, permissions, tool safety, third-party model or site interaction, and user responsibility

## Practical Mapping Rules

- If the target product is a direct AI assistant with mobile login and no enterprise certification, start from `provider_to_c_mobile_login_ai_assistant` or `provider_to_c_mobile_login_ai_media_strong_product_terms`.
- If the target product sits inside a cloud console, exposes APIs, or mainly supports builders and developers, start from `supporter_console_platform`.
- If the target product is for enterprise deployment with admins, employees, or workspaces, start from `supporter_enterprise_agent_platform`.
- If the target product can call tools, access files, browse pages, invoke skills, or perform action-like agent tasks, prefer `work_ai_claw_high_privilege` even if it also looks `to C`.

## Cautions

- Some products inherit the broader Aliyun account or privacy layer rather than using a dedicated product privacy text. Do not force a product-specific privacy structure if the verified source shows account-layer inheritance.
- Public product pages may describe capabilities and target customers but not the full legal boundary. Always let the actual agreement or privacy text win when the two differ.
- Some captures may contain page chrome, media, or partial boilerplate. Before using a capture as a basis for drafting, inspect the first 20 to 40 lines and at least one section deeper in the file.

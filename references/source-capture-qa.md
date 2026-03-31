# Source Capture QA

This file records quality acceptance for the locally captured online references under [source-captures/](source-captures/).

Use it before relying on a public capture for archetype matching or clause-style extraction.

## Acceptance Labels

- `A usable`: the capture includes enough agreement or privacy正文 to support structure extraction and clause-style comparison.
- `B usable with caveats`: the capture is helpful for product positioning or ecosystem signals, but should not be the only basis for section design.
- `C weak`: the capture is too short, too generic, too noisy, or too incomplete to be trusted without re-fetching or cross-checking.

## Acceptance Checklist

Treat a capture as strong only when most of the following are true:

- the title is correct and product-specific or clearly ecosystem-specific
- the opening prompt, effective-date block, or first substantive section is present
- at least one deeper section is preserved beyond the opening block
- the text is mostly正文 rather than page chrome, media placeholders, or navigation noise
- the document type is clear: product agreement, privacy policy, platform terms, or product page

## Current QA Result

### 千问

- `A usable`: [qianwen-user-agreement.md](source-captures/qianwen-chat/qianwen-user-agreement.md)
  - clear title `千问用户服务协议`
  - includes更新/生效信息、接受动作、正文分节
- `A usable`: [qianwen-privacy-policy.md](source-captures/qianwen-chat/qianwen-privacy-policy.md)
  - clear title `千问产品隐私政策`
  - includes引言、目录式结构、信息收集与权利条款
- `B usable with caveats`: [qianwen-chat.md](source-captures/qianwen-chat/qianwen-chat.md)
  - good for product entry and direct-use positioning
  - too short for detailed legal drafting

### 通义听悟

- `B usable with caveats`: [tingwu-home.md](source-captures/tingwu/tingwu-home.md)
  - useful for confirming `音视频转文字`、`播客链接转写`、`智能总结要点`
  - product-page signal only
- `C weak`: [tingwu-user-agreement-baseline.md](source-captures/tingwu/tingwu-user-agreement-baseline.md)
  - extraction is too short to support reliable section borrowing
  - keep only as evidence that the product inherits a broader Aliyun agreement layer
- `A usable`: [tingwu-privacy-baseline.md](source-captures/tingwu/tingwu-privacy-baseline.md)
  - strong ecosystem-level privacy baseline
  - suitable for inherited privacy pattern analysis, not for product-specific facts

### 通义万相

- `A usable`: [wanxiang-user-agreement.md](source-captures/tongyi-wanxiang/wanxiang-user-agreement.md)
  - high-quality product agreement
  - excellent for consumer AI agreement structure
- `A usable`: [wanxiang-privacy-policy.md](source-captures/tongyi-wanxiang/wanxiang-privacy-policy.md)
  - strong full privacy policy with stable section layout
- `B usable with caveats`: [wanxiang-home.md](source-captures/tongyi-wanxiang/wanxiang-home.md)
  - enough to confirm product type
  - too short for anything beyond positioning

### 万小智

- `A usable`: [xiaozhi-user-agreement.md](source-captures/xiaozhi/xiaozhi-user-agreement.md)
  - dedicated smart site-builder agreement
  - useful for purchase, renewal, and service-order style clauses
- `A usable`: [xiaozhi-privacy-baseline.md](source-captures/xiaozhi/xiaozhi-privacy-baseline.md)
  - strong Aliyun privacy baseline
  - useful for inherited website-level privacy structure
- `B usable with caveats`: [xiaozhi-home.md](source-captures/xiaozhi/xiaozhi-home.md)
  - helpful for product positioning, workspace, AI employee, SMB targeting
  - contains some landing-page noise

### JVS Claw

- `A usable`: [jvsclaw-user-agreement.md](source-captures/jvsclaw/jvsclaw-user-agreement.md)
  - dedicated user agreement for the claw product family
  - useful for high-risk work-agent baseline selection
- `B usable with caveats`: [jvsclaw-home.md](source-captures/jvsclaw/jvsclaw-home.md)
  - useful product signals such as `自动化执行`、`网络深度检索`、`文件整理`
  - should not be used alone for legal structure

### 阿里云百炼

- `A usable`: [bailian-service-agreement.md](source-captures/bailian/bailian-service-agreement.md)
  - strong platform-style agreement
  - suitable for technical-support or builder-platform archetypes
- `B usable with caveats`: [bailian-home.md](source-captures/bailian/bailian-home.md)
  - helpful for platform positioning and builder scenarios
  - not a legal baseline by itself

### AgentOne

- `A usable`: [agentone-service-agreement.md](source-captures/agentone/agentone-service-agreement.md)
  - strong enterprise platform service agreement
  - useful for `to B` admin or employee archetypes
- `A usable`: [agentone-privacy.md](source-captures/agentone/agentone-privacy.md)
  - strong enterprise privacy baseline
- `B usable with caveats`: [agentone-home.md](source-captures/agentone/agentone-home.md)
  - confirms enterprise Agent platform positioning
  - includes media noise and marketing imagery

### 钉钉悟空

- `A usable`: [wukong-service-agreement.md](source-captures/wukong/wukong-service-agreement.md)
  - strong high-privilege AI-work agreement
  - explicitly covers工具调用、文件处理、网页操作、插件/技能扩展
- `A usable`: [wukong-privacy-policy.md](source-captures/wukong/wukong-privacy-policy.md)
  - strong privacy reference for agent execution, file processing, website interaction, and third-party model/plugin scenarios
- `B usable with caveats`: [wukong-home.md](source-captures/wukong/wukong-home.md)
  - useful for confirming `AI 工作平台` positioning
  - contains invitation-state and video shell noise

### ArkClaw

- `A usable`: [arkclaw-service-terms.md](source-captures/arkclaw/arkclaw-service-terms.md)
  - usable service-terms baseline for claw-type products
- `A usable`: [arkclaw-privacy-policy.md](source-captures/arkclaw/arkclaw-privacy-policy.md)
  - usable ecosystem privacy baseline
- `B usable with caveats`: [arkclaw-home.md](source-captures/arkclaw/arkclaw-home.md)
  - confirms ArkClaw product entry and hosted-assistant framing
- `B usable with caveats`: [arkclaw-product-doc.md](source-captures/arkclaw/arkclaw-product-doc.md)
  - useful for skills, safety interception, and托管 risk signals
  - extraction still contains nontrivial rendering noise

## Practical Use Rules

- Prefer `A usable` captures when borrowing section order, opening prompt style, and clause-grouping patterns.
- Use `B usable with caveats` captures mainly for product positioning, capability confirmation, and ecosystem inheritance signals.
- Do not use `C weak` captures as the sole basis for section design.
- If a target product maps mainly to a `B` or `C` source, combine it with the nearest `A usable` legal text from the same archetype family.

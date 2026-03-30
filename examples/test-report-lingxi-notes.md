# PRD Legal Drafter 测试报告

## 测试目标

验证该 Skill 是否能够基于一个企业 AI 产品 PRD：

- 正确抽取协议相关事实
- 区分用户协议与隐私政策的结构重点
- 在事实缺失时保留待确认项，而不是补造事实
- 输出带有来源说明的可审阅草案

## 测试输入

- 输入文件：[sample-prd-lingxi-notes.md](/Users/xianshi/Downloads/docs_skill/prd-legal-drafter/examples/sample-prd-lingxi-notes.md)
- 产品类型：企业 AI SaaS
- 复杂度覆盖点：`to B`、管理员/员工账号、手机号验证、订阅收费、AI 内容处理、第三方服务商、隐私权利路径

## 预期结果

- 产出两份草案：用户协议、隐私政策
- 输出事实清单和待确认事项
- 对“保存期限、跨境、退款细则”等 PRD 未明确问题保留占位符

## 实际结果

- 已产出完整测试输出文件：[sample-output-lingxi-notes.md](/Users/xianshi/Downloads/docs_skill/prd-legal-drafter/examples/sample-output-lingxi-notes.md)
- 该输出已按你提供的《万相服务协议》《万相隐私政策》做强结构参考，明显吸收了“审慎阅读/签约动作”“服务规范”“知识产权”“Cookie”“共享转让公开披露”“信息存储”等章节组织方式
- Skill 成功将企业签约、管理员/员工双角色、AI 输入输出处理和第三方能力接入反映到协议结构中
- Skill 未擅自补充保存期限、跨境传输、退款细则和 Cookie 管理机制，符合“不能捏造事实”的设计目标

## 测试结论

- 该 Skill 的核心流程是成立的，适合先作为“协议起草草案器 + 缺口识别器”使用
- 在没有内部协议库时，也能基于 PRD 输出一版接近阿里系产品协议风格的结构化草案
- 真正上线前，仍建议补齐内部模板库和字段数据库，以提高条款匹配度和法务一致性

## 建议的下一步增强

- 增加一个标准化 intake 表单，把 PRD 中常缺的法律字段单独补齐
- 接入内部用户协议/隐私政策模板库，替换目前的公开结构参考
- 增加“字段缺失即阻断 final publish”的更强校验模式

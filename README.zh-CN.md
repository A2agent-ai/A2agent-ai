# A2Agent

**通过一个兼容 OpenAI 与 Anthropic 的 API 网关，统一访问 GLM、Kimi、DeepSeek、Qwen 和 MiniMax。**

[官网](https://a2agent.me/) · [文档](https://docs.a2agent.me/) · [模型目录](https://docs.a2agent.me/models/overview) · [定价](https://docs.a2agent.me/models/pricing) · [服务状态](https://a2agent.me/status) · [控制台](https://a2agent.me/dashboard)

## 用户与开发者优惠

- 符合条件的新用户注册后可获得 **5 美元 API 体验额度**。
- 支持模型的价格通常比对应上游公开 API 标价低 **20%–50%**。
- 符合条件的订阅方案可享 **3 天免费试用**。
- 部分方案目前支持 **支付 60 美元获得 80 美元使用额度**，或**支付 100 美元获得 140 美元使用额度**。

可直接[创建账号](https://a2agent.me/dashboard)，购买前请查看[最新定价页面](https://docs.a2agent.me/models/pricing)。模型价格、套餐权益、活动范围和资格可能调整，请以控制台和最新活动条款为准。

## 与 A2Agent 合作

我们欢迎开源作者、Coding Agent 团队、API 工具和开发者社区与 A2Agent 合作。

- 符合条件的推广合作伙伴，可从有效推荐充值中获得 **5%–10% 的 Token 返还**。
- 开源作者可根据仓库活跃度、Star 数、技术匹配度和预期集成价值，申请 **20–100 美元 API 额度**。
- 影响力较好的项目可申请**每月持续 API 额度**和兼容性支持。
- 我们可以协助测试 OpenAI/Anthropic 端点、流式响应、工具调用、模型发现和集成文档。

技术集成请先提交 [Integration Request](https://github.com/A2agent-ai/a2agent-integrations/issues/new?template=integration_request.yml)；赞助、推荐合作和账号额度请使用[A2Agent 文档列出的私下支持渠道](https://docs.a2agent.me/account/status#contacting-support)。请勿在公开 PR 中填写商业条款或私人账号信息。

赠送额度不可转让或兑换现金。是否通过申请及是否提供持续支持，以项目审核和最新计划条款为准。

## 快速开始

先在控制台创建 API Key，再发送 OpenAI 兼容请求：

```bash
curl https://api.a2agent.me/v1/chat/completions \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "YOUR_MODEL_ID",
    "messages": [{"role": "user", "content": "你好！"}]
  }'
```

请先通过 `GET https://api.a2agent.me/v1/models` 获取当前可用的模型 ID。Pi、Hermes 和 Cline 的配置教程、示例与验证状态见 [a2agent-integrations](https://github.com/A2agent-ai/a2agent-integrations)。

## 隐私、安全与支持

请求正文通常不会被有意持久化，但临时处理、调试、安全调查及法律义务等情况可能构成例外。发送敏感数据前，请阅读最新的[隐私政策](https://docs.a2agent.me/help/privacy)。切勿将真实 API Key 提交到 GitHub。

技术集成和文档问题请提交 [GitHub Issue](https://github.com/A2agent-ai/a2agent-integrations/issues)；账号、充值和账单问题请使用[官网文档列出的支持渠道](https://docs.a2agent.me/account/status#contacting-support)。

[English](README.md)

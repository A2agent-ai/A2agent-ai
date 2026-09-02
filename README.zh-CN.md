# A2Agent

**通过一个兼容 OpenAI 与 Anthropic 的 API 网关，统一访问 GLM、Kimi、DeepSeek、Qwen 和 MiniMax。**

[官网](https://a2agent.me/) · [文档](https://docs.a2agent.me/) · [模型目录](https://docs.a2agent.me/models/overview) · [服务状态](https://a2agent.me/status) · [控制台](https://a2agent.me/dashboard)

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

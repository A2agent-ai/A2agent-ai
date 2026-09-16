# A2Agent

[English](README.md) | 简体中文 | [日本語](README.ja.md) | [한국어](README.ko.md)

**通过一个兼容 OpenAI、Anthropic 与 Gemini 的 API 网关，统一访问 GLM、Kimi、DeepSeek、Qwen 和 MiniMax。**

[官网](https://a2agent.me/) · [文档](https://docs.a2agent.me/) · [模型目录](https://a2agent.me/models) · [定价](https://a2agent.me/pricing) · [集成](https://a2agent.me/integrations) · [服务状态](https://a2agent.me/status) · [控制台](https://a2agent.me/dashboard)

[![A2Agent 官网概览](assets/a2agent-overview.jpg)](https://a2agent.me/)

## A2Agent 提供什么

- 使用一个 API Key 访问支持的 GLM、Kimi、DeepSeek、Qwen 和 MiniMax 模型。
- 支持 OpenAI Chat Completions 与 Responses、Anthropic Messages 和 Gemini GenerateContent 接口。
- 支持模型发现、流式响应、工具调用和 Coding Agent 集成。
- 提供实时模型价格和服务健康状态。
- 支持按量付费，并为更高并发和用量需求提供企业方案。

完整产品说明请参阅[什么是 A2Agent？](https://a2agent.me/what-is-a2agent)。A2Agent 与 Agent2Agent（A2A）协议没有关联。

## 快速开始

先在[控制台](https://a2agent.me/dashboard)创建 API Key，再发送 OpenAI 兼容请求：

```bash
curl https://api.a2agent.me/v1/chat/completions \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "YOUR_MODEL_ID",
    "messages": [{"role": "user", "content": "你好！"}]
  }'
```

选择模型前，请获取当前账号可用的模型 ID：

```bash
curl https://api.a2agent.me/v1/models \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY"
```

## 支持的接口

| 接口 | 端点 |
| --- | --- |
| OpenAI Chat Completions | `POST /v1/chat/completions` |
| OpenAI Responses | `POST /v1/responses` |
| Anthropic Messages | `POST /v1/messages` |
| Gemini GenerateContent | `POST /v1beta/models/{model}:generateContent` |
| 模型发现 | `GET /v1/models` |

不同模型和上游平台支持的能力可能不同。模型 ID 和能力请查看[实时模型目录](https://a2agent.me/models)，当前费率请查看[定价页面](https://a2agent.me/pricing)。

## 客户端集成

网站提供以下工具的配置教程：

- [Claude Code](https://a2agent.me/integrations/claude-code)
- [Codex CLI](https://a2agent.me/integrations/codex-cli)
- [Cline](https://a2agent.me/integrations/cline)
- [Roo Code](https://a2agent.me/integrations/roo-code)
- [Kilo Code](https://a2agent.me/integrations/kilo-code)
- [Cursor](https://a2agent.me/integrations/cursor)

[A2Agent 集成仓库](https://github.com/A2agent-ai/a2agent-integrations)还提供版本化教程、示例和兼容性测试。

## 实时与机器可读信息

- [模型目录](https://a2agent.me/models)和[定价](https://a2agent.me/pricing)
- [服务状态](https://a2agent.me/status)
- [llms.txt](https://a2agent.me/llms.txt) 和 [llms-full.txt](https://a2agent.me/llms-full.txt)
- [博客](https://a2agent.me/blog)和[站点地图](https://a2agent.me/sitemap.xml)

模型、价格、限制和活动可能变化，请以实时网站和控制台为准。

## 隐私与安全

请求正文通常不会被有意持久化，但临时处理、用户要求的调试、安全调查及法律义务等情况可能构成例外。使用前请阅读最新的[隐私政策](https://a2agent.me/privacy)、[服务条款](https://a2agent.me/terms)和[退款政策](https://a2agent.me/refund-policy)。

切勿提交真实 API Key。请使用环境变量或操作系统的凭据存储。

## 合作与支持

- 合作与推荐计划：[合作伙伴计划](https://a2agent.me/partners)
- 技术集成缺陷和文档修正：[GitHub Issues](https://github.com/A2agent-ai/a2agent-integrations/issues)
- 账号和账单支持：使用 [About 页面](https://a2agent.me/about)列出的联系渠道
- 安全漏洞：按照 [SECURITY.md](https://github.com/A2agent-ai/a2agent-integrations/blob/main/SECURITY.md) 中的说明私下报告

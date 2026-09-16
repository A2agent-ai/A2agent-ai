# A2Agent

English | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | [한국어](README.ko.md)

**One API gateway for GLM, Kimi, DeepSeek, Qwen, and MiniMax, with OpenAI-, Anthropic-, and Gemini-compatible interfaces.**

[Website](https://a2agent.me/) · [Documentation](https://docs.a2agent.me/) · [Models](https://a2agent.me/models) · [Pricing](https://a2agent.me/pricing) · [Integrations](https://a2agent.me/integrations) · [Status](https://a2agent.me/status) · [Dashboard](https://a2agent.me/dashboard)

[![A2Agent website overview](assets/a2agent-overview.jpg)](https://a2agent.me/)

## What A2Agent provides

- One API key for supported GLM, Kimi, DeepSeek, Qwen, and MiniMax models.
- OpenAI Chat Completions and Responses, Anthropic Messages, and Gemini GenerateContent interfaces.
- Model discovery, streaming, tool calls, and coding-agent integrations.
- Live model pricing and service-health information.
- Pay-as-you-go access, with enterprise options for higher concurrency and volume requirements.

Read [What is A2Agent?](https://a2agent.me/what-is-a2agent) for the full product overview. A2Agent is not affiliated with the Agent2Agent (A2A) protocol.

## Quick start

Create an API key in the [dashboard](https://a2agent.me/dashboard), then send an OpenAI-compatible request:

```bash
curl https://api.a2agent.me/v1/chat/completions \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "YOUR_MODEL_ID",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
```

Retrieve the model IDs available to your account before choosing a model:

```bash
curl https://api.a2agent.me/v1/models \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY"
```

## Supported interfaces

| Interface | Endpoint |
| --- | --- |
| OpenAI Chat Completions | `POST /v1/chat/completions` |
| OpenAI Responses | `POST /v1/responses` |
| Anthropic Messages | `POST /v1/messages` |
| Gemini GenerateContent | `POST /v1beta/models/{model}:generateContent` |
| Model discovery | `GET /v1/models` |

Feature support varies by model and upstream platform. Use the [live model catalog](https://a2agent.me/models) for model IDs and capabilities, and the [pricing page](https://a2agent.me/pricing) for current rates.

## Integrations

Setup guides are available for:

- [Claude Code](https://a2agent.me/integrations/claude-code)
- [Codex CLI](https://a2agent.me/integrations/codex-cli)
- [Cline](https://a2agent.me/integrations/cline)
- [Roo Code](https://a2agent.me/integrations/roo-code)
- [Kilo Code](https://a2agent.me/integrations/kilo-code)
- [Cursor](https://a2agent.me/integrations/cursor)

The [A2Agent integrations repository](https://github.com/A2agent-ai/a2agent-integrations) also contains versioned guides, examples, and compatibility tests.

## Live and machine-readable information

- [Model catalog](https://a2agent.me/models) and [pricing](https://a2agent.me/pricing)
- [Service status](https://a2agent.me/status)
- [llms.txt](https://a2agent.me/llms.txt) and [llms-full.txt](https://a2agent.me/llms-full.txt)
- [Blog](https://a2agent.me/blog) and [sitemap](https://a2agent.me/sitemap.xml)

Prices, model availability, limits, and promotions can change. The live website and dashboard are authoritative.

## Privacy and security

Request bodies are not ordinarily intentionally persisted. Temporary processing, user-requested debugging, security, and legal-obligation exceptions may apply. Review the current [Privacy Policy](https://a2agent.me/privacy), [Terms of Service](https://a2agent.me/terms), and [Refund Policy](https://a2agent.me/refund-policy) before use.

Never commit an API key. Use environment variables or your operating system's credential store.

## Partners and support

- Partnership and referral information: [Partner Programme](https://a2agent.me/partners)
- Technical integration bugs and documentation corrections: [GitHub Issues](https://github.com/A2agent-ai/a2agent-integrations/issues)
- Account and billing support: use the contact channels listed on the [About page](https://a2agent.me/about)
- Security vulnerabilities: follow the private reporting instructions in [SECURITY.md](https://github.com/A2agent-ai/a2agent-integrations/blob/main/SECURITY.md)

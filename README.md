# A2Agent

**One API gateway for GLM, Kimi, DeepSeek, Qwen, and MiniMax, with OpenAI- and Anthropic-compatible endpoints.**

[Website](https://a2agent.me/) · [Documentation](https://docs.a2agent.me/) · [Model catalog](https://docs.a2agent.me/models/overview) · [Service status](https://a2agent.me/status) · [Dashboard](https://a2agent.me/dashboard)

## Quick start

Create an API key in the dashboard, then send an OpenAI-compatible request:

```bash
curl https://api.a2agent.me/v1/chat/completions \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "YOUR_MODEL_ID",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
```

Retrieve the current model IDs before choosing a model:

```bash
curl https://api.a2agent.me/v1/models \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY"
```

## Supported interfaces

- OpenAI Chat Completions: `POST /v1/chat/completions`
- Anthropic Messages-compatible requests
- Model discovery: `GET /v1/models`

## Client integrations

The [A2Agent integrations repository](https://github.com/A2agent-ai/a2agent-integrations) contains versioned guides, examples, and compatibility tests for:

- [Pi Coding Agent](https://github.com/A2agent-ai/a2agent-integrations/blob/main/docs/clients/pi.md)
- [Hermes Agent](https://github.com/A2agent-ai/a2agent-integrations/blob/main/docs/clients/hermes-cli.md)
- [Cline](https://github.com/A2agent-ai/a2agent-integrations/blob/main/docs/clients/cline.md)

## Privacy and security

Request bodies are not ordinarily intentionally persisted. Temporary processing, debugging, security, and legal-obligation exceptions may apply. Read the current [privacy policy](https://docs.a2agent.me/help/privacy) before sending sensitive data.

Never commit an API key. Use environment variables or your operating system's credential store.

## Support

- Technical integration bugs and documentation corrections: [GitHub Issues](https://github.com/A2agent-ai/a2agent-integrations/issues)
- Account, top-up, and billing questions: use the support channel listed in the [A2Agent documentation](https://docs.a2agent.me/account/status#contacting-support)
- Security vulnerabilities: follow the private reporting instructions in [SECURITY.md](https://github.com/A2agent-ai/a2agent-integrations/blob/main/SECURITY.md)

[简体中文](README.zh-CN.md)

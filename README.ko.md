# A2Agent

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | 한국어

**OpenAI, Anthropic 및 Gemini 호환 인터페이스를 통해 GLM, Kimi, DeepSeek, Qwen, MiniMax를 하나의 API 게이트웨이에서 사용할 수 있습니다.**

[공식 사이트](https://a2agent.me/) · [문서](https://docs.a2agent.me/) · [모델 목록](https://a2agent.me/models) · [요금](https://a2agent.me/pricing) · [연동](https://a2agent.me/integrations) · [서비스 상태](https://a2agent.me/status) · [대시보드](https://a2agent.me/dashboard)

[![A2Agent 웹사이트 개요](assets/a2agent-overview.jpg)](https://a2agent.me/)

## A2Agent가 제공하는 기능

- 하나의 API 키로 지원되는 GLM, Kimi, DeepSeek, Qwen 및 MiniMax 모델을 이용할 수 있습니다.
- OpenAI Chat Completions 및 Responses, Anthropic Messages, Gemini GenerateContent 인터페이스를 지원합니다.
- 모델 검색, 스트리밍, 도구 호출 및 코딩 에이전트 연동을 제공합니다.
- 실시간 모델 요금과 서비스 상태를 확인할 수 있습니다.
- 사용량 기반 결제와 함께 높은 동시 실행 수 및 대규모 사용을 위한 기업 옵션을 제공합니다.

전체 제품 설명은 [A2Agent란?](https://a2agent.me/what-is-a2agent)을 참조하세요. A2Agent는 Agent2Agent(A2A) 프로토콜과 관련이 없습니다.

## 빠른 시작

[대시보드](https://a2agent.me/dashboard)에서 API 키를 만든 다음 OpenAI 호환 요청을 보내세요.

```bash
curl https://api.a2agent.me/v1/chat/completions \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "YOUR_MODEL_ID",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
```

모델을 선택하기 전에 계정에서 이용 가능한 모델 ID를 조회하세요.

```bash
curl https://api.a2agent.me/v1/models \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY"
```

## 지원 인터페이스

| 인터페이스 | 엔드포인트 |
| --- | --- |
| OpenAI Chat Completions | `POST /v1/chat/completions` |
| OpenAI Responses | `POST /v1/responses` |
| Anthropic Messages | `POST /v1/messages` |
| Gemini GenerateContent | `POST /v1beta/models/{model}:generateContent` |
| 모델 검색 | `GET /v1/models` |

지원 기능은 모델과 업스트림 플랫폼에 따라 다릅니다. 모델 ID와 기능은 [실시간 모델 목록](https://a2agent.me/models), 현재 요금은 [요금 페이지](https://a2agent.me/pricing)에서 확인하세요.

## 클라이언트 연동

다음 도구의 설정 가이드를 제공합니다.

- [Claude Code](https://a2agent.me/integrations/claude-code)
- [Codex CLI](https://a2agent.me/integrations/codex-cli)
- [Cline](https://a2agent.me/integrations/cline)
- [Roo Code](https://a2agent.me/integrations/roo-code)
- [Kilo Code](https://a2agent.me/integrations/kilo-code)
- [Cursor](https://a2agent.me/integrations/cursor)

[A2Agent 연동 저장소](https://github.com/A2agent-ai/a2agent-integrations)에는 버전 관리 가이드, 예제 및 호환성 테스트도 포함되어 있습니다.

## 실시간 및 기계 판독 가능 정보

- [모델 목록](https://a2agent.me/models)과 [요금](https://a2agent.me/pricing)
- [서비스 상태](https://a2agent.me/status)
- [llms.txt](https://a2agent.me/llms.txt) 및 [llms-full.txt](https://a2agent.me/llms-full.txt)
- [블로그](https://a2agent.me/blog)와 [사이트맵](https://a2agent.me/sitemap.xml)

모델, 요금, 한도 및 프로모션은 변경될 수 있습니다. 실시간 웹사이트와 대시보드를 기준으로 합니다.

## 개인정보 보호 및 보안

일반적으로 요청 본문을 의도적으로 영구 저장하지 않습니다. 다만 임시 처리, 사용자가 요청한 디버깅, 보안 대응 및 법적 의무에 따른 예외가 적용될 수 있습니다. 이용 전에 최신 [개인정보 처리방침](https://a2agent.me/privacy), [서비스 약관](https://a2agent.me/terms), [환불 정책](https://a2agent.me/refund-policy)을 확인하세요.

API 키를 커밋하지 마세요. 환경 변수나 운영체제의 자격 증명 저장소를 사용하세요.

## 파트너 및 지원

- 파트너십 및 추천 정보: [파트너 프로그램](https://a2agent.me/partners)
- 기술 연동 오류 및 문서 수정: [GitHub Issues](https://github.com/A2agent-ai/a2agent-integrations/issues)
- 계정 및 청구 지원: [About 페이지](https://a2agent.me/about)에 안내된 연락 채널을 이용하세요
- 보안 취약점: [SECURITY.md](https://github.com/A2agent-ai/a2agent-integrations/blob/main/SECURITY.md)의 절차에 따라 비공개로 신고하세요

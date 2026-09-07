# A2Agent

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.ja.md) | 한국어

**OpenAI 및 Anthropic 호환 엔드포인트를 통해 GLM, Kimi, DeepSeek, Qwen, MiniMax를 하나의 API 게이트웨이에서 사용할 수 있습니다.**

[공식 사이트](https://a2agent.me/) · [문서](https://docs.a2agent.me/) · [모델 목록](https://docs.a2agent.me/models/overview) · [요금](https://docs.a2agent.me/models/pricing) · [서비스 상태](https://a2agent.me/status) · [대시보드](https://a2agent.me/dashboard)

[![A2Agent 웹사이트 개요](assets/a2agent-overview.jpg)](https://a2agent.me/)

## 사용자와 개발자를 위한 혜택

- 자격 요건을 충족하는 신규 계정에는 **미화 5달러 상당의 API 체험 크레딧**이 제공됩니다.
- 지원 모델의 요금은 일반적으로 **해당 모델 제공업체가 공개한 API 정가보다 20%~50% 낮습니다**.
- 대상 구독에는 **3일 무료 체험**이 포함될 수 있습니다.
- 현재 일부 요금제에서는 **60달러로 80달러 상당**, 또는 **100달러로 140달러 상당**을 사용할 수 있습니다.

[계정을 만들거나](https://a2agent.me/dashboard) 구매 전에 [최신 요금 페이지](https://docs.a2agent.me/models/pricing)를 확인하세요. 제공 여부, 모델 요금, 요금제 혜택 및 자격 요건은 변경될 수 있습니다. 실제 대시보드와 공개된 프로그램 약관을 기준으로 합니다.

## A2Agent와의 협력

오픈 소스 관리자, 코딩 에이전트 팀, API 도구 개발자 및 개발자 커뮤니티와 협력합니다.

- 자격 요건을 충족하는 추천 파트너는 추천받은 사용자의 대상 충전 건에 대해 **5%~10%의 토큰 환급**을 받을 수 있습니다.
- 오픈 소스 개발자는 저장소 활동, 스타 수, 기술 적합성 및 예상 연동 가치를 바탕으로 **20~100달러 상당의 API 크레딧**을 받을 수 있습니다.
- 영향력이 큰 프로젝트에는 **매월 지속적으로 제공되는 API 크레딧**과 호환성 지원을 검토합니다.
- OpenAI/Anthropic 엔드포인트 테스트, 스트리밍, 도구 호출, 모델 검색 및 연동 문서 작성을 지원할 수 있습니다.

기술 연동을 논의하려면 [Integration Request](https://github.com/A2agent-ai/a2agent-integrations/issues/new?template=integration_request.yml)를 등록하세요. 후원, 추천 제휴 또는 계정 크레딧에 관한 상담은 [A2Agent 문서](https://docs.a2agent.me/account/status#contacting-support)에 안내된 비공개 지원 채널을 이용하세요. 공개 PR에 거래 조건이나 비공개 계정 정보를 기재하지 마세요.

크레딧은 프로모션용이며 양도하거나 현금으로 교환할 수 없습니다. 승인 및 지속적인 지원은 프로젝트 심사와 현행 프로그램 약관에 따릅니다.

## 빠른 시작

대시보드에서 API 키를 만든 다음 OpenAI 호환 요청을 보내세요.

```bash
curl https://api.a2agent.me/v1/chat/completions \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "YOUR_MODEL_ID",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
```

모델을 선택하기 전에 현재 사용 가능한 모델 ID를 조회하세요.

```bash
curl https://api.a2agent.me/v1/models \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY"
```

## 지원 인터페이스

- OpenAI Chat Completions: `POST /v1/chat/completions`
- Anthropic Messages 호환 요청
- 모델 검색: `GET /v1/models`

## 클라이언트 연동

[A2Agent 연동 저장소](https://github.com/A2agent-ai/a2agent-integrations)는 다음 클라이언트의 버전 관리 가이드, 예제 및 호환성 테스트를 제공합니다.

- [Pi Coding Agent](https://github.com/A2agent-ai/a2agent-integrations/blob/main/docs/clients/pi.md)
- [Hermes Agent](https://github.com/A2agent-ai/a2agent-integrations/blob/main/docs/clients/hermes-cli.md)
- [Cline](https://github.com/A2agent-ai/a2agent-integrations/blob/main/docs/clients/cline.md)

## 개인정보 보호 및 보안

일반적으로 요청 본문을 의도적으로 영구 저장하지 않습니다. 다만 임시 처리, 디버깅, 보안 대응 및 법적 의무 등에 따른 예외가 적용될 수 있습니다. 민감한 정보를 보내기 전에 최신 [개인정보 처리방침](https://docs.a2agent.me/help/privacy)을 확인하세요.

API 키를 커밋하지 마세요. 환경 변수나 운영체제의 자격 증명 저장소를 사용하세요.

## 지원

- 기술 연동 오류 및 문서 수정: [GitHub Issues](https://github.com/A2agent-ai/a2agent-integrations/issues)
- 계정, 충전 및 청구 관련 문의: [A2Agent 문서](https://docs.a2agent.me/account/status#contacting-support)에 안내된 지원 채널을 이용하세요
- 보안 취약점: [SECURITY.md](https://github.com/A2agent-ai/a2agent-integrations/blob/main/SECURITY.md)의 비공개 신고 절차를 따르세요

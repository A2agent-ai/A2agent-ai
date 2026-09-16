# A2Agent

[English](README.md) | [简体中文](README.zh-CN.md) | 日本語 | [한국어](README.ko.md)

**OpenAI、Anthropic、Gemini 互換インターフェースを備えた、GLM、Kimi、DeepSeek、Qwen、MiniMax 向けの統合 API ゲートウェイ。**

[公式サイト](https://a2agent.me/) · [ドキュメント](https://docs.a2agent.me/) · [モデル一覧](https://a2agent.me/models) · [料金](https://a2agent.me/pricing) · [連携](https://a2agent.me/integrations) · [稼働状況](https://a2agent.me/status) · [ダッシュボード](https://a2agent.me/dashboard)

[![A2Agent 公式サイトの概要](assets/a2agent-overview.jpg)](https://a2agent.me/)

## A2Agent の機能

- 1 つの API キーで、対応する GLM、Kimi、DeepSeek、Qwen、MiniMax モデルにアクセスできます。
- OpenAI Chat Completions と Responses、Anthropic Messages、Gemini GenerateContent インターフェースに対応します。
- モデル検出、ストリーミング、ツール呼び出し、コーディングエージェント連携を提供します。
- モデル料金とサービスの稼働状況をリアルタイムで確認できます。
- 従量課金に加え、高い同時実行数や大規模利用向けの法人オプションを提供します。

詳しい製品概要は [A2Agent とは？](https://a2agent.me/what-is-a2agent) をご覧ください。A2Agent は Agent2Agent（A2A）プロトコルとは関係ありません。

## クイックスタート

[ダッシュボード](https://a2agent.me/dashboard)で API キーを作成し、OpenAI 互換リクエストを送信します。

```bash
curl https://api.a2agent.me/v1/chat/completions \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "YOUR_MODEL_ID",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
```

モデルを選ぶ前に、アカウントで利用可能なモデル ID を取得してください。

```bash
curl https://api.a2agent.me/v1/models \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY"
```

## 対応インターフェース

| インターフェース | エンドポイント |
| --- | --- |
| OpenAI Chat Completions | `POST /v1/chat/completions` |
| OpenAI Responses | `POST /v1/responses` |
| Anthropic Messages | `POST /v1/messages` |
| Gemini GenerateContent | `POST /v1beta/models/{model}:generateContent` |
| モデル検出 | `GET /v1/models` |

利用できる機能はモデルや上流プラットフォームによって異なります。モデル ID と機能は[最新のモデル一覧](https://a2agent.me/models)、現在の料金は[料金ページ](https://a2agent.me/pricing)で確認してください。

## クライアント連携

次のツール向けセットアップガイドを公開しています。

- [Claude Code](https://a2agent.me/integrations/claude-code)
- [Codex CLI](https://a2agent.me/integrations/codex-cli)
- [Cline](https://a2agent.me/integrations/cline)
- [Roo Code](https://a2agent.me/integrations/roo-code)
- [Kilo Code](https://a2agent.me/integrations/kilo-code)
- [Cursor](https://a2agent.me/integrations/cursor)

[A2Agent 連携リポジトリ](https://github.com/A2agent-ai/a2agent-integrations)には、バージョン管理されたガイド、サンプル、互換性テストもあります。

## 最新情報と機械可読データ

- [モデル一覧](https://a2agent.me/models)と[料金](https://a2agent.me/pricing)
- [サービス稼働状況](https://a2agent.me/status)
- [llms.txt](https://a2agent.me/llms.txt) と [llms-full.txt](https://a2agent.me/llms-full.txt)
- [ブログ](https://a2agent.me/blog)と[サイトマップ](https://a2agent.me/sitemap.xml)

モデル、料金、制限、キャンペーンは変更される場合があります。最新のウェブサイトとダッシュボードを基準としてください。

## プライバシーとセキュリティ

通常、リクエスト本文を意図的に永続保存することはありません。ただし、一時処理、ユーザーが依頼したデバッグ、セキュリティ対応、法的義務などの例外があります。利用前に最新の[プライバシーポリシー](https://a2agent.me/privacy)、[利用規約](https://a2agent.me/terms)、[返金ポリシー](https://a2agent.me/refund-policy)をご確認ください。

API キーをコミットしないでください。環境変数または OS の認証情報ストアを利用してください。

## パートナーとサポート

- パートナー・紹介情報：[パートナープログラム](https://a2agent.me/partners)
- 技術的な連携不具合とドキュメント修正：[GitHub Issues](https://github.com/A2agent-ai/a2agent-integrations/issues)
- アカウントと請求のサポート：[About ページ](https://a2agent.me/about)に記載された連絡先をご利用ください
- セキュリティ上の脆弱性：[SECURITY.md](https://github.com/A2agent-ai/a2agent-integrations/blob/main/SECURITY.md) の手順に従い非公開で報告してください

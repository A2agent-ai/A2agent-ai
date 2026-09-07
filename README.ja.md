# A2Agent

[English](README.md) | [简体中文](README.zh-CN.md) | 日本語 | [한국어](README.ko.md)

**OpenAI および Anthropic 互換のエンドポイントを備えた、GLM、Kimi、DeepSeek、Qwen、MiniMax 向けの統合 API ゲートウェイ。**

[公式サイト](https://a2agent.me/) · [ドキュメント](https://docs.a2agent.me/) · [モデル一覧](https://docs.a2agent.me/models/overview) · [料金](https://docs.a2agent.me/models/pricing) · [稼働状況](https://a2agent.me/status) · [ダッシュボード](https://a2agent.me/dashboard)

[![A2Agent 公式サイトの概要](assets/a2agent-overview.jpg)](https://a2agent.me/)

## ユーザーと開発者向けの特典

- 条件を満たす新規アカウントには、**5 米ドル分の API お試しクレジット**が付与されます。
- 対応モデルの料金は通常、**各提供元が公開する API 定価より 20%～50% 低く**設定されています。
- 対象のサブスクリプションには、**3 日間の無料トライアル**が含まれる場合があります。
- 現在、一部のプランでは **60 米ドルで 80 米ドル分**、または **100 米ドルで 140 米ドル分**を利用できます。

[アカウントを作成](https://a2agent.me/dashboard)するか、購入前に[最新の料金ページ](https://docs.a2agent.me/models/pricing)をご確認ください。提供状況、モデル料金、プランの特典、適用条件は変更される場合があります。ダッシュボードと公開されているプログラム規約を優先してください。

## A2Agent とのパートナーシップ

オープンソースのメンテナー、コーディングエージェントの開発チーム、API ツール、開発者コミュニティとの協力を歓迎します。

- 条件を満たす紹介パートナーは、対象となる紹介先のチャージに対して **5%～10% のトークン還元**を受けられる場合があります。
- オープンソース開発者には、リポジトリの活動状況、スター数、技術的な適合性、連携に期待される価値に応じて、**20～100 米ドル分の API クレジット**を提供する場合があります。
- 影響力の大きいプロジェクトには、**毎月継続して付与される API クレジット**と互換性サポートを検討します。
- OpenAI/Anthropic エンドポイントのテスト、ストリーミング、ツール呼び出し、モデル検出、連携ドキュメントの作成を支援できます。

技術的な連携については、[Integration Request](https://github.com/A2agent-ai/a2agent-integrations/issues/new?template=integration_request.yml) を作成してください。スポンサーシップ、紹介提携、アカウントのクレジットに関する相談には、[A2Agent ドキュメント](https://docs.a2agent.me/account/status#contacting-support)に記載された非公開のサポート窓口をご利用ください。公開 PR に商取引の条件や非公開のアカウント情報を記載しないでください。

クレジットはプロモーション用で、譲渡や換金はできません。承認および継続的な支援は、プロジェクトの審査と現行のプログラム規約に従います。

## クイックスタート

ダッシュボードで API キーを作成し、OpenAI 互換のリクエストを送信します。

```bash
curl https://api.a2agent.me/v1/chat/completions \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "YOUR_MODEL_ID",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
```

モデルを選ぶ前に、現在利用可能なモデル ID を取得してください。

```bash
curl https://api.a2agent.me/v1/models \
  -H "Authorization: Bearer YOUR_A2AGENT_KEY"
```

## 対応インターフェース

- OpenAI Chat Completions: `POST /v1/chat/completions`
- Anthropic Messages 互換のリクエスト
- モデル検出: `GET /v1/models`

## クライアント連携

[A2Agent 連携リポジトリ](https://github.com/A2agent-ai/a2agent-integrations)では、次のクライアント向けに、バージョン管理されたガイド、サンプル、互換性テストを提供しています。

- [Pi Coding Agent](https://github.com/A2agent-ai/a2agent-integrations/blob/main/docs/clients/pi.md)
- [Hermes Agent](https://github.com/A2agent-ai/a2agent-integrations/blob/main/docs/clients/hermes-cli.md)
- [Cline](https://github.com/A2agent-ai/a2agent-integrations/blob/main/docs/clients/cline.md)

## プライバシーとセキュリティ

通常、リクエスト本文を意図的に永続保存することはありません。ただし、一時的な処理、デバッグ、セキュリティ対応、法的義務などにより例外が生じる場合があります。機密情報を送信する前に、最新の[プライバシーポリシー](https://docs.a2agent.me/help/privacy)をご確認ください。

API キーをコミットしないでください。環境変数または OS の認証情報ストアを利用してください。

## サポート

- 技術的な連携の不具合やドキュメントの修正: [GitHub Issues](https://github.com/A2agent-ai/a2agent-integrations/issues)
- アカウント、チャージ、請求に関する質問: [A2Agent ドキュメント](https://docs.a2agent.me/account/status#contacting-support)に記載されたサポート窓口をご利用ください
- セキュリティ上の脆弱性: [SECURITY.md](https://github.com/A2agent-ai/a2agent-integrations/blob/main/SECURITY.md) の手順に従い、非公開で報告してください

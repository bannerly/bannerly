# bannerly

**bannerly** は、広告配信プラットフォーム **bannerly** のプロジェクトです。
bannerly は、スタートアップや小規模サービスのための軽量な広告配信サーバーです。運用者は各自の Cloudflare にデプロイして使うセルフホスト型で、自社の Web サイトやアプリに広告枠を持ち、提携先への直接販売と空き枠のバックフィルを、ひとつの管理画面で運用できます。

## リポジトリ

| リポジトリ | 内容 |
|---|---|
| [server](https://github.com/bannerly/server) | bannerly 広告配信サーバー（Cloudflare Workers / D1 / KV / Queues） |
| [sdk](https://github.com/bannerly/sdk) | Expo / React Native 用クライアント SDK |
| [manifest](https://github.com/bannerly/manifest) | 全リポジトリをまとめて取得するための tsrc マニフェスト |

## まとめて取得する

[tsrc](https://your-tools.github.io/tsrc/) を使うと、全リポジトリをワークスペースにまとめて clone / sync できます。

```sh
pipx install tsrc

mkdir bannerly && cd bannerly
tsrc init https://github.com/bannerly/manifest.git
tsrc sync
```

## bannerly の特徴

- セルフホスト — 運用者は各自の Cloudflare にデプロイして使う（テナントは1デプロイ内の仕分け単位）
- 配信ルール — 優先度（Override / Contract / Remnant）、重み付け、地域、曜日・時間帯、日次上限、フリークエンシーキャップ
- クリエイティブ2形式 — HTML と、アプリでネイティブ描画できる構造化形式
- 審査フローと販売フロー — バナー審査、プラン申込から契約キャンペーンの自動生成まで
- レポート — 期間指定レポートと、広告主ごとの月次レポート（CSV 対応）

詳しくは [server リポジトリの README](https://github.com/bannerly/server#readme) を参照してください。

## ライセンス

各リポジトリは MIT License で公開されています。

---

bannerly is developed by RE-X K.K.

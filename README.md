# じすいメモ Ver.1

自炊初心者向けの、シンプルな食材管理＋GPT相談アプリです。

## できること
- 食材名と量を登録・編集・削除
- データをブラウザの localStorage に保存
- 「今日何作る？」の条件を選んでGPT向けプロンプト生成
- 「買い物する」の条件を選んでGPT向けプロンプト生成
- スーパーで安い食材を見つけた時の購入相談プロンプト生成
- 生成したプロンプトをコピー

## スマホで使う方法
このフォルダを静的Webサーバーに置くと、そのままスマホブラウザで使えます。
例：GitHub Pages / Netlify / Vercel / Cloudflare Pages など。

iPhoneではSafariで開き、
共有 →「ホーム画面に追加」
にするとアプリ風に使えます。

## ローカルで試す
PCでこのフォルダを開き、ターミナルで以下を実行します。

python3 -m http.server 8000

その後 http://localhost:8000 を開いてください。

## 将来拡張しやすいポイント
現在はUI・食材データ・プロンプト生成を1ファイルにまとめていますが、
次の段階では以下を分離できます。

- data / storage
- prompt builders
- AI client
- recipe history
- meal prep
- expiry tracking

OpenAI API接続時は、プロンプト生成関数の出力をAPIクライアントへ渡す構造にできます。

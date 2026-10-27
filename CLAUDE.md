# 生成AI研修 参加報告（同僚向け）

2026年10月27日の校外研修「教職員向け 生成AI活用研修」（会場：川崎市立橘高校）の内容を、同僚の先生向けに専門用語なしでまとめたページ。

- 公開URL：https://upopotennis-gif.github.io/ai-kenshu-houkoku/
- リポジトリ：git@github.com:upopotennis-gif/ai-kenshu-houkoku.git（main / root）
- 非公開版（claude.ai）：https://claude.ai/artifact/7W3SNjCppcub86q1ecTU9R

## ファイル
- `ai-kenshu.html`：元のページ（claude.ai用。doctype・head なし）。直すのはこちら
- `index.html`：GitHub Pages 用。`ai-kenshu.html` に doctype・head・body をかぶせて作る
- `生成AI研修_参加報告.pdf`：印刷用（A4）。index.html を Chrome の headless で PDF にしたもの

## 更新の手順
1. `ai-kenshu.html` を直す
2. index.html を作り直す（head に charset・viewport・noindex を入れ、`</style>` までを head、残りを body に）
3. PDF を作り直す：`"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --no-pdf-header-footer --virtual-time-budget=8000 --print-to-pdf=生成AI研修_参加報告.pdf file://$PWD/index.html`
4. スマホ幅で確認 → `git add -A && git commit -m "…" && git push`

## まだのこと
- 研修の音声（講師の話）を書き起こして足す。音声はまだ届いていない（講師スライドは反映済み）

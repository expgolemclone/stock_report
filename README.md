# Stock Report

銘柄レポートをブラウザで閲覧する静的サイト。

## Preview

```sh
python -m http.server 8765
```

ブラウザで http://localhost:8765 を開く。

## 構成

```
index.html              一覧ページ
viewer.html             MDレンダラー（HTMLがない銘柄用）
assets/{ticker}/        各銘柄のレポート（.html または .md）
```

## 銘柄の追加

1. `assets/{ticker}/{ticker}.md` を配置
2. `index.html` の `TICKERS` と `viewer.html` の `TICKER_NAMES` に追記
3. プレゼン形式の HTML を作成した場合は `hasHtml: true` に変更

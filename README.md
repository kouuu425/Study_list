# インプット型プロダクトバックログ

学習ロードマップを管理する静的 Web アプリです。`index.html` 単体で動作します。

## ホスティング

### GitHub Pages（推奨）

このリポジトリはすでに GitHub Pages で公開されています。

**URL:** `https://kouuu425.github.io/Study_list/`

`main` ブランチに push すると自動で反映されます。

---

### Cloudflare Pages

1. [Cloudflare Pages](https://pages.cloudflare.com/) にログイン
2. 「Create a project」→「Connect to Git」でこのリポジトリを選択
3. ビルド設定はすべて空欄のまま「Save and Deploy」

### Vercel

```bash
npx vercel --yes
```

---

## ローカルで開く

ブラウザで `index.html` を直接開くだけで動作します。

```bash
open index.html
```

## PBI の追加・編集

`index.html` 内の `DATA` 配列を編集してください。

```js
{
  id: 9,                      // 連番
  title: 'タイトル',
  done: false,                // 完了済みは true
  steps: ['手順1', '手順2'], // 任意
  sources: [
    { category: 'カテゴリ名', items: [
      { label: 'リンク名', url: 'https://...' },  // URL なしは null
    ]}
  ],
  goals: ['完了目安1', '完了目安2']  // 任意
}
```

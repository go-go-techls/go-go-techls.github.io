# テックルズ ホームページ

福祉 × デザイン × テクノロジーのチーム「テックルズ」の公式サイト（GitHub Pages 用の静的サイト）。

## 構成

```
.
├── index.html        # トップページ（1 ページ完結）
├── styles.css        # スタイル
├── assets/           # ロゴ・写真
├── .nojekyll         # Jekyll 処理を無効化（静的ファイルをそのまま配信）
└── CNAME             # （任意）独自ドメインを使う場合に作成
```

## ローカルで確認する

```sh
# どちらでも OK
python3 -m http.server 8000
# → http://localhost:8000
```

## GitHub Pages で公開する

1. GitHub にリポジトリを作成（例：`techls/techls.github.io` または任意のリポジトリ）
2. このディレクトリを push する
   ```sh
   git add -A
   git commit -m "テックルズのホームページを公開"
   git branch -M main
   git remote add origin git@github.com:<ORG_OR_USER>/<REPO>.git
   git push -u origin main
   ```
3. リポジトリの **Settings → Pages** で、Source を `Deploy from a branch`、Branch を `main` / `(root)` に設定
4. 数分後、`https://<USER>.github.io/<REPO>/` で公開される

## 独自ドメイン（techls.org など）を使う場合

1. リポジトリ直下に `CNAME` ファイルを作成し、使いたいドメインを 1 行だけ書く
   ```
   www.techls.org
   ```
2. DNS 側で GitHub Pages 向けのレコードを設定
   - サブドメイン（`www` など）→ `CNAME` レコードで `<USER>.github.io` を指す
   - apex（`techls.org`）→ GitHub Pages の A / AAAA レコードを設定
3. Settings → Pages の **Custom domain** に同じドメインを入力し、**Enforce HTTPS** を有効化

> アプリ「ええやん.ai!」はすでに `eeyan-ai.techls.org` で稼働中。本サイトは `techls.org` または `www.techls.org` を想定。

## リンク

- ええやん.ai!: https://eeyan-ai.techls.org/
- Linktree: https://linktr.ee/techtechtechls
- X: https://x.com/techtechtechls

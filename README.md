# GitHub Pages 個人サイト・スターター

シンプルな個人サイトとして始め、後からブログ記事を増やせるJekyll構成です。ビルド作業や追加ライブラリは不要で、GitHub Pages上で自動的に処理されます。

## 最初に変更する場所

1. `_config.yml`
   - `YOUR-USERNAME`をGitHubのユーザー名に変更
   - `YOUR-NAME`とサイト名・説明文を変更
2. `index.html`
   - `YOUR-NAME`と`［趣味…］`を自分の内容に変更
3. `about.md`と`hobbies.md`
   - 仮文言を自分の内容に変更
4. `_posts/2026-09-22-first-note.md`
   - サンプル記事を編集するか、不要なら削除

## GitHub Pagesで公開する

### ユーザーサイトにする場合（最も簡単）

1. GitHubで `YOUR-USERNAME.github.io` というPublicリポジトリを作る
2. このフォルダの中身を、リポジトリ直下へアップロードする
3. リポジトリの **Settings → Pages** を開く
4. **Build and deployment** のSourceで **Deploy from a branch** を選択
5. Branchを **main**、フォルダを **/(root)** にして保存
6. 数分後に `https://YOUR-USERNAME.github.io/` を確認

### 通常のリポジトリ名を使う場合

例えばリポジトリ名が `my-site` なら、`_config.yml`を次のように変更します。

```yml
url: "https://YOUR-USERNAME.github.io"
baseurl: "/my-site"
```

公開URLは `https://YOUR-USERNAME.github.io/my-site/` になります。

## 記事を追加する

`_posts`フォルダに、`YYYY-MM-DD-title.md`という名前のファイルを追加します。

```markdown
---
layout: post
title: "記事のタイトル"
---

ここに本文を書きます。
```

GitHubへ反映すると、トップページと「記録」ページの一覧に自動で追加されます。

## 色を変更する

`assets/css/style.css`冒頭の変数を編集します。

```css
:root {
  --bg: #f6f3ed;
  --text: #252824;
  --accent: #496957;
}
```

## 公開前チェック

- 仮表記（`YOUR-...`、`［...］`）を検索して置き換えたか
- 本名、所属、メールアドレスを公開して問題ないか
- 写真に位置情報や他人の顔が含まれていないか
- スマートフォンで読みにくくないか


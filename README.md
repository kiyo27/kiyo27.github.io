# kiyo27 blog

![example branch parameter](https://github.com/kiyo27/kiyo27.github.io/actions/workflows/gh-pages.yaml/badge.svg)

| key | value |
| --- | -- |
| site generator | https://gohugo.io/ |
| theme | https://github.com/alex-shpak/hugo-book |

## セットアップ

プロジェクトをクローン

```
git clone git@github.com:kiyo27/kiyo27.github.io.git
```

サブモジュールをセットアップ

```
$ git submodule init
$ git submodule update
```

新しい記事を作成(vscode で開く)

```
hugo new posts/first-post.md --editor="code"
```

開発サーバ起動

```
hugo server
```

ドラフトも表示

```
hugo server -D
```

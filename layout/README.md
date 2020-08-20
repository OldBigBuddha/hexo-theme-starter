# layout

Hexo が各ページを生成するためにテンプレートとするファイル群です。

各テンプレート内で使われている変数（`config`, `theme`, `page` など）は Hexo によって提供されているものです。各ファイルの先頭にテンプレート内で使用している変数のドキュメントリンクを張っています。テンプレート内で使えるすべての変数は [Variables | Hexo](https://hexo.io/docs/variables) でご確認ください。

また、一部のプラグインによって生成されるページについてはプラグインが提供している変数を利用している場合もあります。また、ここで列挙しているテンプレートを利用するプラグインは Hexo のテンプレートに使われているものなので、別途追加する必要はありません。

## `index.pug`

Link: [./index.pug](./index.pug)

Dependencies:

- [hexojs/hexo-generator-index](https://github.com/hexojs/hexo-generator-index)
- [hexojs/hexo-pagination](https://github.com/hexojs/hexo-pagination)

`hexo-generator-index` で生成される index ページの生成に使われるテンプレートです。

## `post.pug`

Link: [./post.pug](./post.pug)

Dependencies: なし

プロジェクトルートの `source/_posts` に配置されている Markdown ファイルを HTML へ変換する際に使われるテンプレートです。

## `tag.pug`

Link: [./tag.pug](./tag.pug)

Dependencies:

- [hexojs/hexo-generator-tag](https://github.com/hexojs/hexo-generator-tag)
- [hexojs/hexo-pagination](https://github.com/hexojs/hexo-pagination)

`hexo-generator-tag` で生成されるタグの詳細ページに使われるテンプレートです。

## `archive.pug`

Link: [./archive.pug](./archive.pug)

Dependencies:

- [hexojs/hexo-generator-archive](https://github.com/hexojs/hexo-generator-archive)
- [hexojs/hexo-pagination](https://github.com/hexojs/hexo-pagination)

`hexo-generator-archive` で生成されるアーカイブページに使われるテンプレートです。

## `category.pug`

Link: [./category.pug](./category.pug)

Dependencies:

- [hexojs/hexo-generator-category](https://github.com/hexojs/hexo-generator-category)
- [hexojs/hexo-pagination](https://github.com/hexojs/hexo-pagination)

`hexo-generator-archive` で生成されるアーカイブページに使われるテンプレートです。

## `hexo-pagination` について

テンプレートにはほぼすべてに [`hexojs/hexo-pagination`](https://github.com/hexojs/hexo-pagination) が利用されています。このプラグインは名前の通り大量のデータをページング処理するために利用されます。

`hexo-pagination` が使われるレイアウトで利用している `page` 変数は Hexo のドキュメントにあるグローバル変数としての `page` とは違った値を保有しています。

| 変数名 | 説明 |
| ----- | --- |
| `layout` | レイアウト名（レイアウトテンプレートのファイル名） |
| `date` | 作成日時 |
| `path` | このページへの URL |
| `base` | ベース URL |
| `total` | 合計ページ数 |
| `current` | 現在のベージ番号 |
| `current_url` | 現在ページへのパス（`path` と同様） |
| `posts` | 現在のページで表示する [記事のデータ](https://hexo.io/docs/variables#Page-Variables) |
| `prev` | 前ページの番号 |
| `prev_link` | 前ページへの URL |
| `next` | 次ページの番号 |
| `next_link` | 次ページへの URL |

詳しくはリポジトリにある [README.md](https://github.com/hexojs/hexo-pagination/blob/master/README.md) を確認してください。

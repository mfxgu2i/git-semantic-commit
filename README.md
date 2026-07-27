# git-semantic-commit

コーディングエージェント向けのスキル。変更を意味のある単位に分けて、規定のフォーマットでコミットする。

[Semantic Commit Messages](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716) をもとに、日本語のコミットメッセージ向けに調整しています。

## フォーマット

```
<type>: <subject>
<issue-id>
```

| type | 対象 |
| --- | --- |
| `feat` | ユーザー向けの新機能や更新・改修 |
| `fix` | ユーザー向けのバグ修正 |
| `docs` | 開発に関するドキュメントの追加・変更 |
| `refactor` | コードのリファクタリング（機能の変更なし） |
| `test` | テストの追加・修正（プロダクションコードの変更なし） |
| `chore` | ビルドツールやタスクランナーの設定変更 |

`<issue-id>` は任意です。書く場合は、1行目の直後に空行を1つ入れます。

```
fix: 問い合わせフォームの必須チェックが効かない不具合を修正する

PROJECT_KEY-01
```

## 方針

### 粒度から扱う

書式だけを直しても、コミットは読めるようになりません。1コミット = 1つの意図になるよう、変更を分けるところから指示します。

### コミットで止まる

`push` は必ず事前確認を取ります。履歴を書き換える操作（`--amend` / `rebase` / `reset --hard`）は、名指しの指示があるときだけ実行します。

## インストール

```
npx skills add mfxgu2i/git-semantic-commit
```

## 参考

- [Semantic Commit Messages](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716)

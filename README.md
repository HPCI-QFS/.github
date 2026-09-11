# .github

HPCI-QFS Organization の**プロフィールページ**と、**組織共通の community health files** を置く特殊リポジトリ。
通常のコードは含まない。

## 構成

```
profile/README.md    ← https://github.com/HPCI-QFS に表示される内容（このパスのみ。変更不可・フォールバックなし）
CODE_OF_CONDUCT.md   ← 以下は任意。org 内の各リポジトリが自前で持たない場合の既定値になる
CONTRIBUTING.md
SECURITY.md
SUPPORT.md
.github/ISSUE_TEMPLATE/
.github/PULL_REQUEST_TEMPLATE.md
```

## 注意

- **このリポジトリは public でなければならない。** private にすると org ページへの表示が止まる
- 既定値として継承されるのは root / `.github/` / `docs/` に置いたファイルのみ
- **CODEOWNERS と GitHub Actions のワークフローは org 全体に継承されない。** 各リポジトリに置く
- Issue テンプレートは all-or-nothing。各リポジトリが自前の `.github/ISSUE_TEMPLATE` を持つと、既定側は一切使われない
- LICENSE も継承されない
- 変更は default branch に commit した時点で反映される。デプロイ手順は不要
- public なので、**機微な情報（分担機関の詳細、未公表の数値、NDA 由来の内容）は置かない**
- メンバー限定の表示内容が必要になったら、別途 `.github-private` リポジトリ（private）の `profile/README.md` に置く

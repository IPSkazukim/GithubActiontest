# GithubActionTest

githubのactionの動作検証用

## ドキュメント自動生成

このリポジトリは、GitHub Actionsを使用してソースコードから自動的にドキュメントを生成します。

### 機能

- Pythonソースコードのdocstringから自動的にHTMLドキュメントを生成
- GitHub Pagesにドキュメントを自動デプロイ
- mainまたはmasterブランチへのpush時に自動実行
- Mermaid図のサポート

### ドキュメント生成の仕組み

1. **ソースコード**: `src/` ディレクトリにPythonファイルとdocstringが含まれています
2. **GitHub Actions**: `.github/workflows/generate-docs.yml` がドキュメント生成を自動化します
3. **MkDocs**: Pythonのdocstringから美しいHTMLドキュメントを生成します
4. **GitHub Pages**: 生成されたドキュメントは `gh-pages` ブランチにデプロイされます

### ドキュメントの閲覧

ドキュメントは以下のURLで閲覧できます（GitHub Pagesを有効にした後）:
```
https://IPSkazukim.github.io/GithubActionTest/
```

### ローカルでのドキュメント生成

```bash
# 依存関係のインストール
pip install -r requirements.txt

# ドキュメントの生成
mkdocs build

# ローカルサーバーで確認
mkdocs serve
```

### プロジェクト構造

```
.
├── .github/
│   └── workflows/
│       └── generate-docs.yml  # ドキュメント生成のワークフロー
├── docs/                       # MkDocsドキュメントソース
│   ├── index.md
│   └── api/
├── src/                        # Pythonソースコード
│   ├── __init__.py
│   ├── calculator.py          # 計算機クラス
│   ├── euclidean.py           # ユークリッドの互除法
│   └── utils.py               # ユーティリティ関数
├── mkdocs.yml                  # MkDocs設定ファイル
├── requirements.txt            # Python依存関係
└── README.md                   # このファイル
```

## APIドキュメント

各モジュールの詳細なAPIドキュメントは、左側のナビゲーションメニューからアクセスできます。

- [Calculator](api/calculator.md) - 基本的な計算機能
- [Utils](api/utils.md) - ユーティリティ関数
- [Euclidean](api/euclidean.md) - ユークリッドの互除法

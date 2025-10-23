# GitHub設定リポジトリ

このリポジトリは、業務効率化やデータ活用を目的としたコード管理を円滑にするための **GitHub標準設定** をまとめています。

## 📂 構成
.github/
    ├── ISSUE_TEMPLATE/           # Issueテンプレート
    │   ├── bug_report.md         # バグ報告用
    │   └── feature_request.md    # 改善要望用
    ├── workflows/                # GitHub Actionsワークフロー
    │   └── ci.yml                # CI（テスト・Lint・品質チェック）
    ├── dependabot.yml            # 依存関係の脆弱性検知と自動更新
    ├── PULL_REQUEST_TEMPLATE.md  # PRテンプレート
    └── README.md                 # この説明ファイル


## ✅ 目的
- コードレビューを効率化
- 脆弱性検知と自動更新（Dependabot）
- CI/CDによる品質担保
- Issue/PRテンプレートで情報整理

## 🔍 主な機能
- **Dependabot**  
  - Python（pip）とGitHub Actionsの脆弱性検知・自動修正PR
- **CIワークフロー**  
  - Pythonテスト（pytest）
  - Linter（ruffやflake8）
  - SQLLint（sqlfluff）※必要に応じて追加
- **テンプレート**  
  - バグ報告・改善要望のIssueテンプレート
  - 汎用的なPRテンプレート

## 🛠 運用ルール
- **PR作成時**: PULL_REQUEST_TEMPLATE.mdを利用
- **Issue登録時**: 適切なテンプレートを選択
- **依存関係更新**: DependabotのPRを確認し、CIが通過したらマージ
- **CI結果確認**: 全テスト・Lintが成功していることを確認

## 📌 注意事項
- 機密情報や個人情報は含めない
- SQLやPythonコードはセキュリティベストプラクティスを遵守
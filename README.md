# GitHub Actions カスタムアクション チュートリアル

このリポジトリは [GitHub Actions でカスタムアクションを作ろう](https://zenn.dev/farstep/books/learn-github-actions/viewer/create-custom-actions) のチュートリアルを実践するためのサンプルリポジトリです。

## 📚 チュートリアル内容

### 1. Docker Action の作成
- Dockerコンテナベースのカスタムアクション
- `action.yml` の設定
- 入力・出力パラメータの定義

### 2. JavaScript Action の作成
- Node.jsベースのカスタムアクション
- `@actions/core` パッケージの使用
- 軽量で高速な実行

### 3. Composite Action の作成
- 既存のアクションを組み合わせたアクション
- シェルスクリプトとの連携
- ワークフローの再利用

## 🚀 使用方法

### Docker Action
```yaml
- uses: ./
  with:
    name: 'World'
```

### JavaScript Action
```yaml
- uses: ./javascript-action
  with:
    name: 'World'
```

### Composite Action
```yaml
- uses: ./composite-action
  with:
    name: 'World'
```

## 📁 ディレクトリ構成

```
.
├── README.md
├── action.yml              # Docker Action設定
├── Dockerfile             # Docker Action用
├── entrypoint.sh          # Docker Action用スクリプト
├── javascript-action/     # JavaScript Action
│   ├── action.yml
│   ├── index.js
│   └── package.json
└── composite-action/      # Composite Action
    └── action.yml
```

## 🔧 開発環境

- Docker
- Node.js (v16以上)
- GitHub CLI (推奨)

## 📖 参考資料

- [GitHub Actions でカスタムアクションを作ろう](https://zenn.dev/farstep/books/learn-github-actions/viewer/create-custom-actions)
- [GitHub Actions公式ドキュメント](https://docs.github.com/en/actions)
- [カスタムアクション作成ガイド](https://docs.github.com/en/actions/creating-actions)

## 🎯 学習目標

1. カスタムアクションの3つのタイプを理解する
2. 適切なアクションタイプを選択できるようになる
3. 再利用可能なワークフローを作成できるようになる
4. GitHub Marketplaceでのアクション公開方法を学ぶ

---

**注意**: このリポジトリはチュートリアル用のサンプルコードです。本番環境での使用は想定していません。

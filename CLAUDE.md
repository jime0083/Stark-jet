# Stark Jet - Project Rules

## Project Overview
コーヒーショップ「Stark Jet」の公式Webサイト

## Tech Stack
- **Framework**: React (SPA - Single Page Application)
- **Styling**: CSS (vanilla)
- **Hosting**: GitHub Pages

## Architecture Rules

### React SPA
- シングルページアプリケーション形式で構築
- React 18を使用
- クライアントサイドルーティング（必要に応じてReact Router）
- コンポーネントベースの設計

### GitHub Pages Deployment
- `gh-pages`ブランチにデプロイ
- ビルド成果物は`/docs`または`/build`ディレクトリに出力
- 相対パスを使用（`homepage`設定に注意）
- SPAのため、404.htmlによるリダイレクト対応が必要

## File Structure
```
/Stark jet
├── index.html      # エントリーポイント
├── styles.css      # グローバルスタイル
├── app.jsx         # メインReactアプリケーション
├── images/         # 画像アセット
└── CLAUDE.md       # プロジェクトルール
```

## Deployment Commands
```bash
# GitHub Pagesへのデプロイ（手動）
git add .
git commit -m "Update site"
git push origin master

# gh-pagesブランチを使用する場合
# npm run deploy（package.json設定後）
```

## Design Specifications
- カラースキーム: ダーク（#0e0d0c）+ クリーム（#f0ece4）
- レイアウト: 左右50/50分割、フルスクリーンセクション
- スクロール: scroll-snapによるセクションスナップ
- インタラクション: クリックで詳細展開

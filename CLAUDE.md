# Stark Jet - Project Rules

## Project Overview
コーヒーショップ「Stark Jet」の公式Webサイト

## Live URL
https://jime0083.github.io/Stark-jet/

## ⚠️ 参考サイト準拠ルール（最重要・厳守）

### 参考サイト
- **メインページ**: https://www.thomasmonavon.com/
- **詳細ページ**: https://www.thomasmonavon.com/gregory-lalle

### 厳守事項

⛔ **以下の要素は参考サイトと完全に同じにすること。独自の実装や逸脱は禁止。**

| 要素 | ルール |
|------|--------|
| 画面遷移アニメーション | 参考サイトと同一のタイミング・イージング・動作 |
| 文字のフォント | 参考サイトと同一（またはできる限り近いもの） |
| 文字の表示アニメーション | 参考サイトと同一（左下から広がる等） |
| スクロール挙動 | 参考サイトと同一の速度・イージング |
| カーソル表示 | 参考サイトと同一（Open/Close表示） |
| 詳細ビュー遷移 | 参考サイトと同一のアニメーション |

### 作業前の確認事項

1. **参考サイトの該当部分を必ず確認してから実装する**
2. **独自のアニメーションや挙動を追加しない**
3. **「これでいいだろう」という推測で実装しない**
4. **不明な場合はユーザーに確認する**

### 進捗管理ファイル
- **problem.txt**: 問題一覧
- **progress.txt**: タスク進捗管理

## ⚠️ 修正ループルール（厳守）

### 修正フロー

```
修正 → チェック → (問題あり) → 修正 → チェック → ... → (問題なし) → ユーザー確認待ち
```

### 各フェーズの説明

1. **修正フェーズ**
   - 参考サイトを分析
   - コードを実装
   - デプロイ

2. **チェックフェーズ**
   - 問題点が解決できているか確認
   - 参考サイトと同様の実装ができているか確認
   - 問題があれば修正フェーズに戻る

3. **ユーザー確認フェーズ**
   - 修正ループをパスした後、ユーザーに確認を依頼
   - ユーザーが問題なしと確認して初めて「解決」とする

### 厳守事項

⛔ **以下は絶対禁止**

| 禁止事項 | 理由 |
|----------|------|
| ユーザー確認なしに次のタスクに進む | タスク完了はユーザーが判断する |
| チェックフェーズを省略する | 品質を担保するため必須 |
| 「おそらく大丈夫」で完了とする | 必ず確認すること |

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

## Brand Assets

### Official Logo
- **ファイル**: `images/ロゴ.png`
- **用途**: ファビコン、ヘッダーロゴ、OGP画像、その他ブランディング全般
- **重要**: サイトのロゴが必要な場合は必ずこの画像を使用すること

## Design Specifications
- カラースキーム: ダーク（#0e0d0c）+ クリーム（#f0ece4）
- レイアウト: 左右50/50分割、フルスクリーンセクション
- スクロール: scroll-snapによるセクションスナップ
- インタラクション: クリックで詳細展開

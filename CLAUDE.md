# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

タスクの追加・完了・削除ができるシンプルなタスクボードアプリ。タスクは localStorage に永続化される。

**Tech Stack**

| 区分 | 技術 |
|---|---|
| UI フレームワーク | React 19 |
| ビルドツール | Vite 8 |
| スタイリング | CSS (CSS Variables) |
| 状態管理 | React useState / useEffect |
| データ永続化 | localStorage |
| CI/CD | GitHub Actions |

## Naming Conventions

- **コンポーネントファイル**: PascalCase（例: `TaskItem.jsx`）
- **コンポーネント関数**: PascalCase の named export（例: `export default function App()`）
- **CSS クラス名**: kebab-case（例: `.task-item`, `.delete-btn`）
- **localStorage キー**: `taskboard-` プレフィックス（例: `taskboard-tasks`）
- **イベントハンドラ**: `handle` プレフィックス（例: `handleKeyDown`）、または動詞のみ（例: `addTask`, `toggleTask`）

## デプロイ先

https://tkywork.github.io/taskboard-app/

`main` ブランチへの push で GitHub Actions が自動ビルド・デプロイする。  
Vite の `base` は `/taskboard-app/` に設定済み（[vite.config.js](vite.config.js)）。

## Git Operations

**コードを変更するたびに GitHub にプッシュする。**

- 機能追加・修正・リファクタリング問わず、変更のたびにコミット＆プッシュする。
- コミットメッセージは日本語または英語で簡潔に記述する。
- 無関係な変更を1コミットにまとめない。

```bash
git add <変更ファイル>
git commit -m "変更内容を簡潔に説明するメッセージ"
git push
```

## Development Commands

```bash
# 依存パッケージのインストール
npm install

# 開発サーバー起動
npm run dev

# ビルド
npm run build

# Lint
npm run lint
```

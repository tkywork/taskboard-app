# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a taskboard application. Update this section with the tech stack and architecture details as the project evolves.

## Git Operations

**Push to GitHub after every code change.**

- After every meaningful code change (feature, fix, refactor), commit and push to GitHub immediately.
- Use clear, descriptive commit messages in Japanese or English consistent with the project convention.
- Never accumulate multiple unrelated changes in a single commit.

```bash
git add <changed files>
git commit -m "変更内容を簡潔に説明するメッセージ"
git push
```

Initialize and connect to GitHub if not yet done:

```bash
git init
git remote add origin https://github.com/<owner>/taskboard-app.git
git branch -M main
git push -u origin main
```

## Development Commands

Update this section once the tech stack is decided. Common patterns:

```bash
# Install dependencies
npm install       # Node.js / React / Vue etc.
pip install -r requirements.txt  # Python

# Start dev server
npm run dev

# Run tests
npm test
npm run test -- --testPathPattern=<file>  # single test file

# Build
npm run build

# Lint
npm run lint
```

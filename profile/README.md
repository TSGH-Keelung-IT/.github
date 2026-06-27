# 三軍總醫院基隆分院資訊組

本 GitHub Organization 用於資訊組內部小型開發團隊的版本控制、AI 協作開發、文件管理與程式碼審查。

## 開發核心原則

- 使用 GitHub 進行版本控制
- 使用 Branch 進行功能開發
- 使用 Pull Request 進行審查
- `main` 為正式穩定版本
- AI 工具僅作為開發助手，不得自行合併正式分支
- 嚴禁提交密碼、Token、正式資料、病患資料或個資

## Branch 命名規範

| Branch 類型 | 用途 | 範例 |
|---|---|---|
| `feature/` | 新功能開發 | `feature/QueueReport` |
| `bugfix/` | 一般錯誤修正 | `bugfix/LoginTimeout` |
| `hotfix/` | 正式環境緊急修正 | `hotfix/QueueCrash` |
| `refactor/` | 程式重構 | `refactor/DataAccess` |
| `docs/` | 文件更新 | `docs/README` |
| `db/` | 資料庫變更 | `db/UpdateQueueSP` |
| `config/` | 設定與環境調整 | `config/IIS` |

## AI 開發守則

所有 Codex、ChatGPT、Genspark、Copilot 等 AI 產出的修改，必須：

1. 建立獨立 Branch
2. 只修改本次任務相關檔案
3. 使用清楚的 Commit Message
4. 建立 Pull Request
5. 等待人工 Review
6. 禁止自行 Merge

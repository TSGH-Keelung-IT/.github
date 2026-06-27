# 資訊組 GitHub 協作規範

本文件為 Organization 預設協作規範。若個別專案有自己的 `CONTRIBUTING.md`，以專案內規範為準。

## 1. 開發流程

所有程式修改均應透過 Branch 與 Pull Request。

```text
工作 Branch
↓
Commit
↓
Push
↓
Pull Request
↓
Code Review
↓
Merge
```

## 2. 分支規則

正式穩定版：`main`

整合測試版：`develop`

日常開發分支：

```text
feature/
bugfix/
refactor/
docs/
db/
config/
```

正式環境緊急修正：`hotfix/`

## 3. Branch 命名

允許類型：

```text
feature/功能名稱
bugfix/問題名稱
hotfix/緊急問題名稱
refactor/重構範圍
docs/文件名稱
db/資料庫變更名稱
config/設定名稱
```

範例：

```text
feature/FHIR-Observation
bugfix/LoginTimeout
hotfix/QueueCrash
refactor/DataAccess
docs/README
db/UpdateQueueSP
config/IIS
```

## 4. Commit Message

採用 Conventional Commits：

```text
<type>: <繁體中文描述>
```

可用 type：`feat`, `fix`, `refactor`, `docs`, `db`, `config`, `test`, `chore`

範例：

```text
feat: 新增 Queue 報表功能
fix: 修正登入逾時問題
db: 修改 Queue_GetWaiting SP
config: 調整 NLog 設定
```

## 5. Pull Request 規範

PR 必須說明：

- 修改內容
- 修改原因
- 影響範圍
- 測試方式
- 是否有資料庫異動
- 是否有設定檔異動
- 是否需要部署注意事項

## 6. AI 協作規則

使用 Codex、ChatGPT、Genspark、Copilot 等工具時，請要求 AI：

```text
不可直接修改 main。
不可直接修改 develop。
請建立新的 Branch。
請只修改本次任務需要的檔案。
請使用 Conventional Commits。
完成後請建立 Pull Request。
請不要自行 Merge，等待人工審核。
```

## 7. 禁止事項

不得提交：密碼、Token、API Key、正式 ConnectionString、病患資料、身分證、正式資料庫備份、`bin/`、`obj/`、`publish/`、`appsettings.Production.json`。

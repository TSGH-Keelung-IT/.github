# GitHub Organization 治理規範

## 角色

### Owner

負責 Organization 設定、Repository 建立、權限管理、Branch Protection Rules、GitHub App / Codex 授權與安全事件處理。

### Reviewer

負責 Pull Request 審查、Code Review、資安與資料庫異動確認、合併建議。

### Developer

負責建立 Branch、開發功能、建立 Pull Request、回應 Review，且不直接修改 main。

### AI Assistant

定位為協助撰寫程式、重構、測試與文件，不具備最終決策權，不可自行 Merge。

## 必要規範

所有正式專案均應具備：

- `README.md`
- `CONTRIBUTING.md`
- `SECURITY.md`
- `.gitignore`
- `.github/PULL_REQUEST_TEMPLATE.md`
- `.github/CODEOWNERS`

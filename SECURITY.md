# 資安與資料保護規範

本文件為 Organization 預設資安規範。若個別專案有自己的 `SECURITY.md`，以專案內規範為準。

## 1. 嚴禁提交內容

任何 Repository 均不得提交：

- 病患資料
- 病歷資料
- 醫囑資料
- 檢查報告
- 身分證字號
- 員工個資
- 正式環境資料
- 資料庫備份
- ConnectionString
- 帳號密碼
- API Key
- Token
- 憑證檔
- VPN 設定
- 防火牆設定匯出檔
- AD 帳號清單
- 機敏網路架構資訊

## 2. 禁止提交檔案

```text
appsettings.Production.json
.env
*.bak
*.mdf
*.ldf
*.pfx
*.cer
*.key
*.pem
*.zip
*.7z
*.rar
bin/
obj/
publish/
.vs/
```

## 3. AI 使用限制

使用 AI 工具時，不得提供真實病患資料、正式資料庫內容、正式帳號密碼、內部憑證、完整敏感 Log 或機敏網路設定。

應改用假資料、去識別化資料、結構描述、錯誤摘要、截斷後 Log。

## 4. 發現敏感資料外洩

若敏感資料已被提交：

1. 立即通知 Repository 管理者
2. 移除敏感資料
3. 停用或更換已外洩的 Key / Token / Password
4. 檢查 Git History
5. 必要時重寫 Git History
6. 檢討 `.gitignore`、PR Review 與 AI 開發流程

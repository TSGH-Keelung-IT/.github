# TSGH-Keelung-IT Organization Defaults

本 Repository 名稱應為：

```text
.github
```

用途：作為 `TSGH-Keelung-IT` GitHub Organization 的共用文件與預設模板。

GitHub 會在各專案 Repository 沒有自行提供對應檔案時，套用本 Repository 的預設 Community Health Files，例如：

- `CONTRIBUTING.md`
- `SECURITY.md`
- `SUPPORT.md`
- Pull Request Template
- Issue Templates

> 注意：依 GitHub 官方說明，Organization 預設 Community Health Files 多數情境需要 `.github` Repository 為 Public 才能套用至整個 Organization。

---

## 建議建立方式

```bash
gh repo create TSGH-Keelung-IT/.github --public --description "Default community health files and templates for TSGH-Keelung-IT"
```

接著將本資料夾內容推送進去。

---

## 使用方式

此 Repository 適合放「Organization 共用預設規範」。

若各專案有自己的特殊需求，可在該專案內放置自己的：

```text
CONTRIBUTING.md
SECURITY.md
.github/PULL_REQUEST_TEMPLATE.md
.github/ISSUE_TEMPLATE/
```

專案內檔案會優先於 Organization 的 `.github` 預設檔案。

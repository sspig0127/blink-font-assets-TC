# Copilot Instructions

## Repo Overview

簡短：管理 Sarasa Mono TC 字型資產與 Blink 用 CSS（字型檔 + CSS 配置），供開發者或終端環境引用。按需讀取路徑：

- fonts/ — 字型檔、fonts/README.md
- blink/ — Blink CSS（sarasa-mono-tc*.css）
- README.md — 使用範例與整體說明

## Language Convention

- **All documentation**: 臺灣繁體中文（Traditional Chinese, Taiwan）
- English abbreviations must be followed by `（中文譯名，完整英文名稱）`
- **Code and shell commands**: English is fine; surrounding explanations must be in Traditional Chinese

## Git Conventions

- Protocol: **SSH**
- `user.name`: `Alexander Lin` / `user.email`: `sspig0127+github@gmail.com`
- **Never auto-commit or auto-push** — only commit/push when explicitly asked
- **程式碼**：可用英文；說明、註解使用繁體中文
- **CI 檢查**：PR 觸發 Gitleaks（機密偵測）+ Trivy（弱點掃描）+ pytest

## Line Endings

`.gitattributes` enforces `eol=lf` for all text files. If a shell script shows `\r: command not found` on WSL, fix with:

```bash
sed -i 's/\r//' <script.sh>
```

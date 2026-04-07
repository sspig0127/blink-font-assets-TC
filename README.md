# blink-font-assets-TC

公開提供給 [Blink Shell](https://blink.sh/)（iOS 終端機 App）使用的 [Sarasa Mono TC](https://github.com/be5invis/Sarasa-Gothic) / [Sarasa Gothic Mono TC Emoji Nerd](https://github.com/sspig0127/SarasaMonoTC-Emoji/releases) 字型資產 repo。

> **解決的問題：** Blink Shell 預設不含繁體中文等寬字型，透過此 repo 的 CSS `@font-face` 設定，讓 Blink Shell 能正確顯示中文字符。

## 預期結構

```text
blink-font-assets-TC/
├── blink/
│   ├── sarasa-mono-tc-blink.css                     # 基本 Sarasa Mono TC (Regular/Bold)
│   └── sarasa-mono-tc-Lite-Nerd-blink.css           # Lite + Nerd (emoji) 版本 CSS（示例）
└── fonts/
    ├── SarasaMonoTC-Regular.ttf
    ├── SarasaMonoTC-Bold.ttf
    ├── SarasaMonoTCEmojiLiteNerd-Regular.ttf       # Lite + Nerd (emoji) 版本
    └── SarasaMonoTCEmojiLiteNerd-Bold.ttf
```

## 直接可用的 raw URL

| 資源               | 說明                                                      | URL                                                                                                                   |
| ------------------ | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| CSS (Lite Nerd)    | Blink 匯入用的 `@font-face` 設定（Emoji + Nerd glyphs） | `https://raw.githubusercontent.com/sspig0127/blink-font-assets-TC/main/blink/sarasa-mono-tc-Lite-Nerd-blink.css`    |
| Emoji/Nerd Regular | Lite + Nerd (emoji) 版本 ttf                              | `https://raw.githubusercontent.com/sspig0127/blink-font-assets-TC/main/fonts/SarasaMonoTCEmojiLiteNerd-Regular.ttf` |
| Emoji/Nerd Bold    | Lite + Nerd (emoji) 版本 ttf                              | `https://raw.githubusercontent.com/sspig0127/blink-font-assets-TC/main/fonts/SarasaMonoTCEmojiLiteNerd-Bold.ttf`    |
| CSS (Regular)      | Blink 匯入用的 `@font-face` 設定（基本 Sarasa Mono TC） | `https://raw.githubusercontent.com/sspig0127/blink-font-assets-TC/main/blink/sarasa-mono-tc-blink.css`              |
| Regular            | 一般字重 ttf                                              | `https://raw.githubusercontent.com/sspig0127/blink-font-assets-TC/main/fonts/SarasaMonoTC-Regular.ttf`              |
| Bold               | 粗體字重 ttf                                              | `https://raw.githubusercontent.com/sspig0127/blink-font-assets-TC/main/fonts/SarasaMonoTC-Bold.ttf`                 |

## 快速設定步驟

### 1. 放入字型檔

把你信任來源的字型檔放進 `fonts/`：

**SarasaMonoTC:**

- `fonts/SarasaMonoTC-Regular.ttf`
- `fonts/SarasaMonoTC-Bold.ttf`

> 原始字型也可從 [Sarasa Gothic Releases](https://github.com/be5invis/Sarasa-Gothic/releases) 下載。

**SarasaMonoTC Emoji + Nerd 變體字 **

- `fonts/SarasaMonoTCEmojiLiteNerd-Regular.ttf`
- `fonts/SarasaMonoTCEmojiLiteNerd-Bold.ttf`

> 原始字型也可從我製作的變體字 [Sarasa Gothic Mono TC Emoji Releases](https://github.com/sspig0127/SarasaMonoTC-Emoji/releases) 下載。

### 2. 推送至 GitHub

```bash
git add .
git commit -m "Add Sarasa Mono TC font assets for Blink"
git push origin main
```

### 3. 在 Blink Shell 匯入字型

1. 開啟 Blink Shell → `config`
2. `Appearance`
3. `New Font`
4. 貼上 CSS raw URL
5. 點 `Import`（會直接開始下載／匯入）
6. 點 `Save`

## ⚠️ 注意事項

- 📌 **必要條件：** 這個 repo 需要保持 **public**，Blink 才能直接抓 raw URL
- ⚠️ **暫時限制：** 在字型檔尚未放入前，CSS raw URL 雖然存在，但字型 URL 會是 404
- 📦 **授權提醒：** 若要公開散佈字型檔，請一併放入上游字型授權檔案（Sarasa Gothic 採 [SIL OFL 1.1](https://scripts.sil.org/OFL)）

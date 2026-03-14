# blink-font-assets-TC

公開提供給 `Blink Shell` 使用的 `Sarasa Mono TC` 字型資產 repo。

## 預期結構

```text
blink-font-assets-TC/
├── blink/
│   └── sarasa-mono-tc-blink.css
└── fonts/
    ├── SarasaMonoTC-Regular.ttf
    └── SarasaMonoTC-Bold.ttf
```

## 直接可用的 raw URL

- CSS:
  `https://raw.githubusercontent.com/sspig0127/blink-font-assets-TC/main/blink/sarasa-mono-tc-blink.css`
- Regular:
  `https://raw.githubusercontent.com/sspig0127/blink-font-assets-TC/main/fonts/SarasaMonoTC-Regular.ttf`
- Bold:
  `https://raw.githubusercontent.com/sspig0127/blink-font-assets-TC/main/fonts/SarasaMonoTC-Bold.ttf`

## 你現在只差這一步

把你信任來源的字型檔放進 `fonts/`：

- `fonts/SarasaMonoTC-Regular.ttf`
- `fonts/SarasaMonoTC-Bold.ttf`

之後執行：

```bash
git add .
git commit -m "Add Sarasa Mono TC font assets for Blink"
git push origin main
```

然後在 Blink Shell 內：

```text
config
  → Appearance
  → New Font
  → 貼上 CSS raw URL
  → Download
  → Save
```

## 注意

- 這個 repo 需要保持 **public**，Blink 才能直接抓 raw URL
- 若你要公開散佈字型檔，請一併放入上游字型授權檔案
- 在字型檔尚未放入前，CSS raw URL 雖然存在，但字型 URL 會是 404

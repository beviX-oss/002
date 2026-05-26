# 栖 Atelier · 寵物身心養護所

高級暗色襯線風格的單頁式 Landing Page。

## 檔案結構

```
src/
├── index.html          ← 頁面結構與內容（HTML）
├── css/
│   └── styles.css      ← 所有樣式（變數、版面、元件）
└── js/
    └── image-slot.js   ← <image-slot> Web Component
                          （可拖放圖片框；自動保存）
```

## 設計系統（CSS 變數，定義於 `:root`）

| 用途         | 變數          | 色碼      |
|--------------|---------------|-----------|
| 主背景       | `--bg`      | #14110E   |
| 卡層背景     | `--bg-2`    | #1A1612   |
| 分隔線       | `--line`    | #2A241D   |
| 主要前景文字 | `--fg`      | #EDE6D6   |
| 次要文字     | `--fg-dim`  | #A89C86   |
| 金色點綴     | `--gold`    | #B89968   |

## 字體

從 Google Fonts 載入：
- **Noto Serif TC** — 中文標題
- **Cormorant Garamond** — 西文/斜體裝飾
- **Noto Sans TC** — 內文

## 章節（依出現順序）

1. `header.nav`        — 導覽列
2. `section.hero`      — 主視覺
3. `.strip`            — 服務跑馬燈
4. `#services`         — 服務四宮格
5. `#philosophy`       — 品牌理念（含環境照）
6. `#process`          — 預約三步驟
7. `#team`             — 駐院團隊
8. `section.s .testi`  — 客戶見證
9. `#booking`          — CTA
10. `footer`           — 頁尾

## 圖片替換（<image-slot>）

頁面上有 6 個 `<image-slot>`：
- `#hero-a`、`#hero-b`            ← Hero
- `#philosophy`                     ← 品牌理念
- `#doc-chen`、`#doc-lin`、`#doc-su` ← 駐院團隊

把照片拖入即可，也可點擊上傳。雙擊框內進入裁切模式。

## 本地開發

任意靜態伺服器即可，例如：

```bash
npx serve src
# 或
python3 -m http.server -d src 5173
```

> 直接以 `file://` 開啟也可，但 `<image-slot>` 的 sidecar 持久化需要 HTTP 環境。

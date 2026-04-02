# F-RHA Marketplace

> 為 [f-rha](https://github.com/dio_dio/f-rha) React 元件庫打造的 Claude Code Plugin Marketplace

在 Claude Code 中使用 f-rha 時，自動獲得元件 Props 說明、用法範例、以及最佳實踐建議。

---

## 架構

```
F-RHA-marketplace/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace 目錄設定
├── README.md
└── plugins/
    └── F-RHA/
        ├── .claude-plugin/
        │   └── plugin.json       # Plugin manifest
        ├── CHANGELOG.md
        ├── README.md
        └── skills/
            ├── components/
            │   ├── button/
            │   │   ├── .claude-plugin/plugin.json
            │   │   └── skills/button/SKILL.md
            │   ├── dialog/
            │   │   ├── .claude-plugin/plugin.json
            │   │   └── skills/dialog/SKILL.md
            │   ├── input/
            │   │   ├── .claude-plugin/plugin.json
            │   │   └── skills/input/SKILL.md
            │   └── radio/
            │       ├── .claude-plugin/plugin.json
            │       └── skills/radio/SKILL.md
            └── hooks/
                ├── use-debounce/
                │   ├── .claude-plugin/plugin.json
                │   └── skills/use-debounce/SKILL.md
                └── use-local-storage/
                    ├── .claude-plugin/plugin.json
                    └── skills/use-local-storage/SKILL.md
```

每個 skill 都是獨立的 plugin，擁有自己的 `.claude-plugin/plugin.json` manifest 和 `skills/<name>/SKILL.md` 內容。

---

## 包含技能

### UI 元件

| 技能 | 觸發時機 |
|------|---------|
| **Button** | 使用或詢問按鈕元件，包含 variant、size、disabled 等設定 |
| **Dialog** | 使用或詢問 Modal 對話框，包含開關控制、footer、鍵盤關閉 |
| **Input** | 使用或詢問文字輸入框，包含 label、error message、disabled |
| **Radio** | 使用或詢問單選按鈕群組，支援字串陣列與物件陣列格式 |

### Hooks

| 技能 | 觸發時機 |
|------|---------|
| **useDebounce** | 需要對快速變動的值（搜尋輸入、resize）做防抖處理 |
| **useLocalStorage** | 需要將 React state 持久化到 localStorage |

---

## 安裝

```bash
claude plugin install f-rha
```

安裝後，在任何使用 f-rha 的專案中，Claude 會自動套用對應技能。

---

## 使用方式

安裝完成後不需要額外設定。只要在對話中提到 f-rha 的元件或 hook，Claude 即會自動帶入正確的 API 說明與範例。

**範例對話：**

```
你：幫我用 f-rha 做一個確認刪除的 Dialog
```

```
你：useDebounce 要怎麼搭配搜尋輸入框？
```

---

## 作者

**dio_dio** — denny41606@gmail.com

# APCS Python 教材瀏覽器

以 Streamlit 打造的互動式 APCS Python 知識庫瀏覽器，涵蓋 Level 1～5 完整教學內容。

## 功能

- **知識庫探索** — 依級分與知識點瀏覽實作要點、Python 語法與常見陷阱
- **JSON 技術手冊** — 檢視資料結構規格並下載知識庫 JSON 檔案
- **資料驅動** — 所有教學內容以 JSON 格式管理，支援 JSON Schema 驗證
- **遠端載入** — 可透過 GitHub Raw URL 載入外部知識庫資料

## 知識庫內容

| Level | 名稱 | 知識點 |
|-------|------|--------|
| 1 | 程式設計觀念 | 變數與資料型態、運算子與表達式、條件判斷 |
| 2 | 基礎程式設計能力 | 輸入與輸出、迴圈結構、字串處理 |
| 3 | 程式設計實作能力 | 串列操作、函式設計、排序與搜尋、二維陣列 |
| 4 | 基礎資料結構運用 | 遞迴與 DFS、BFS、堆疊與佇列、字典與集合 |
| 5 | 進階資料結構與演算法 | 動態規劃、圖論演算法、貪心演算法、分治法 |

## 快速開始

```bash
# 建立虛擬環境
python3 -m venv venv
source venv/bin/activate

# 安裝依賴
pip install -r requirements.txt

# 驗證知識庫資料
python scripts/validate.py

# 啟動應用程式
streamlit run app.py
```

## 專案結構

```
APCS_Python/
├── .streamlit/config.toml           # Streamlit 主題設定
├── data/
│   ├── schema.json                  # JSON Schema 驗證規格
│   └── knowledge_apcs_python.json   # 核心知識庫資料
├── lib/
│   └── data_loader.py               # 資料讀取模組
├── scripts/
│   └── validate.py                  # Schema 驗證腳本
├── app.py                           # Streamlit 主程式
└── requirements.txt                 # 依賴套件
```

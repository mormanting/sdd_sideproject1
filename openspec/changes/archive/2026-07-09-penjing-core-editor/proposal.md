## Why

「筆境」目前需要先建立可用的核心編輯骨架，才能承接後續的檔案管理、導出與更完整的寫作流程。這一版要先解決的問題是：提供一個專注、即時、且能穩定渲染複雜 Markdown 內容的基礎工作區。

## What Changes

- 建立「筆境」的雙欄 Markdown 編輯與即時預覽主介面，並在桌面與行動裝置上維持一致的使用邏輯。
- 導入頂部導覽列、快捷工具列、雙欄工作區與底部狀態列，作為 MVP 的固定骨架。
- 建立即時 Markdown 渲染流程，涵蓋基礎語法、程式碼高亮與 Mermaid 圖表繪製。
- 對 Mermaid 重新繪製加入防抖控制，避免在連續輸入時造成明顯卡頓。
- 預設採用淺色模式與繁體中文介面，作為全站基準設定。

## Capabilities

### New Capabilities
- `editor-shell`: 定義「筆境」的版面結構、工具列、底部狀態列、行動裝置切換邏輯、字體縮放與文字統計行為。
- `markdown-rendering`: 定義 Markdown 內容的即時解析、程式碼區塊高亮、Gherkin / Cucumber 關鍵字著色，以及 Mermaid 圖表渲染與防抖要求。

### Modified Capabilities
- 無

## Impact

- 主要影響單一 `index.html` 前端入口與其內嵌的原生 JavaScript 邏輯。
- 會新增對 Tailwind、marked、highlight.js、marked-highlight 與 Mermaid CDN 的依賴。
- 會建立後續規格與任務的基準，讓之後的檔案導出、工作區管理與擴充功能能沿用同一套編輯核心。

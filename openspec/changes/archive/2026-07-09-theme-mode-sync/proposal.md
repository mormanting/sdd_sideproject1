## Why

「筆境」已經有穩定的編輯骨架，下一步需要補上晝夜模式切換，讓長時間寫作時能依場景調整視覺壓力。這次不只是切換背景色，還要把程式碼高亮與 Mermaid 圖表一起切到對應主題，否則視覺會出現不一致。

## What Changes

- 新增頂部導覽列的主題切換按鈕，支援淺色與深色模式互切。
- 使用 `localStorage.theme` 記憶使用者的主題選擇，並在初始化時優先套用。
- 以 `<html>` 的 `.dark` class 作為全站深色模式開關，讓 Tailwind 樣式同步切換。
- 動態切換 Highlight.js 的樣式表 CDN，讓程式碼高亮在深色與淺色模式下都維持可讀性。
- 在主題切換時重新初始化 Mermaid 主題並重繪當前圖表，避免圖表配色與背景脫節。

## Capabilities

### New Capabilities
- `theme-switching`: 定義主題切換按鈕、狀態記憶、初始化預設與全站深色 class 套用行為。
- `theme-rendering-linkage`: 定義 Highlight.js 樣式表切換與 Mermaid 主題重建、重繪的聯動行為。

### Modified Capabilities
- 無

## Impact

- 主要影響 `index.html` 的頂部導覽列、全站配色狀態與初始化流程。
- 需要為 Highlight.js CSS `<link>` 增加可切換的 `id`，並由 JavaScript 直接替換 `href`。
- Mermaid 初始化與圖表重繪流程會變成主題感知，這會影響現有的預覽更新邏輯。
- 需要新增對 `localStorage.theme` 的讀寫，作為視覺狀態的持久化來源。

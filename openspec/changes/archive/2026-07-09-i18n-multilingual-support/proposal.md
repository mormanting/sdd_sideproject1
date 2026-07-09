## Why

「筆境」目前已經具備編輯、主題與圖表聯動，但所有介面文字仍以單一語系為前提。這會限制後續面向不同市場的擴充，也讓新增語系時必須回頭改 HTML 與元件結構，成本過高。

## What Changes

- 建立語系切換器，讓使用者可在繁體中文與 English 之間即時切換，且不需重新整理頁面。
- 將全站可見文案改為資料驅動，改由 JavaScript 字典與 `data-i18n` 屬性注入。
- 使用 `localStorage.lang` 記憶語系偏好，並在初始化時優先套用。
- 將導覽列、工具列、狀態列、主題控制提示與 Mermaid 錯誤提示納入同一套翻譯管線。
- **BREAKING**: 移除 HTML 內硬編碼的顯示文案，改以語系字典提供所有可見文字。

## Capabilities

### New Capabilities
- `language-switching`: 定義語系選單、語系狀態、初始化邏輯與 `localStorage.lang` 持久化。
- `localized-ui-copy`: 定義全站 UI 文案的資料驅動映射、`data-i18n` 掃描與即時翻譯覆蓋範圍。

### Modified Capabilities
- 無

## Impact

- 主要影響 `index.html` 的所有可見文案與其初始化流程。
- 需要將品牌、導覽列、工具列、底欄、主題控制提示與錯誤訊息改為由 JavaScript 字典輸出。
- 會新增語系狀態管理與 DOM 同步更新流程，並與既有主題、渲染與狀態列更新共用單頁架構。
- 未來新增日語、韓語等語系時，只需擴充 JavaScript 字典，不必重構 HTML。

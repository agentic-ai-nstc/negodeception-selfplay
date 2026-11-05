# gemini-3.1-flash-lite

- 模型全名：google/gemini-3.1-flash-lite

## 來源：openrouter

- 執行方式：OpenRouter，供應者固定 google-ai-studio
- 局數 170；公開對話 1,626,767 Qwen tokens；輸入 64,106,987／生成 3,689,096 tokens（供應端 usage）；花費 $21.56
- 不實率：成本／估值 0.025、庫存／需求 0.1397

| 格子 | 局數 | 輸入 tokens | 生成 tokens | 花費 USD | 不實率 成本/估值 | 不實率 庫存/需求 |
|---|---|---|---|---|---|---|
| buyers-vs-concession__google_gemini_3.1_flash_lite__free | 20 | 3,471,450 | 233,071 | 1.218 | 0.004 | 0.0542 |
| buyers-vs-concession__google_gemini_3.1_flash_lite__permitted | 20 | 3,697,501 | 250,400 | 1.300 | 0.0026 | 0.0485 |
| self__google_gemini_3.1_flash_lite__free | 30 | 14,298,953 | 819,917 | 4.805 | 0.001 | 0.1466 |
| self__google_gemini_3.1_flash_lite__honest | 30 | 13,276,012 | 783,971 | 4.495 | 0.0 | 0.1501 |
| self__google_gemini_3.1_flash_lite__permitted | 30 | 16,257,024 | 901,979 | 5.417 | 0.0448 | 0.1691 |
| sellers-vs-concession__google_gemini_3.1_flash_lite__free | 20 | 6,253,580 | 336,300 | 2.068 | 0.0035 | 0.1449 |
| sellers-vs-concession__google_gemini_3.1_flash_lite__permitted | 20 | 6,852,467 | 363,458 | 2.258 | 0.1099 | 0.1495 |

## 已知問題

- pilot 觀察到較常記錯自己的狀態（例如以為某筆成交已成立而宣稱賣完／買齊），謊帳會把這類狀態搞錯記成不實主張；分析說謊時建議用 scripts/claim_audit.py 的 kind_guess 區分 lie 與 state_error。

共同的規則、條件定義、欄位說明與限制見上層 README.md；數字同 stats.json。

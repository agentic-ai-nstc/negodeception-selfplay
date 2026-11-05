# gemma-4-31b

- 模型全名：google/gemma-4-31b-it

## 來源：openrouter

- 執行方式：OpenRouter，供應者固定 deepinfra/fp8
- 局數 86；公開對話 331,655 Qwen tokens；輸入 7,054,477／生成 652,546 tokens（供應端 usage）；花費 $1.67
- 不實率：成本／估值 0.0757、庫存／需求 0.0082

| 格子 | 局數 | 輸入 tokens | 生成 tokens | 花費 USD | 不實率 成本/估值 | 不實率 庫存/需求 |
|---|---|---|---|---|---|---|
| buyers-vs-concession__google_gemma_4_31b_it__free | 13 | 1,017,366 | 91,075 | 0.240 | 0.0 | 0.0 |
| buyers-vs-concession__google_gemma_4_31b_it__permitted | 10 | 800,584 | 69,766 | 0.188 | 0.1458 | 0.0024 |
| self__google_gemma_4_31b_it__free | 15 | 1,301,456 | 126,584 | 0.311 | 0.0 | 0.0175 |
| self__google_gemma_4_31b_it__honest | 14 | 1,158,311 | 115,221 | 0.278 | 0.0 | 0.0091 |
| self__google_gemma_4_31b_it__permitted | 10 | 886,992 | 86,066 | 0.212 | 0.2627 | 0.0079 |
| sellers-vs-concession__google_gemma_4_31b_it__free | 14 | 1,061,999 | 92,612 | 0.249 | 0.0 | 0.0071 |
| sellers-vs-concession__google_gemma_4_31b_it__permitted | 10 | 827,769 | 71,222 | 0.194 | 0.2175 | 0.0145 |

## 已知問題

- 信任度幾乎都給 3，資訊量低。
- 跟 gemma-4-26b-a4b（HPC）是不同模型，不要合併。

共同的規則、條件定義、欄位說明與限制見上層 README.md；數字同 stats.json。

# qwen3.6-27b

- 模型全名：Qwen/Qwen3.6-27B（OpenRouter 名稱 qwen/qwen3.6-27b）

## 來源：cgi01-vllm

- 執行方式：CGI01 本地 vLLM（max_model_len 8192）；脈絡上限 7000 字、互評 8192 tokens
- 局數 50；公開對話 282,130 Qwen tokens；輸入 8,376,742／生成 968,357 tokens（供應端 usage）；花費 $0.00
- 不實率：成本／估值 0.0、庫存／需求 0.0859

| 格子 | 局數 | 輸入 tokens | 生成 tokens | 花費 USD | 不實率 成本/估值 | 不實率 庫存/需求 |
|---|---|---|---|---|---|---|
| self__qwen_qwen3.6_27b__free__cgi01-ctx7000 | 50 | 8,376,742 | 968,357 | 0.000 | 0.0 | 0.0859 |

## 來源：openrouter

- 執行方式：OpenRouter，供應者固定 deepinfra/fp8；脈絡上限 20000 字、互評 32000 tokens
- 局數 66；公開對話 358,053 Qwen tokens；輸入 8,145,098／生成 887,482 tokens（供應端 usage）；花費 $5.45
- 不實率：成本／估值 0.0054、庫存／需求 0.0614

| 格子 | 局數 | 輸入 tokens | 生成 tokens | 花費 USD | 不實率 成本/估值 | 不實率 庫存/需求 |
|---|---|---|---|---|---|---|
| buyers-vs-concession__qwen_qwen3.6_27b__free | 10 | 1,222,566 | 102,818 | 0.720 | 0.0 | 0.0231 |
| buyers-vs-concession__qwen_qwen3.6_27b__permitted | 9 | 1,055,182 | 101,807 | 0.663 | 0.0317 | 0.0297 |
| self__qwen_qwen3.6_27b__free | 10 | 1,229,918 | 159,821 | 0.905 | 0.0 | 0.0755 |
| self__qwen_qwen3.6_27b__honest | 10 | 1,814,334 | 197,315 | 1.212 | 0.0019 | 0.104 |
| self__qwen_qwen3.6_27b__permitted | 7 | 1,168,768 | 138,421 | 0.817 | 0.0091 | 0.0584 |
| sellers-vs-concession__qwen_qwen3.6_27b__free | 10 | 776,198 | 84,550 | 0.519 | 0.0 | 0.0437 |
| sellers-vs-concession__qwen_qwen3.6_27b__permitted | 10 | 878,132 | 102,750 | 0.610 | 0.0 | 0.0545 |

## 已知問題

- 格子 self__qwen_qwen3.6_27b__free__cgi01-ctx7000 是 CGI01 本地 vLLM 的 50 局（只有 free、seeds 0–49）：脈絡上限只有 7000 字（188 次呼叫被截掉較早內容），條件跟 openrouter 的 self__qwen_qwen3.6_27b__free 不同，**不能直接合併**；格子名稱刻意加了 __cgi01-ctx7000 分開放。

共同的規則、條件定義、欄位說明與限制見上層 README.md；數字同 stats.json。

# gemma-4-26b-a4b

- 模型全名：gemma-4-26B-A4B-it（vLLM 服務名稱 gemma-4-26b）

## 來源：hpc-vllm

- 執行方式：NYCU-HPC 上直連 vLLM（DGX-H200-CN04，max_model_len 32768），不經 router；脈絡上限 20000 字、互評 32000 tokens，與 OpenRouter 相同
- 局數 226；公開對話 1,377,192 Qwen tokens；輸入 42,120,002／生成 4,276,484 tokens（供應端 usage）；花費 $0.00
- 不實率：成本／估值 0.0001、庫存／需求 0.0328

| 格子 | 局數 | 輸入 tokens | 生成 tokens | 花費 USD | 不實率 成本/估值 | 不實率 庫存/需求 |
|---|---|---|---|---|---|---|
| self__gemma_4_26b__free | 82 | 15,171,822 | 1,543,783 | 0.000 | 0.0 | 0.0334 |
| self__gemma_4_26b__honest | 72 | 13,187,353 | 1,351,750 | 0.000 | 0.0001 | 0.0341 |
| self__gemma_4_26b__permitted | 72 | 13,760,827 | 1,380,951 | 0.000 | 0.0002 | 0.0309 |

## 已知問題

- 幾乎不回信任度：信任度提示只列主張則數，模型多半回「請提供對話紀錄」而不輸出 <T> 標籤（peer.errors 的 missing_trust）；collect_dataset --check 因此把各局標成互評失敗，PM 決定不修。
- 主張判斷大多是 uncertain（約 77%）。
- MoE 的 26B-A4B，跟 OpenRouter 上的 gemma-4-31b-it 是不同模型，不要合併。

共同的規則、條件定義、欄位說明與限制見上層 README.md；數字同 stats.json。

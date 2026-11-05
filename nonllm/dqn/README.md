# dqn

- 模型全名：DQN（agents/checkpoints/dqn_seller.pt、dqn_buyer.pt）

## 來源：selfplay

- 執行方式：nv12 CPU
- 局數 50000；公開對話 286,112,706 Qwen tokens
- 不實率：成本／估值 0.0、庫存／需求 None

| 格子 | 局數 | 輸入 tokens | 生成 tokens | 花費 USD | 不實率 成本/估值 | 不實率 庫存/需求 |
|---|---|---|---|---|---|---|
| none-dqn | 50000 | 0 | 0 | 0.000 | 0.0 | None |

## 已知問題

- 固定句型，文字高度重複；不說謊（主張都與事實相符）；沒有互評。

共同的規則、條件定義、欄位說明與限制見上層 README.md；數字同 stats.json。

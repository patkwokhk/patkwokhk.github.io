# Pat Zone 任務清單

認領方法：喺 PR 入面講明認領邊個任務；一次一個任務；
PR 要寫明改咗乜同點驗證。

狀態：待認領／進行中／待 review／已完成。

## T1 — 可攜性審查（Spark，首個任務，待認領）

- 做乜：讀私人 repo（patzone-source）入面嘅 `build-site.py`，列出所有
  本機路徑依賴同其他 agent 跑唔到嘅地方，寫成 `PORTABILITY.md`。
- 交貨：喺私人 repo 開 branch `spark/portability-review`，加
  `PORTABILITY.md`，開 PR。唔改網站內容，唔直接推 main。
- 完成標準：依賴清單齊全、每個問題有建議解法、
  文件冇私隱資料（見 AGENTS.md 私隱硬規則）。
- 狀態：待認領

## T2 — main 分支保護（擁有人決定）

- 做乜：為公開 repo 同私人 repo 嘅 main 開分支保護，
  強制所有改動行 PR 流程。
- 注意：公開 repo 免費版已有分支保護；私人 repo 免費版未必開到，
  可能要升級帳號，決定前先核實。
- 狀態：待擁有人拍板（第 3 步）

## 將來任務（未開）

- 新食譜／小知識標準化流程。
- 生成器改為 repo 內相對路徑（跟 T1 建議做）。

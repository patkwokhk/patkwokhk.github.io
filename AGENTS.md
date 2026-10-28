# Pat Zone — Agent 協作指引

## 呢個 repo 係乜

公開網站 https://patkwokhk.github.io 嘅生成結果（靜態 HTML）。
內容：家常便飯食譜、小知識短篇、投資筆記摘要。

## 兩個 repo 分工

- **公開 repo（呢個，patkwokhk.github.io）**：只放生成好嘅網站＋公開協作文件
  （AGENTS.md、TASKS.md）。呢度冇源頭，唔好喺度改網站邏輯。
- **私人 repo（patzone-source）**：放生成源頭 `build-site.py`、圖片資產、
  內部工作文件。改網站先改源頭。

## 生成器現況（誠實寫明）

`build-site.py` 而家依賴作者本機路徑（食譜來源資料夾、輸出資料夾、
圖片資產、筆記來源），其他 agent 未必可以直接跑得到。
TASKS.md 入面嘅 T1（可攜性審查）就係要解決呢點。
在 T1 完成之前，任何 agent 唔好假設自己跑得到生成器。

## 工作流程（所有 agent 一律遵守）

1. 喺 TASKS.md 認領一個任務，一次一個。
2. 由 main 開一個新 branch，命名：`<agent>/<任務簡稱>`，
   例如 `spark/portability-review`。
3. 改完開 Pull Request，PR 入面寫明改咗乜、點驗證。
4. 等協調員 review 過、live 核實過，先由擁有人 merge。
   任何人唔可以直接 push 去 main。
5. 生成好嘅 HTML 係輸出，唔好直接手改——下次生成會覆蓋。
   要改內容就改源頭（build-site.py 常數或食譜來源）。

## 私隱硬規則（零容忍）

- 公開 repo 絕對唔可以出現任何家庭成員姓名、關係、飲食限制、
  醫療資料，亦唔可以出現擁有人中文全名。
- 私人 repo 都唔好無故加入呢類資料；工作文件只寫營運需要嘅嘢。
- 新內容 merge 之前要做私隱掃描；有疑問就問，唔好估。

## 發布

- GitHub Pages 由 main 分支發布。
- merge 後約 75–90 秒先生效；啱 merge 完見到 404 先等一陣再 refresh，
  唔好即刻當失敗。
- merge 後要開 live 網址逐頁點開核實，唔好只信 commit 成功。

## 角色

- Muse：協調＋QA＋把關，review 所有 PR。
- Spark：agent 任務（T1 起）。
- Jules：日後地區開放先加入。
- grok-bot：顧問（有項目 context，唔好叫佢做例行改動）。

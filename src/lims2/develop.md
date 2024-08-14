# 💻日常開發流程 Develop

- 描述 `PG` 日常開發功能流程
- 首先要取得 `SA` 開立 `mantis單號`
- 接著確認已經切換到起始分支 (通常是 `dev`)
- 然後建立新分支，按上方工具列 Branch

# 📊流程圖

![](../../asset/lims-develop.svg)

# 🌱建立功能開發分支 Create (Feature) Branch

![](../../asset/lims2/dev-create-branch.png)

- ⚠️注意目前分支是否為 `dev` (避免從開發中的分支長出分支)
- 輸入分支名稱，使用前綴 `f/` 加 `mantis單號`
- 按下 Create Branch

![](../../asset/lims2/dev-create-branch-finish.png)

- 分支建立完成時，會與其起始分支內容相同(版本相同)
- 例如上圖 `f/1234` 和 `dev` 會在同一個 `node` 上
- Sourcetree 左側也會出現分支，如果有前綴詞則會自動分類

# 🛠️完成功能開發 Finish Feature

- 分支開好後，即可(在分支上)開始進行功能開發
- 完成後記得 `add` 並 `commit`，同時撰寫 commit message
- 下圖是一個完成功能的示範

![](../../asset/lims2/dev-branch-commit.png)

- 提交了兩次修改 = 兩次 `commit`
- 可以看到 `f/1234` 領先了其他分支**兩個**版本 (或說兩個 `node`)

# 🔄合併分支 Merge (Feature) Branch

- 開發完畢需將修改併入 `dev`，以便更新到測試環境
- Git 並沒有併入 `merge into` 這種行為(指令)
- 所以實際是先切換(checkout)到 `dev`，然後合併 `merge` 分支 `f/1234`

![](../../asset/lims2/dev-switch-to-dev.png)

- Sourcetree 左側選單點兩下 `dev` 即可切換分支，指令可用 `checkout` or `swtich`
- 🚨務必注意切換前原本修改已經 `commit` 或者 add to `stash`

![](../../asset/lims2/dev-merge-feature-branch.png)

- 確認目前分支為 `dev`
- 點選 Sourcetree 上方 Merge 按鈕
- 選擇要併入的分支(或者說節點)進行合併，此為 `f/1234`

![](../../asset/lims2/dev-ready-to-push.png)

- 合併完成後，會看到 `dev` 已經與 `f/1234` 在同一個 `node`
- 表示 `dev` 已包含 `f/1234` 修改內容
- Sourcetree 會提示可進行 `push` (判斷 `dev` 與 `origin/dev` 有差距)

# 🚀推送更新 Push

- 推送 `push` 本地的修改歷程到遠端
- 每日版更人員即可取得資料並進行版更

![](../../asset/lims2/dev-pushing.png)

- 點選 Sourcetree 上方工具列 Push
- 勾選分支 `dev` 後點選 Push 按鈕

![](../../asset/lims2/dev-pushed.png)

- 完成推送後，遠端(的追蹤)分支 `origin/dev` 應該與本地版本一致
- 到此便完成一個功能的開發，版更人員拉取遠端 `dev` 即可取得更新

# ⚠️注意事項

- 推送 `push` 資料時，如版本差異，Sourcetree 應會提示警告
- 建議平常就執行 `fetch` 更新追蹤分支 `origin/dev` 如有衝突比較能第一時間解決
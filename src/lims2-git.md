---
marp: true
paginate: true
footer: git-`lims2.0`
---

![bg left](https://picsum.photos/1080?image=1002)

##### ![w:160](../asset/gitlogo.png)  LIMS 2.0 Workflow
###
```bat
git --implement "LIMS" -v 2.0 🤖
```
#
#

`OAD` **Brian Li**

---

![bg right](https://picsum.photos/1080?image=1006)

# **A**genda

- 🔍**流程圖檢視要點**
- 🔄**主要流程拆解**
  開發流程
  每日更新
  每周更新(OAD)
  每周更新(IT)
- 📝**說明討論與注意事項**
- 🎭**使用情境**
- 🚀**未來規劃**

---

![bg left](https://picsum.photos/1080?image=1050)

### 💻常見**指令**中英對照

|||
|-:|-|
|**clone**|`複製` `下載`|
|**checkout**|`簽出(指定分支)`|
|**add**|`新增` `加入(檔案到暫存)`|
|**commit**|`提交(版本更新)`|
|**merge**|`合併(分支、更新內容)`|
|**push**|`推送(更新歷程到遠端)`|
|**pull**|`拉取(更新歷程)`|
|**fetch**|`擷取 = 更新追蹤分支`|

---

![bg 85%](..//asset/lims-workflow.svg)

---

![bg left fit](../asset/lims-samples.svg)

# 🔍流程圖**檢視要點**

- 各項目使用不同圖示區別
- 流程不包含 `SQL Script` `文件` 與 `ClientAPI` 等，僅針對主程式開發與更新流程進行說明
- 相關回覆訊息都只是舉例，可以表述執行內容即可
- 從 `START` 開始，往 `END` 結束
###
>💡左邊有幾個流程圖項目與圖例

---

![bg right:60% 95%](../asset/lims-first-use.svg)

# **初次**使用[📝](../src/lims2/first-use.md)

- 初次使用請先 `clone`
- `clone` 預設簽出**預設分支**(通常就是 `main`)
- 其他分支需**自行簽出**

#

>💡未來如有其他遠端分支需下載到本地使用，同樣要 `checkout`
>📝表示有文件可參考

---

![bg right:30%](https://picsum.photos/1080?image=1023)

# 🔄主要流程**拆解**

- **開發流程 Feature Development** [📝](../src/lims2/develop.md)
  日常功能開發流程，包含 `SA` 開單與 `PG` 開發等
- **每日更新 Daily Update** [📝](../src/lims2/daily-update.md)
  `PG` 每日更新，以及更新後 `SA` 通知 `BU` 等流程
- **每周更新 Weekly Update (OAD)** [📝](../src/lims2/weekly-update-oad.md)
  `SA` 通知 `PG` 推送更新並建立 `PR`，審核併入 `main`
- **每周更新 Weekly Update (IT)** [📝](../src/lims2/weekly-update-it.md)
  `SA` 拉取 `main` 編譯並發布，聯絡 `PM` 通知 `IT`
  #
>📝表示有額外文件可參考
---

![bg fit](..//asset/lims-develop.svg)

---

![bg fit](..//asset/lims-daily-update.svg)

---

![bg fit](..//asset/lims-weekly-update-oad.svg)

---

![bg fit](..//asset/lims-weekly-update-it.svg)

---

![bg right:35%](https://picsum.photos/1080?image=1010)

# 🧠說明討論**與**注意事項

- 主要分支為 `main` 與 `uat`
- `clone` 後，請確認已簽出 `main` 與 `uat`
- `main` 遠端設定保護，不可 `push`，更新開 `PR`
- ⚠️開發請由 `main` 開分支，完成後併入 `uat`
- 開發功能分支 `feature` 前綴使用 `f/`
- 測試版更分支前綴可用 `u/`，正式版更 `r/`
- 每日與週更新建議(但不強制)用 `分支` 管理
- ⚠️確認 VS2022 **不在**偵錯狀態下再操作版控
- ⚠️功能未完成需切換分支，可 `stash` 或乾脆先 `commit`，避免切換分支前殘留 `unstaged` 檔案

---

![bg left:35%](https://picsum.photos/1080?image=1060)

# 🎭使用情境 **Use Case**

- 🚧剛剛 `main` 更新了，手邊還有**開發中**功能[📝](../src/lims2/usecase-sync-main.md)
- 🐛正式機**剛上線**發現異常，需進行快速修復
- 🔗多張需求單有**關聯**，程式邏輯重疊可一起做
- ⚡開發到一半，突然來了緊急**插件**，怎麼辦
- 💥完蛋，程式發生**衝突**了
#
>📝表示有額外文件可參考

---

![bg 75%](../asset/lims-usecase-sync-main.svg)

---

![bg fit](../asset/lims-usecase-hotfix.svg)

---

![bg 85%](../asset/lims-usecase-related-feature.svg)

---

![bg 85%](../asset/lims-usecase-urgent-issue.svg)

---

![bg right:40%](https://picsum.photos/1080?image=1062)

# 💥衝突 **Conflict**

- **版本控制** = 檔案**歷程管控**與**差異整併**
- 任何**合併操作**都**可能**產生衝突 `conflict`
- git 常見**合併操作**包括：
  `merge` `rebase` `cherry-pick` `squash`
- 良好的**架構**與**分工**，可有效避免衝突
- 時常**同步** `main`，也可降低衝突機率
- git 可自訂 `diff-tool` 與 `merge-tool`
###
>💡程式衝突可找相關開發者一起討論，避免衍伸出其他更多衝突(物理)😆

---

<!-- _class: invert -->

![bg left:50%](https://picsum.photos/1080?image=1041)

# ➡️**Next** Steps

- **Automation**
  Batch Command
  Powershell Script

- **CI/CD**
  Continuous Intergration
  Continuous Delivery / Deplyment
  Gitea Runner / Actions

---

![bg right:60%](https://picsum.photos/1080?image=1035)

# 😀 Thank you !

feel free to ask if you have any other questions

#

🏢 **OAD** 
👤 Brian Li
📞 `#1429`
📧 brian.li@sgs.com
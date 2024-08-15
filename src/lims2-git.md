---
marp: true
paginate: true
footer: git-`lims2.0`
---

![bg left](https://picsum.photos/1080?image=1002)

##### ![](../asset/gitlogo.png) in LIMS 2.0
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

- **流程圖檢視要點**
- **流程拆解**
  開發流程
  每日更新
  每周更新(OAD)
  每周更新(IT)
  每周更新之後
- **說明與討論事項**
- **討論結果與注意事項**
- **未來可能規劃**

---

![bg left fit](../asset/lims-samples.svg)

# 流程圖**檢視要點**

- 不同項目使用不同圖示區別
- 流程不包含 `SQL Script` `文件` 與 `ClientAPI` 等，僅針對主程式開發與更新流程進行說明
- 相關回覆訊息都只是舉例，可以表述執行內容即可
- 從 `START` 開始，往 `END` 結束
###
>💡左邊是流程圖項目與範例說明

---

![bg left](https://picsum.photos/1080?image=1050)

### 常見**名詞**中英對照與說明

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

![bg right:30%](https://picsum.photos/1080?image=1023)

# 流程**拆解**

- **開發流程 Develop**
  日常功能開發流程，包含 `SA` 開單與 `PG` 開發等
- **每日更新 Daily Update**
  `PG` 每日更新，以及更新後 `SA` 通知 `BU` 等流程
- **每周更新 Weekly Update (OAD)**
  `SA` 通知 `PG` 推送更新並建立 `PR`，審核併入 `main`
- **每周更新 Weekly Update (IT)**
  `SA` 拉取 `main` 編譯並發布，聯絡 `PM` 通知 `IT`
- **每周更新之後 After Weekly Update**
  建議(但不強制)開發中的功能合併最新 `main`

---

![bg fit](..//asset/lims-develop.svg)

---

![bg fit](..//asset/lims-daily-update.svg)

---

![bg fit](..//asset/lims-weekly-update-oad.svg)

---

![bg fit](..//asset/lims-weekly-update-it.svg)

---

![bg 75%](../asset/lims-develop-after-weekly-update.svg)

---

![bg left:40%](https://picsum.photos/1080?image=1010)

# 說明與**討論**

- 如使用 `git-flow` 請注意其**預設行為**❗
- 主要分支是否為 `main` 與 `develop`❓
- `develop` 是否簡化為 `dev`❓
- `feature` 是否簡化為 `f`，例如 `f/1234`❓
- `release` 是否簡化為 `r`，例如 `r/1234`❓
- 每日更新是否需建立 `release` 分支❓
- `release` 是否簡化為 `uat`❓
###
>💡任何的合併行為都可能產生衝突，如沒把握排除請知會相關提交人員一起協助

---

![bg right:35%](https://picsum.photos/1080?image=1058)

# 討論**結果**與注意事項

- 主要分支為 `main` 與 `dev`
- `clone` 後，請確認已簽出 `main` 與 `dev`
- `main` 設定保護，不可 `push`，提交更新走 `PR`
- ⚠️開發請由 `main` 開分支，完成後併入 `dev`
- 功能分支 `feature` 前綴使用 `f/`
- 發行分支 `release` 前綴可用 `r/`
- 每日更新建議(但不強制)用 `release` 管理
- ⚠️確認 VS2022 **不在**偵錯狀態下，再操作版控
- ⚠️功能未完成需切換分支，可用 `stash` 或者乾脆先 `commit`，避免切換前殘留 `unstaged` 檔案

---

<!-- _class: invert -->

![bg left:50%](https://picsum.photos/1080?image=1041)

# **Next** Steps

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
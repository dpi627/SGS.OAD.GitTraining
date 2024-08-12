---
marp: true
paginate: true
footer: git-`lims2.0`
---

![bg left](https://picsum.photos/720?image=1002)

##### ![](../asset/gitlogo.png) in LIMS 2.0
###
```bat
git --implement "LIMS" -v 2.0 🤖
```
#
#

`OAD` **Brian Li**

---

![bg right](https://picsum.photos/720?image=1006)

# **A**genda

- **流程圖檢視要點**
- **流程圖拆解**
  開發流程
  每日更新
  每周更新(OAD)
  每周更新(IT)
- **說明與討論事項**
- **未來規劃**

---

![bg left fit](../asset/lims-samples.svg)

# 流程圖**檢視要點**

- [前提] `main` 限特殊權限操作
- [前提] `PG` 僅操作 `develop`
- 流程不包含 `SQL Script` `文件` 與 `ClientAPI`，僅針對主程式更新流程進行說明、討論
- 相關回覆訊息都只是舉例，可以表述執行內容即可
- 從 `START` 開始，往 `END` 方向走

>💡左邊是流程圖項目與範例說明

---

![bg left](https://picsum.photos/720?image=1050)

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

![bg right:30%](https://picsum.photos/720?image=1023)

# 流程圖**拆解**

- **開發流程 Develop**
  日常功能開發流程，包含 `SA` 開單與 `PG` 開發等
- **每日更新 Daily Update**
  `PG` 每日更新，以及更新後 `SA` 通知 `BU` 等流程
- **每周更新 Weekly Update (OAD)**
  `SA` 通知 `PG` 推送更新並建立 `PR`，審核併入 `main`
- **每周更新 Weekly Update (IT)**
  `SA` 拉取 `main` 編譯並發布，聯絡 `PM` 通知 `IT`
#
>💡流程如有未盡之處，還請大家不吝提出建議

---

![bg fit](..//asset/lims-develop.svg)

---

![bg fit](..//asset/lims-daily-update.svg)

---

![bg fit](..//asset/lims-weekly-update-oad.svg)

---

![bg fit](..//asset/lims-weekly-update-it.svg)

---

![bg right:40%](https://picsum.photos/720?image=1010)

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

<!-- _class: invert -->

![bg left:50%](https://picsum.photos/720?image=1041)

# **Next** Steps

- **Automation**
  Batch Command
  Powershell Script

- **CI/CD**
  Continuous Intergration
  Continuous Delivery / Deplyment
  Gitea Runner / Actions

---

![bg right:60%](https://picsum.photos/720?image=1035)

# 😀 Thank you !

feel free to ask if you have any other questions

#

🏢 **OAD** 
👤 Brian Li
📞 `#1429`
📧 brian.li@sgs.com
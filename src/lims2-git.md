---
marp: true
paginate: true
footer: git-`lims2.0`
---

![bg left](https://picsum.photos/1080?image=1002)

##### ![w:160](../asset/gitlogo.png) Workflow in LIMS
###
```bat
git --implement "LIMS" -v 2.0 🤖
```
###### 🚧 LIMS工作流程建置與導入
#
#

`OAD` **Brian Li**

---

![bg right:40%](https://picsum.photos/720?image=1005)

## 👤**適合**對象

- 參與化性 LIMS 專案同仁 (不限形式)
- 具備 Git 基礎知識，包含 CLI 與 GUI 使用
- 了解工作流程 `Workflow` 基本概念

## 🎯預期**目標**

- 完成 LIMS 新工作流程制訂與實行
- 解決 SSDLC 稽核缺失
###
>💡需要複習的同仁，可參考之前分享資料 [`0`](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/publish/section0.pdf) [`1`](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/publish/section1.pdf) [`2`](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/publish/section2.pdf) [`3`](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/publish/section3.pdf) [`4`](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/publish/section4.pdf) [`5`](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/publish/section5.pdf) 與 [`快速上手`](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/publish/quick-start.pdf) [`GitFlow`](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/publish/GitFlow.pdf)

---

![bg left:60%](https://picsum.photos/1080?image=1068)

# 🏷️Agenda

- 🔍**流程圖檢視要點**
- 🔄**主要流程拆解**
  　功能開發
  　每日更新
  　每周更新 `OAD` `IT`
- 💬**說明與注意事項**
- 🎭**使用情境演示**
- ✅**已知問題處理**
- 🚀**未來規劃**

---

![bg right:45%](https://picsum.photos/1080?image=1050)

# 💻常見**指令**

|||
|-:|-|
|**clone**|`複製`、`下載`|
|**checkout**|`簽出(分支、節點)`|
|**add**|`新增`、`加入(檔案到暫存區)`|
|**commit**|`提交(更新內容、檔案修改)`|
|**merge**|`合併(分支)`|
|**push**|`推送(更新歷程到遠端)`|
|**pull**|`拉取(更新歷程到本地)`|
|**fetch**|`擷取(更新本地追蹤分支)`|

---

![bg left:55% fit](../asset/lims-samples.svg)

# 🔍流程圖**檢視要點**

- 各項目使用不同**圖示**區別
- 流程僅針對主程式**開發**、**更新**與**部署**進行說明
- 相關**回覆訊息**都只是舉例，可以表述執行內容即可
- 虛線表示**隱性**或**可忽略**
- 從 `START` 開始往 `END` 結束
#
>💡左邊是流程圖項目與圖例

---

![bg 85%](..//asset/lims-workflow.svg)

---

![bg right:60% 95%](../asset/lims-first-use.svg)

# **初次**使用[📝](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/src/lims2/first-use.md)

- 初次使用請先 `clone`
- `clone` 預設簽出**預設分支** (通常是 `main`)
- 其他分支需**自行簽出**

#

>💡遠端分支在本地使用之前都要 `checkout`
>
>📝表示有文件可參考

---

![bg right:30%](https://picsum.photos/1080?image=1023)

# 🔄主要流程**拆解**

- **功能開發 Feature Development** [📝](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/src/lims2/develop.md)
  日常功能開發流程，包含 `SA` 開單與 `PG` 開發
- **每日更新 Daily Update** [📝](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/src/lims2/daily-update.md)
  `PG` 每日更新測試機，更新後 `SA` 通知 `BU`
- **每周更新 Weekly Update (OAD)** [📝](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/src/lims2/weekly-update-oad.md)
  `SA` 通知 `PG` 推送更新建立 `PR`，審核後併入 `main`
- **每周更新 Weekly Update (IT)** [📝](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/src/lims2/weekly-update-it.md)
  `SA` 拉取 `main` 編譯並發布，通知 `PM` 聯絡 `IT`
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

![bg left:40%](https://picsum.photos/1080?image=1010)

# 💬說明事項

- 常駐分支為 `main` 與 `uat`
- `main` 為穩定分支，部署正式機使用
- `uat` 為測試分支，部署測試機使用
- 遠端 `main` 設定保護、禁止隨意 `push`
- 更新 `main` 需建立 `PR`，專人審核後併入
- 開發功能 `feature` 分支前綴使用 `f/`
- 每日與每週更新**建議**用分支管理
- 每日更前綴可用 `u/`，每週更新 `r/`
- 熱修 `hotfix` 前綴可用 `h/`

>⚠️務必確認常駐分支 `main` `uat` 均已簽出

---

![bg right:35%](https://picsum.photos/1080?image=1081)

# 🚨**注意**事項

- ⚠️**任何操作**均需確認**當前分支**與**目標分支**
- 開發由 `main` 開分支，完工後切換 `uat` 合併
- **關閉**開發工具再操作版控有機會避免一些問題
- 提交時務必確認修改檔案**名稱**與**內容**是否正確
- 提交時如發現異常修改，確認後可 `Discard`
- 開發中**切換分支**，可以先 `commit` 或 `stash`，盡量避免切換分支時殘留 `unstaged` 檔案
- ⚠️**任何操作**均需確認**當前分支**與**目標分支**
- ⚠️**任何操作**均需確認**當前分支**與**目標分支**

---

![bg left:35%](https://picsum.photos/1080?image=1060)

# 🎭使用情境 **Use Case**

- 🚧開發功能期間 `main` 進行了**更新**[📝](http://twvoadtpw100004/brian_li/SGS.OAD.GitTraining/src/branch/main/src/lims2/usecase-sync-main.md)
- 🐞正式機剛**上線**就發現異常，需進行**快速修復**
- 🔗多張**關聯**需求單，**共用**程式邏輯可一起開發
- ⚡開發期間突發**緊急插件**，需優先處理
- 😱寫到一半才發現忘了**切換**分支
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

![bg 90%](../asset/lims-usecase-dev-on-wrong-branch.svg)

---

![bg left:40%](https://picsum.photos/1080?image=1062)

# 💥衝突 **Conflict**

- **版本控制** = 檔案**歷程管控**與**差異整併**
- 任何**合併操作**都**可能**產生衝突 `conflict`
- git 常見**合併操作**包括：
  `merge` `rebase` `cherry-pick` `squash`
- 良好的**架構**與**分工**，可有效避免衝突
- 時常**同步** `main`，若發生衝突較易處理
- git 可自訂 `diff-tool` 與 `merge-tool`
###
>💡若程式發生衝突，可找相關開發者一起討論，避免衍生出其他更多衝突(物理)😆

---

![bg right:40%](https://picsum.photos/1080?image=1073)

# ✅已知問題**與**處理

>已知主機 `twvoadtpw100004` 問題，之前使用 `twoadcode` 均沒有遇到，目前無解

- ❓與遠端進行**驗證**時，偶爾會異常
  💡`push` 與 `pull` 時偶爾會遇到，一次不行就跑兩次，通常第二次都會成功

- ❓Email **通知功能**無法使用
  💡`Gitea` 完成特定操作後會發送 Email 通知，目前無法啟用公司信箱作為寄送功能使用，暫時以 `TEAMS` 人工通知取代

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

# 💖 Thank you !

feel free to ask if you have any other questions 😀


#
#

💻 **OAD** 
🤖 Brian Li
📱 `#1429`
✉️ brian.li@sgs.com
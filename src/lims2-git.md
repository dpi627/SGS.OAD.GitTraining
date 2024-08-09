---
marp: true
paginate: true
footer: git-`lims2.0`
---

![bg left](https://picsum.photos/720?image=1002)

##### ![](../asset/gitlogo.png) in LIMS 2.0
###
```bat
git --implement-to "LIMS 2.0" ✨
```
#
#

`OAD` **Brian Li**

---

![bg right](https://picsum.photos/720?image=1006)

# **A**genda

- **流程圖檢視要點**
- **流程拆解**
  開發流程
  每日更新
  每周更新(OAD)
  每周更新(IT)
- **說明與討論事項**

---

![bg left fit](../asset/lims-samples.svg)

# 流程圖**檢視要點**

- 前提：`main` 限特殊權限版控
- 前提：`PG` 僅可控制 `develop`
- 不包含 SQL，版控另行評估
- 不包含 ClientAPI 或其他例外狀況
- 不包含 LIMS 文件更新
- 回覆訊息都只是舉例，沒有強制怎麼寫，看得懂就好
- 從 `START` 開始，往 `END` 方向走

>💡左邊是常見項目與範例圖示

---

![bg right:30%](https://picsum.photos/720?image=1023)

# 流程圖**拆解**

- **開發流程 Develop**
  日常功能開發的流程，包含 `SA` 開單與 `PG` 開發等
- **每日更新 Daily Update**
  版更 `PG` 每日更新流程，以及更新後 `SA` 通知 `BU`
- **每周更新 Weekly Update OAD**
  `SA` 通知 `PG` 退送更新與建立 `PR`，審核後合併
- **每周更新 Weekly Update IT**
  `SA` 拉取 `main` 並編譯後聯絡 `PM` 通知 `IT`
#
>💡單獨思考恐有未盡之處，歡迎大家不吝指教

---

![bg fit](..//asset/lims-develop.svg)

---

![bg fit](..//asset/lims-daily-update.svg)

---

![bg fit](..//asset/lims-weekly-update-oad.svg)

---

![bg fit](..//asset/lims-weekly-update-it.svg)

---

![bg left:40%](https://picsum.photos/720?image=1010)

# 說明與**討論**

- 不建議 git-flow，如使用請注意其**預設行為**
- 主要分支是否為 `main` 與 `develop`
- `develop` 是否改為 `dev`
- `feature` 是否改為 `f`，例如 `f/1234`
- `release` 是否改為 `r`，例如 `r/1234`
- 每日更新是否需建立 `release` 分支
- `release` 是否改為 `uat`
>💡任何的合併行為都可能產生衝突，如沒把握自行排除請支會相關人員協助

---

<!-- _class: invert -->

![bg left:60%](https://picsum.photos/720?image=1041)

# **Next** Steps

- Batch Command
- CI
- CD

---

![bg right:60%](https://picsum.photos/720?image=1035)

# 😀 Thank you !

feel free to ask if you have any other questions

#

🏢 **OAD** 
👤 Brian Li
📞 `#1429`
📧 brian.li@sgs.com
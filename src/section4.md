---
marp: true
paginate: true
headingDivider: 1
footer: git-section-`04`
---

# 
![bg right:33%](https://picsum.photos/720?image=116)
![](../asset/gitlogo.png)
```powershell
git --section 04 -workflow "pull request" ;{
```
##
> **OAD** / brian_li

# **A**genda
![bg left:60%](https://picsum.photos/720?image=126)
- Workflow
- Pull Request
- Code Review
- Demo
- Resources
- Homework

# <!-- workflow -->
![bg fit](../asset/workflow.png)

# Role**s**
![bg left:33%](https://picsum.photos/720?image=323)
||Big|Samll|Dragon|
|-|-|-|-|
|**PM**|Jeff/Lawrence|Jeff|Brian|
|**SA**|Mecer/Amy|Mecer|Brian|
|**SD**|Mecer/Amy|Mecer/Brian|Brian|
|**PG**|Birdie/Neil/Brian|Brian|Brian|
|**QA**|Mecer/Amy/BU|Brian|---|
> 角色種類與人員數量配置因專案大小而異，沒有絕對標準，例如也可能有 **DBA** 或 **ART** 等

#
![bg](../asset/workflow2.png)

# Pull Request - **What** & **Why**
![bg right:33%](https://picsum.photos/720?image=259)

###### A **REQUEST** for ask someone to **PULL** our commits and merge into other branch
######
- 開發者通常在**個人分支**上開發
- 完成開發後需合併回 `main`
- 以防萬一，合併之前應該要接受**檢查**
- 通知**專案負責人**或**其他工程師**
- 經過**檢查**、**討論**或**修改**才進行合併
- 通常由**特殊權限**或**角色**進行合併

# Pull Request - **How**
![bg left:33%](https://picsum.photos/720?image=290)
- `main` branch is usually protected
- create a branch `A`, make changes and commit
- push `A` to remote repo, then go to server*
- create a **PR** (pull request) on server
- discuss = **code review**
- approve** = merge `A` into `main`
######
>*server 意指 Gitea GitHub 或 Azure DevOps
**依照討論結果，也可能拒絕合併再修正

# DEMO on **Gitea**
![bg right:60%](https://picsum.photos/720?image=76)
- ### Pull Request
- ### Code Review

> ⚠️建議學習 `Markdown`

# **Mark**down
![bg left:60% 90%](../asset/md.jpg)
| 優點  | 缺點 |
|------|-----|
|簡潔易讀|學習曲線|
|跨平台|排版限制|
|生態系|非標準化|

> `GitHub` `Gitea` `Jupyter Notebook` `Notion` `GPT`

# Code **Review**
![bg right:20%](https://picsum.photos/720?image=743)
| 優點(品質🔺)                | 缺點(額外成本)                                         |
|----------------------|----------------------------------------------|
| 提高代碼一致性        | 消耗時間和人力                               |
| 發現並修正錯誤        | 可能引起開發者之間的衝突或緊張               |
| 促進知識分享和團隊合作| 可能產生過多的討論和評論                      |
| 學習機會            | 可能會導致拖延和延遲項目進度                 |
| 提高代碼一致性        | 可能忽視小錯誤和問題，導致低效率             |

⚠️必須在同一種架構下才有可能實現，包括 `Language` `FrameWork` `Architecture Pattern` `Design Pattern` `Packages` ... 等等

# **Online** Reources
![bg left:35%](https://picsum.photos/720?image=649)
- [與其它開發者的互動 - 使用 Pull Request（PR）](https://gitbook.tw/chapters/github/pull-request)
- [什麼是 Pull Request?](https://shoujhengduan.medium.com/%E4%BB%80%E9%BA%BC%E6%98%AF-pull-request-b476ee3e0217)
- [如何進行 Code Review?](https://enginebai.medium.com/code-review-guidelines-b76a859c377c)
- [淺談Code Review的好處及意義](https://blog.alantsai.net/posts/2019/05/code-review-what-is-code-review-and-why-we-want-to-do-it)
- [Create Pull Request in Azure DevOps](https://blog.alantsai.net/posts/2019/05/code-review-02-what-is-pull-request-and-how-to-create-it-in-azure-devops)
- [Markdown 官方教程](https://markdown.com.cn/basic-syntax/)


# What's **next** ...
![bg right:34%](https://picsum.photos/720?image=797)
|Subject|Keywords|
|---|---|
|**CI/CD**|`Actions` `Pipline` `yaml`|
|**AI**|`GitHub Copilot CLI` `Commit Message`|
|**Misc.**|`git svn` `azure devops`|
<!-- _class: invert -->

# Home**work**
![bg left:20%](https://picsum.photos/720?image=888)
- Create a `repo`* on [Gitea](http://twoadcode:3000/) or `local`
- Create branch `A`, make chages and commit
- Push `A` to `remote`
- Go to Gitea, create a pull request*
- Find someone to review or just commit yourself
- Send `reop`'s url to [Mecer](mailto:mecer.wu@sgs.com).
###
> *If the `repo` created on `remote`, `clone` it before next step.
**Try `Markdown` during pull request creation
⚠️ Make sure the `remote` `repo` is set to `puclic`.


# 😀 Thank you !
![bg right:60%](https://picsum.photos/720?image=738)
feel free to ask if you have any other questions.
##
> **OAD** / brian_li / #1429
brian.li@sgs.com
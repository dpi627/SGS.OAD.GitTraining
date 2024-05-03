---
marp: true
paginate: true
headingDivider: 1
footer: git-section-`02`
---

# 
![](../asset/gitlogo.png)
```powershell
git --section 02 -branch "remote repo" :(
```
##
> **OAD** / brian_li
![bg right:33%](https://picsum.photos/720?image=213)

# **A**genda
- Branch
- Remote Repository
- Git Server/Service
- Resources
- Homework
![bg left](https://picsum.photos/720?image=143)

#
![bg fit 75%](../asset/branch2.png)

# CLI - **Branch**
|指令|中文|簡述|
|---|---|---|
|**branch**|分支|分支相關操作|
|**checkout**|檢出|切換指定分支*|
|**merge**|合併|以**目前分支**併吞其他分支|
|**rebase**|重設|看不到合併提交，更簡潔|
> *語意上應該是 `checkout` **`to`** `{another-branch}`
`2.23` 之後提供 `switch` 取代 `checkout`
⚠️切換分支時，如有**未提交修改**會警告
⚠️Git 指令永遠都是針對 `目前分支` 進行操作
![bg right:30%](https://picsum.photos/720?image=543)

# DEMO - **Branch**
建立分支
```powershell
git branch dev
```
切換分支 (擇一)
```powershell
git checkout dev
git switch dev
```
合併分支*
```powershell
git merge dev
```
> *注意當前分支是否為 `main`
⚠️只要合併就有機率產生衝突 (conflict)
![bg left:33%](../asset/ignore.jpg)
<!-- _backgroundColor: #ddd -->

# Git - **checkout**
![bg right:60% 95%](../asset/checkout.svg)
- `檢出`特定分支
- 也稱`簽出`/`切換`分支
- 等同取得分支資料
- 取得`HEAD`版本資料

⚠️切換分支後，實體資料會立刻被替換為分支版本內容

⚠️`2.23` 後可用 `switch`

# Git - **merge**
![bg right fit vertical](../asset/merge1.png)
![bg right fit](../asset/merge2.png)
##### Git can automatically merge commits unless there are changes that **conflict** in both commit sequences.
沒衝突會自動合併

# Git - **rebase**
![bg right fit vertical](../asset/rebase1.svg)
![bg right fit](../asset/rebase2.svg)
###### Remember `rebase` can alter the commit history. This can be **dangerous** if not done properly, especially with branches that others are working on.
團隊開發沒事不要 `rebase`，除非大家都很熟悉操作
###### https://needoneapp.medium.com/git-merge-vs-git-rebase-17392c4d870d

#
<!-- Git - cherry-pick -->
![bg fit](../asset/cherrypick3.jpg)
![bg fit](../asset/cherrypick2.jpg)

# Resolving **conflict**
![bg right:60% fit vertical](../asset/conflict1.png)
![bg right 95% vertical](../asset/conflict2.png)
##### 合併有機率**衝突**
- 使用 `<` `=` `>` 標註
- 修改到正確即可

https://gitbook.tw/chapters/branch/fix-conflict

#
![bg fit 90%](../asset/allarea.png)

# CLI - **Remote**

|指令|中文|簡述|
|---|---|---|
|**clone**|複製|下載整個遠端repo*|
|**remote**|遠端|管理遠端相關操作**|
|**push**|推送|上傳修改資料到遠端|
|**pull**|拉取|下載修改資料到本地|
|**fetch**|擷取|下載修改資料到**追蹤分支**|

> *`clone` 取得的 repo 預設非 owner 無法 `push`
**遠端 `repo` 預設別名為 `origin`
![bg right:33%](https://picsum.photos/720?image=550)

# DEMO - **Remote**
設定遠端 `repo`
```powershell
git remote add origin https://xxx.yyy/zzz.git
```
推送資料並設定 `upstream`* (上游)
```powershell
git push -u origin main
```
拉取資料 = `fetch` + `merge`
```powershell
git pull
```
> *透過 `clone` 取得的 `repo` 預設已有 `upstream`
![bg left:33%](../asset/ignore.jpg)
<!-- _backgroundColor: #ddd -->

# Git - **Tracking** Branch
- 與遠端分支關聯的**本地分支**
- `origin` = 遠端 `repo`
- `origin/main` = 遠端 `main` 追蹤分支
- 追蹤分支**僅**用來反映其遠端分支變化
- 本地**無法**直接操作追蹤分支
###
> *左圖為 `ftech` 示意，僅更新追蹤分支
![bg vertical left:44% fit](../asset/fetch3.png)

#
![bg 80%](../asset/trankingBranch.png)

# Git - **push**
![bg right:70% fit](../asset/push1.png)
###### 上傳資料
###### 版本如與 `remote` 有差異會跳**警告**
###### 如**警告**請先同步資料 `pull` or `fetch`

# Git - **pull**
![bg 80% right:70% vertical](../asset/pull3.png)
![bg 70% fit](../asset/pull4.png)
###### = `fetch` + `merge`
###### 下載更新資料
###### **協同作業**期間會不斷執行，確保本地資料有同步更新

# Why need **fetch** ?
- **查看遠端更新**
    不須合併即可檢視遠端修改歷程
- **比對分支差異**
    透過 `diff` 比對，預覽合併結果
- **保持資料同步**
    定期執行，避免合併時大量變更
![bg vertical left:50% fit](../asset/fetch1.png)
![bg left:50% fit](../asset/fetch2.png)

# Git **clone**
![bg right:78% 95%](../asset/clone.svg)

###### 下載Repo
###### 通常**開發之前**執行一次

# Repo **Fork**
![bg left:78% 95%](../asset/fork.svg)

# Git **Sever**/**Service**
###
|[Gitea](https://about.gitea.com/)✅|[Azure DevOps](https://dev.azure.com/)✅|[GitHub](https://github.com/)☑️|[GitLab](https://about.gitlab.com/)|
|-|-|-|-|
|![w:250](../asset/gitea.png)|![w:250](../asset/azuredevops.png)|![w:220](../asset/github.png)|![w:200](../asset/gitlab.png)|
###
>☑️個人練習 / ✅公司使用 (可到 [這裡](http://twoadcode:3000/) 註冊帳號練習，目前未確定何種平台)
<!-- _backgroundColor: #eee; -->

# Dev**Ops**
![bg right:70% fit](../asset/devops2.png)
### Development Operations
##### 一種重視**軟體開發人員**（Dev）和**IT運維技術人員**（Ops）之間溝通合作的文化、運動或慣例

#
![bg 90%](../asset/devops.png)

# **Online** Resources
- https://www.toptal.com/developers/gitignore
- https://heidiliu2020.github.io/git-commit-message/
- https://www.youtube.com/watch?v=0chZFIZLR_0
## **Offline** Resources
- https://www.tenlong.com.tw/products/9789864342662
- https://www.tenlong.com.tw/products/9789865025274
![bg vertical fit right:28%](../asset/book1.png)
![bg vertical fit right:28%](../asset/book2.png)

# What's **next** ...
##
|Subject|Keywords|
|---|---|
|**Work Flow**|`Git Flow` `GitHub Flow` `Other Workflow`|
|**SSDLC**|`OAD Work Flow ?`|
|**Misc.**|`gitignore`|

![bg right:30%](https://picsum.photos/720?image=554)
<!-- _class: invert -->

# Home**work**
- Create a account in [Gitea](http://twoadcode:3000/)
- Create your own remote repo or `fork` [demoGit](http://twoadcode:3000/brian_li/demoGit)
- Clone the remote repo (to local)
- Create a branch `B` with your name
- Make some changes and commit
- Merge `B` into `main`**
- Push to remote*** (only `main` or `B` together)
- Capture screen and mail to [Mecer](mailto:mecer.wu@sgs.com)

> *`fork` = Copy the repo to your own account
**make sure the `HEAD` is pointed on `main`
***version diff warning may appear
![bg left:33%](https://picsum.photos/720?image=83)


# 😀 Thank you !
feel free to ask if you have any other questions.
##
> **OAD** / brian_li / #1429
brian.li@sgs.com
![bg right:60%](https://picsum.photos/720?image=715)
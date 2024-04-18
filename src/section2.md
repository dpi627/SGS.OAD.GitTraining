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
- Why fetch
- Conflict
- Resources
- Homework 2
![bg left](https://picsum.photos/720?image=143)

#
![bg fit 75%](../asset/branch2.png)

# CLI - **Branch**
|指令|中文|簡述|
|---|---|---|
|**branch**|分支|操作分支*|
|**checkout**|簽出|切換指定分支**|
|**merge**|合併|以**目前分支**併吞其他分支|
|**rebase**|重設|看不到合併提交，更簡潔|
###
> *Git 指令永遠都是針對 `目前分支` 進行操作
**`2.23` 之後提供 `switch` 取代 `checkout`
![bg right:30%](https://picsum.photos/720?image=543)

# DEMO - **Branch**
建立分支
```powershell
git branch dev
```
切換分支 (擇一即可)
```powershell
git checkout dev
git switch dev
```
合併分支*
```powershell
git switch main
git merge dev
```
> *⚠️注意當前分支是否為 `main`
![bg left:33%](../asset/ignore.jpg)
<!-- _backgroundColor: #ddd -->

# Git - **merge**
![bg right:70% fit](../asset/merge.png)

# Git - **rebace**
![bg right:70% fit](../asset/rebase.png)

# CLI - **Remote**
##
|指令|中文|簡述|
|---|---|---|
|**remote**|遠端|管理遠端分支*|
|**push**|推送|上傳修改資料到遠端|
|**pull**|拉取|下載修改資料到本地|
|**fetch**|擷取|下載修改資料到**追蹤分支**|
###
> *遠端 `repo` 預設別名為 `origin`
![bg right:33%](https://picsum.photos/720?image=550)

# DEMO - **Remote**
設定遠端 `repo`
```powershell
git remote add origin https://xxx.yyy/zzz.git
```
推送資料*
```powershell
git push -u origin main
```
拉取資料 = `fetch` + `merge`
```powershell
git pull
```
> *設定上游為 `origin/main`，未來 `push` 即可
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
![bg fit](../asset/pull3.png)
![bg fit](../asset/pull4.png)

#
![bg fit](../asset/push1.png)
![bg fit](../asset/push2.png)

# Why need **fetch** ?
- **查看遠端更新**
    不須合併即可檢視遠端修改歷程
- **比對分支差異**
    透過 `diff` 比對，預覽合併結果
- **保持資料同步**
    定期執行，避免合併時大量變更
![bg vertical left:50% fit](../asset/fetch1.png)
![bg left:50% fit](../asset/fetch2.png)

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
|**Git Server**|`GitHub` `Gitea` `GitLab` `Azure DevOps`|
|**Work Flow**|`Git Flow` `GitHub Flow` `OAD Flow?`|
|**CI/CD**|`Action` `Pipline` `yaml`|
|**AI**|`GitHub Copilot CLI` `Commit Message Generator`|
|**Misc.**|`Pull Request` `Code Review`|

![bg right:24%](https://picsum.photos/720?image=555)
<!-- _class: invert -->

# Home**work** 2
- Create a account in [Gitea](http://twoadcode:3000/)
- Back to the local repo
- Create a branch `B` with your name
- Add content and then commit
- Merge `B` into `main`
- Push to remote* (only `main` or `B` together)
- Capture screen and mail to [Mecer](mailto:mecer.wu@sgs.com)
###
> *version diff warning may appear
![bg left:20%](https://picsum.photos/720?image=83)

# 😀 Thank you !
feel free to ask if you have any other questions.
##
> **OAD** / brian_li / #1429
brian.li@sgs.com
![bg right:60%](https://picsum.photos/720?image=715)
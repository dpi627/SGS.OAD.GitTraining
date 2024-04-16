---
marp: true
paginate: true
headingDivider: 1
---

# 
![](asset/gitlogo.png)
![bg right:33%](asset/log.jpg)

```powershell
git --distributed-even-if-your-workflow-isnt
```
##
> **OAD** / brian_li

# **A**genda
- What's Git
- CLI and GUI
- local and remote
- Resources
![bg left](https://picsum.photos/720?image=20)

# **名詞**解釋
![bg left:33%](asset/github.jpeg)
|名詞|簡述|
|---|---|
|**Git**|一種分散式「**版本控制**」|
|**GitHub**|一個提供多種服務的「**網站**」|
|**Repository**|儲存庫、程式庫，簡稱 `repo`|
|**Branch**|分支，一個 `repo` 可能包含多個分支|
|**CLI**|Command Line Interface，例如 CMD|

# 
![bg 120%](asset/novc.png)
![bg fit](asset/aftervc.png)

# **CLI** - Command Line Interface
###
|CMD|Git Bash|Terminal✅|VS2022|VSCode|ADS|
|-|-|-|-|-|-|
|![w:200](asset/cmd.png)|![w:200](asset/gitbash.png)|![w:150](asset/terminal.png)|![w:100](asset/Visual_Studio_Icon_2022.svg.png)|![w:100](asset/vscode.png)|![w:100](asset/ads.jpg)|
###
>後面三項常用開發工具也有內建CLI可以使用，✅表示筆者常用
熟悉指令對後續操作有幫助，建議從指令開始學習

# CLI - **Repository**
##
|指令|中文|簡述|
|---|---|---|
|**init**|初始化|在 `local` 建立 `repo` 與預設分支*|
|**status**|狀態|檢視目前 `repo` 狀態|
|**clone**|複製|下載整個 `remote repo` 到 `local`|
###
> *[為免歧視](https://www.ithome.com.tw/news/140094)，預設分支後來由 `master` 改為 `main`
![bg right:33%](https://picsum.photos/720?image=609)

# DEMO - **Repository**
本地初始化
```powershell
git init
```
```powershell
git status
```
下載遠端 `repo`
```powershell
git clone https://xxx.yyy/zzz.git
```
![bg left:33%](asset/ignore.jpg)
<!-- _backgroundColor: #ddd -->

# Repository **.git**
- `git init` 之後產生
- 儲存 Git 相關資料
    - commits
    - branches
    - tags
    - remotes
    - index
    - config files
![bg right:60% 110%](asset/reset.png)

#
![bg 90%](asset/status.png)

# CLI - **File**
##
|指令|中文|簡述|
|---|---|---|
|**add**|加入|將檔案加入暫存區，準備提交(尚未提交)|
|**commit**|提交|提交修改*至 `repo`，需填寫提交內容|
|**log**|歷程|檢視** `repo` 歷程記錄|
###
> *每次 `commit` 都會生成一個 `hash code`，例如 `c802b33`
**離開檢視請按 `q`，或者利用參數縮小範圍
![bg right:25%](https://picsum.photos/720?image=579)

# DEMO - **File**
暫存區加入特定或全部 `untracked` 檔案
```powershell
git add code.txt
git add .
```
提交修改
```powershell
git commit -m "my first commit"
```
檢視歷程
```powershell
git log
git log --oneline --graph
```
![bg left:33%](asset/ignore.jpg)
<!-- _backgroundColor: #ddd -->

# Git - **HEAD**
- Git 的指標(指針)
- 指向當前 `branch`
- 或指向最新 `commit`
- 可搭配 `~n` 與 `^n`
- 許多指令都與 `HEAD` 有關，例如 `checkout` `merge` `rebase` `reset` `status` `log` ...等
![bg fit right:60%](asset/head.png)

# CLI - **Branch**
##
|指令|中文|簡述|
|---|---|---|
|**branch**|分支|建立分支，需提供分支名稱|
|**checkout**|簽出|切換到指定分支，需提供分支名稱|
|**switch**|切換|同上，於 `Git 2.23` 後提供|
|**merge**|合併|以目前分支***併吞**其他分支|
###
> *⚠️Git 指令永遠都是針對 `目前分支` 進行操作
![bg right:33%](https://picsum.photos/720?image=543)

# DEMO - **Branch**
建立分支
```powershell
git branch dev
```
切換分支
```powershell
git checkout dev
git switch dev
```
合併分支 
```powershell
git swtich main
git merge dev
```
> ⚠️注意當前分支是否為 `main`
![bg left:33%](asset/ignore.jpg)
<!-- _backgroundColor: #ddd -->

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

# Git - **Tracking** Branch
- 與遠端分支關聯的**本地分支**
- `origin` = 遠端 `repo`
- `origin/main` = 遠端 `main` 的追蹤分支
- 追蹤分支**僅**用來反映其遠端分支變化
- 關於遠端的**操作***會影響追蹤分支
- **無法**直接操作追蹤分支
###
> *例如 `clone` `push` `pull` `fetch` 等
**左為 `ftech` 示意，僅更新追蹤分支
![bg vertical left:44% fit](asset/fetch3.png)

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
![bg left:33%](asset/ignore.jpg)
<!-- _backgroundColor: #ddd -->

# Why need **FETCH** ?
- **查看遠端更新**
    不須合併即可檢視遠端修改歷程
- **比對分支差異**
    透過 `diff` 比對，預覽合併結果
- **保持資料同步**
    定期執行，避免合併時大量變更
![bg vertical left:50% fit](asset/fetch1.png)
![bg left:50% fit](asset/fetch2.png)

# **GUI** - Graphic User Interface
###
|[TortoiseGit](https://tortoisegit.org/)|[GitHub Desktop](https://desktop.github.com/)|[Sourcetree](https://www.sourcetreeapp.com/)✅|VS2022|VSCode|ADS|
|-|-|-|-|-|-|
|![w:200](asset/tortoise.png)|![w:200](asset/githubdesktop.png)|![w:150](asset/sourcetree.png)|![w:100](asset/Visual_Studio_Icon_2022.svg.png)|![w:100](asset/vscode.png)|![w:100](asset/ads.jpg)|
###
>各 GUI 操作邏輯不同，支援指令、功能也略有不同，但底層 Git 指令都是一樣的
可能有自訂功能例如 `Sync` = `push` + `pull` 或 `Publish` = `remote` + `push`

# 取消提交

# Online **Resources**
- https://learngitbranching.js.org/?locale=zh_TW
- https://www.toptal.com/developers/gitignore
- https://heidiliu2020.github.io/git-commit-message/
- https://kingofamani.gitbooks.io/git-teach/content/
- https://jlord.us/git-it/index-zhtw.html
### **Offline** Resources
- https://www.tenlong.com.tw/products/9789864342662
- https://www.tenlong.com.tw/products/9789865025274
![bg vertical fit right:20%](asset/book1.png)
![bg vertical fit right:20%](asset/book2.png)

# Home**work**
- Install* Git from https://git-scm.com/download/win
- Install* GUI or CLI
- Clone the repo http://twoadcode:3000/brian_li/demoGit.git
- Create your own directory `D`
- Create a text file `T` in `D`
- Write something in `T` and save
- Add `T` to the stage
- Commit
- Capture screen and mail to [Mecer](mailto:mecer.wu@sgs.com)
##
> *probably need IT support
![bg left:20%](https://picsum.photos/720?image=537)

# What's **next** ...
##
|Git Server|AI|CI/CD|Workflow|misc.|
|---|---|---|---|---|
|Gitea|GitHub Copilot CLI|Action|Git Flow|Pull Request|
|GitHub|Commit Generator|Pipline|GitHub Flow|Code Review|
|Azure DevOps||YAML|Our Flow ?||
<!-- _class: invert -->

# 😀 Thank you !
feel free to ask if you have any questions.
##
> **OAD** / brian_li / #1429
brian.li@sgs.com
![bg right:60%](https://picsum.photos/720?image=505)
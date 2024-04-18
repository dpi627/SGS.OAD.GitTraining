---
marp: true
paginate: true
headingDivider: 1
footer: git-section-`00`
---

# 
![](asset/gitlogo.png)
```powershell
git --section 00 -msg "before we start" :)
```
##
> **OAD** / brian_li
![bg right:33%](asset/log.jpg)

# **A**genda
- Version Control
- What's Git
- CLI / GUI
- Resources
![bg left](https://picsum.photos/720?image=20)

# **名詞**解釋
|名詞|簡述|
|---|---|
|**Git**|一種分散式「**版本控制**」|
|**GitHub**|一個提供多種服務的「**網站**」|
|**Repository**|儲存庫、程式庫，簡稱 `repo`|
|**Branch**|分支，一個 `repo` 可包含多個分支|
|**CLI**|Command Line Interface，例如 CMD|

![bg left:33%](asset/github.jpeg)

# 
![bg fit 90%](asset/novc.png)

#
![bg fit](asset/aftervc.png)

#
![bg fit 90%](asset/commit.png)

#
![bg fit 60%](asset/repo.png)

#
![bg fit 75%](asset/branch2.png)

#
![bg fit 75%](asset/gitflow.png)

# **CLI** - Command Line Interface
|CMD|Git Bash|Terminal✅|VS2022|VSCode|ADS|
|-|-|-|-|-|-|
|![w:200](asset/cmd.png)|![w:200](asset/gitbash.png)|![w:150](asset/terminal.png)|![w:100](asset/Visual_Studio_Icon_2022.svg.png)|![w:100](asset/vscode.png)|![w:100](asset/ads.jpg)|
###
>✅表示個人常用，後面三種開發工具也有內建CLI
熟悉指令對學習 Git 十分有幫助，建議從指令開始了解
<!-- _backgroundColor: #eee; -->

# **GUI** - Graphic User Interface
|[TortoiseGit](https://tortoisegit.org/)|[GitHub Desktop](https://desktop.github.com/)|[Sourcetree](https://www.sourcetreeapp.com/)✅|VS2022|VSCode|ADS|
|-|-|-|-|-|-|
|![w:200](asset/tortoise.png)|![w:200](asset/githubdesktop.png)|![w:150](asset/sourcetree.png)|![w:100](asset/Visual_Studio_Icon_2022.svg.png)|![w:100](asset/vscode.png)|![w:100](asset/ads.jpg)|
###
>各 GUI 操作邏輯、功能略有不同，但底層一樣都是 Git 指令
GUI 有自訂功能例如 **`Sync`** ≈ `pull` + `push` 或 **`Publish`** ≈ `remote` + `push`
<!-- _backgroundColor: #eee; -->

#
![bg](asset/ios1.jpg)
---
marp: true
paginate: true
headingDivider: 1
---
# 
![](asset\gitlogo.png)
![bg right:33%](asset\log.jpg)

```sh
git --distributed-even-if-your-workflow-isnt
```
##
> **OAD**
>brian_li

# **常見**專有名詞
![bg left:33%](asset\github.jpeg)
|名詞|簡述|
|---|---|
|**Git**|一種分散式「**版本控制**」|
|**GitHub**|一個提供多種服務的「**網站**」|
|**Repository**|儲存庫、程式庫，簡稱 `repo`|
|**Branch**|分支，一個 `repo` 可能包含多個分支|
|**CLI**|Command Line Interface|

# 
![bg 120%](asset\novc.png)
![bg fit](asset\aftervc.png)

# CLI - **基本操作**
##
|指令|中文|簡述|
|---|---|---|
|**init**|初始化|建立 `repo` 與預設分支|
|**status**|狀態|檢視目前 `repo` 狀態|
|**add**|加入|將檔案加入暫存區|
|**commit**|提交|提交修改至 `repo` |
##
> 預設分支於 2020 後陸續由 `master` 改為 `main`

# CLI - **分支**(Branch)
##
|指令|中文|簡述|
|---|---|---|
|**branch**|分支|建立分支|
|**checkout**|簽出|切換指定分支|
|**switch**|切換|同上，於 Git 2.23 後支援|
##
> ⚠️ Git 操作永遠都是針對當下分支

# Commit Template

```
#1 {內容摘要} 12345 需求修改
#2 {一行空白}
#3 {內容描述} 修改了 xxx 和 yyy
```

# 取消提交
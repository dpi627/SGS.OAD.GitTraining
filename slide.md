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
# 常見名詞
|名詞|簡述|
|---|---|
|Git|一種分散式版本控制|
|GitHub|提供多種服務的網站|
|Repository|儲存庫、程式庫，簡稱 `repo`|

# 常見指令
|command|中文|簡述|
|---|---|---|
|init|初始化|建立repo|
|add|加入|將檔案加入暫存區|
|commit|提交|提交修改至repo|
|revert|復原|復原某個版本紀錄|
|branch|分支|建立分支|
|checkout|簽出|切換到指定分支|

| Git 2.23 版本後支援 `switch`，更為直覺
# Commit Template

```
#1 {內容摘要} 12345 需求修改
#2 {一行空白}
#3 {內容描述} 修改了 xxx 和 yyy
```

# 取消提交
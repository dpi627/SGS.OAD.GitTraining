---
marp: true
paginate: true
footer: git-`quickstart`
---

![bg left](https://picsum.photos/720?image=893)

##### ![](../asset/gitlogo.png) Qucik Start
###
```bat
git quick-start "from zero to git" ✨
```
###
`OAD` **Brian Li**

---

![bg right](https://picsum.photos/720?image=829)

## **適合**對象

- SGS Taiwan 同仁
- 幾乎或不曾使用過 Git
- 工作上需要進行版本控制

## 預期**目標**

- 最快速度了解以下項目
- ![h:30](/asset/sourcetree.png) **Sourcetree** 基礎操作
- ![h:25](/asset/gitea.png) **Gitea** 基礎功能使用

---

![bg left](https://picsum.photos/720?image=820)

# **A**genda
  
- ![w:30](../asset/giticon.png) **Git**
  基礎知識
  常見指令

- ![w:30](../asset/sourcetree.png) **Sourcetree**
  安裝流程
  基礎操作

- ![w:30](../asset/gitea.png) **Gitea**
  功能分享
  建立儲存庫

---

![bg 50% left:40% vertical](../asset/gitlogo.png)
![bg 70%](../asset/github-text.png)
![bg 60%](../asset/gitea-text.png)

## **Git**

- 一套開源的分散式版本控制軟體
- 本地安裝即可使用

## **GitHub**

- 一個提供多種服務的網站
- 需要註冊方可使用

## **Gitea**

- 開源專案，功能與 GitHub 雷同
- 可於封閉網路環境部署，適合企業使用

---

![bg fit 90%](../asset/allarea.png)

---

![bg right vertical](https://fakeimg.pl/960/?text=status)
![bg](https://fakeimg.pl/960/999/ddd/?text=add)
![bg](https://fakeimg.pl/960/?text=commit)

# **Local** 相關常見指令

```sh
# 初始化 local repo (首次執行)
git init

# 查看 local repo 狀態
git status

# 將所有 unstaged 檔案加入 stage
git add .

# 提交(commit)修改到 local repo
git commit -m "{message}"
```
###
>`repo`全名為 Respository，也可稱為儲存庫 (不限定只能放程式)

---

![bg left vertical](https://fakeimg.pl/960/999/ddd/?text=clone)
![bg](https://fakeimg.pl/960/?text=pull)
![bg](https://fakeimg.pl/960/999/ddd/?text=push)

# **Remote** 相關常見指令

```sh
# 下載 remote repo (首次執行)
git clone {htt://url/repo.git}

# 拉取 remote repo 提交紀錄
git pull

# 推送 local 提交記錄至 remote
git push
```

###

- 擷取 `fetch` 也是一個重要指令
- 追蹤分支 `Tracking Branch` 觀念可一起進行了解

---



---
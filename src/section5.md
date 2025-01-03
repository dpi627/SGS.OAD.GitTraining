﻿---
marp: true
paginate: true
headingDivider: 1
footer: git-section-`05`
---

# 
![bg right:33%](https://picsum.photos/720?image=128)
![](../asset/gitlogo.png)
```powershell
git --section 05 -cicd "github actions" :/
```
##
> **OAD** / brian_li

# **A**genda
![bg left:60%](https://picsum.photos/720?image=196)
- CI/CD
- Gitea Actions
    Runner
    YAML
- Demo
- Resources

# CI **/** CD - 持續整合 **/** 部署
![bg right:25%](https://picsum.photos/720?image=296)
###### 一種軟體開發實踐方法，目的在**自動化**和**簡化**開發、測試和部署**過程**
###
- 持續**整合**（Continuous Integration）：
    程式碼頻繁地合併到 repo
    每次合併自動觸發測試和建置流程
- 持續**部署**/交付（Continuous Deployment/Delivery）
    自動化部署程式碼到測試或正式環境
    持續交付軟體更新至使用者

#
![bg 90%](../asset/cicd2.png)

# CICD **Flow** & **Result**
![bg vertical 50%](../asset/cicd.svg)
![bg vertical 100%](..//asset/cicd_result.png)

# Gitea Actions **Act Runner**
![bg left:60% fit](../asset/cicd.png)
- 用於執行**工作流程**
- 可以是**虛擬機**、**實體機**或者**容器**
- 官方有提供，也可自建
- 獨立專案，Go 撰寫

# Gitea **Actions**
![bg right:65% 95%](../asset/actions.svg)
- 致敬
    [GitHub Actions](https://docs.github.com/en/actions)
- 大部分相容
- 使用 **YAML** 撰寫
###
⚠️`yaml` 可放路徑 `.gitea/workflows/` `.github/workflows/`


# YA**ML**
![bg right fit](../asset/yaml.png)
###### **Y**et **A**nother **M**arkup **L**anguage
- key-value pair 集合
- value 可以是字串或結構
- 結構使用縮排定義
- 不可以用 **Tab**
- 子節點比父節點縮排更多即可，空白數量**不**重要
- 支援 UTF-8, UTF-16 and UTF-32

#
![bg fit](../asset/yaml_json.png)
<!-- _class: invert -->

# SimpleAction.**yaml**
![bg left:33%](https://picsum.photos/720?image=400)
```yaml
name: Greetings!  ------------ # workflow name

on: [push, pull]  ------------ # event(s)

jobs:
  Greeting:  ----------------- # job id**
    runs-on: windows  -------- # runner label***
    steps:   ----------------- # action(s)
      - name: Say Hello   ---- # action name*
      - run: echo Hello!  ---- # run script
```

>*`name` is optional
**`job id` must be unipue
***`runs-on` should match the runner `label`

# Gitea Actions **Variables**
![bg right:33%](https://picsum.photos/720?image=411)

- 共用變數可儲存於 **Variables**
- 說明請參考 [官方文件](https://docs.gitea.com/usage/actions/actions-variables)
- 新增 `FIRST_NAME` = `Brian`
- 取用 `${{ vars.FIRST_NAME }}`
###
```yaml
run: echo "My first name is ${{ vars.FIRST_NAME }}."

# My first name is Brian.
```

# Gitea Actions **Secrets**
![bg left:33%](https://picsum.photos/720?image=426)

- 機密資訊則儲存於 **Secrets**
- 說明請參考 [官方文件](https://docs.gitea.com/usage/secrets)
- 新增 `LAST_NAME` = `****` (儲存後即隱藏)
- 取用 `${{ secrets.LAST_NAME }}`
###
```yaml
run: echo "My last name is ${{ secrets.LAST_NAME }}."

# My last name is ****.
```

# DEMO
![bg right:60% vertical](https://picsum.photos/720?image=744)
- Actions Enable ?
- Runner Statuds
- Create Workflow
- Push
- Review Result

# **Online** Reources
![bg left:35%](https://picsum.photos/720?image=744)
- [Gitea Actions](https://docs.gitea.com/usage/actions/overview)
- [GitHub Actions](https://docs.github.com/en/actions)

| [動手學GitHub!](https://www.books.com.tw/products/0010926249)|[AzureDevOps顧問實戰](https://www.books.com.tw/products/0010921349) |
|-|-|
|![w:200](../asset/book4.png)| ![w:180](../asset/book3.png)|

# 😀 Thank you !
![bg right:60%](https://picsum.photos/720?image=669)
feel free to ask if you have any other questions.
##
> **OAD** / brian_li / #1429
brian.li@sgs.com
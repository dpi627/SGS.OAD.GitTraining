![](https://img.shields.io/badge/Git-555?logo=git)
![](https://img.shields.io/badge/gitignore-555?logoColor=999&logo=gitignore.io)
![](https://img.shields.io/badge/Gitea-555?logo=gitea)
![](https://img.shields.io/badge/Sourcetree-666?logoColor=0052CC&logo=sourcetree)
![](https://img.shields.io/badge/Markdown-555?logoColor=000&logo=markdown)
![](https://img.shields.io/badge/Explorer-555?logoColor=FAB70C&logo=googledocs)
![](https://img.shields.io/badge/Subversion-555?logo=subversion)
![](https://img.shields.io/badge/video-CC0000?logo=airplayvideo)

# 🔍版控使用情境

在使用版控的時候，常見有以下兩種情境

|類型|說明|適合|
|-|-|-|
|`origin-first`|在遠端初始化儲存庫後下載至本機|新專案|
|`project-first`|在本機初始化儲存庫後推送至遠端|舊專案|

## ⚠️常見情境多為 `project-first`

- 上述兩種狀況名稱 `origin-first` `project-first` 為自行定義，如果沒看過很正常
- 大部分狀況可能都是已存在舊專案，即 `project-first`，先有專案才加入版控
- 以下針對此類型進行操作說明補充，建立一個示範專案，再加入版控

---

# ➡️示範專案說明

- 使用 Visual Studio 建立一個 Console Protject，名為 `demoEmpty`
- 於方案加入一個 Class Library Project，名為 `demoEmpty.Util`
- `demoEmpty` 加入 `demoEmpty.Util` 參考，也加入 `NuGet` 套件
- 編譯並發布 `demoEmpty`，並手動加入少許 `log`，產出一些額外檔案
- 方案預設已使用 Subversion 版控 (即根目錄下存在 `.svn` 資料夾)

## 🗃️方案目錄

```powershell
📂demoEmpty
  📁.svn    #---------------------- ignore must
  📁.vs     #---------------------- ignore must
  📁demoEmpty
    📁bin   #---------------------- ignore must
    📁log   #---------------------- ignore suggest
    📁obj   #---------------------- ignore must
    📁Properties    #-------------- ignore suggest
    📄demoEmpty.csproj
    📄demoEmpty.csproj.user #------ ignore must
    📄Program.cs
  📁demoEmpty.Util  #-------------- same as above
  📄demoEmpty.sln
```

- 備註部分不需加入版控，版控以程式碼為主即可
- 忽略檔案表示可能會影響協作或根本與版控無關
- 建議使用 [gitignore.io](https://gitignore.io/) 生成 `.gitignore`

>⚠️如有系統文件可考慮納入版控，主要仍以專案程式原始碼為主即可

---

# 📜Project First 流程說明

|操作環境|項目|示範影片|補充說明|
|-:|-|-|-|
| ![](https://img.shields.io/badge/Gitea-555?logo=gitea) |建立空的遠端儲存庫| [![](https://img.shields.io/badge/video-CC0000?logo=airplayvideo)](../asset/video/net-remote-create-empty-repo.mp4) |
| ![](https://img.shields.io/badge/Explorer-555?logoColor=FAB70C&logo=googledocs) |方案加入 `.gitignore`| [![](https://img.shields.io/badge/video-CC0000?logo=airplayvideo)](../asset/video/net-add-git-ignore.mp4) | 使用[網站](https://gitignore.io/) 生成 `.gitignore`
| ![](https://img.shields.io/badge/Explorer-555?logoColor=FAB70C&logo=googledocs) |方案加入 `readme.md` <sup>[*1](#memo1)</sup> | [![](https://img.shields.io/badge/video-CC0000?logo=airplayvideo)](../asset/video/net-add-readme.mp4) | 建議學習 `Markdown` 語法
| ![](https://img.shields.io/badge/Sourcetree-666?logoColor=0052CC&logo=sourcetree) |初始化本地儲存庫| [![](https://img.shields.io/badge/video-CC0000?logo=airplayvideo)](../asset/video/net-create-local-repo.mp4) | 會提示路徑已存在 <sup>[*2](#memo2)</sup>
| ![](https://img.shields.io/badge/Sourcetree-666?logoColor=0052CC&logo=sourcetree) |本地儲存庫提交版控| [![](https://img.shields.io/badge/video-CC0000?logo=airplayvideo)](../asset/video/net-init-commit.mp4) | 提交初次加入的檔案
| ![](https://img.shields.io/badge/Gitea-555?logo=gitea) ![](https://img.shields.io/badge/Sourcetree-666?logoColor=0052CC&logo=sourcetree) |本地儲存庫加入遠端| [![](https://img.shields.io/badge/video-CC0000?logo=airplayvideo)](../asset/video/net-add-remote.mp4) | 即加入 `origon` |
| ![](https://img.shields.io/badge/Sourcetree-666?logoColor=0052CC&logo=sourcetree) ![](https://img.shields.io/badge/Gitea-555?logo=gitea) |推送提交，並於遠端檢視| [![](https://img.shields.io/badge/video-CC0000?logo=airplayvideo)](../asset/video/net-push.mp4) | 初次推送需要進行驗證 <sup>[*3](#memo3)</sup> |

<a id="memo1"><sup>*1 加入 `readme.md` 非必要步驟，但能加入更好</sup></a>
<br>
<a id="memo2"><sup>*2 初始化儲存庫時，如果路徑已經存在會顯示警告，繼續執行即可</sup></a>
<br>
<a id="memo3"><sup>*3 初次推送遠端儲存庫會進行驗證，之後推送就不需要了</sup></a>

---

# 📎補充資料

- [有些檔案我不想放在 Git 裡面...](https://gitbook.tw/chapters/using-git/ignore)
- [線上生成忽略檔 - gitignore.io](https://gitignore.io/)
- [Markdown 語法說明](https://markdown.tw/)
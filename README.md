# Git 學習記錄

- 學習連結:
    
    [https://www.youtube.com/watch?v=NugoF40e6Dk](https://www.youtube.com/watch?v=NugoF40e6Dk)
    
    [https://www.youtube.com/watch?v=MJUJ4wbFm_A&t=655s](https://www.youtube.com/watch?v=MJUJ4wbFm_A&t=655s)
    
    [https://www.youtube.com/watch?v=eulnSXkhE7I](https://www.youtube.com/watch?v=eulnSXkhE7I)
    
    [https://github.com/MuhammedBuyukkinaci/My-Git-Notes/blob/master/README.md](https://github.com/MuhammedBuyukkinaci/My-Git-Notes/blob/master/README.md)
    

### 基礎/常見 Git 指令

- 初始化
    - `git init`
    - 簡單來說, 就是在專案資料夾下建立一個隱藏資料夾(.git)來管理所有版本相關資訊
- 觀察Repository檔案狀況
    - `git status`
    - 確認該檔案夾下所有git狀況, 就是去看隱藏資料夾(.git)的內容
    - 如果該路徑下無.git資料夾, 就會顯示提示”not a git repository”

- 將檔案加入追蹤(index)清單
    - `git add <. or file name>`
    - .表示所有
    - 將該路徑下所有檔案加入git 追蹤清單, 但還非管理版本步驟
    - tells git to include the file in the next revision to the repository
- 建立一組版本記錄&更新
    - `git commit -m <message>`
    - Actually make the save.
    - 如果想 add + commit in the same time
        - `git commit -am <message>`   

---

- 上傳本機專案記錄到遠端 or github相關
    - 查詢本機端專案(Repository)是否上遠端
        - `git remote -v`
    - Link遠端的Repository url
        - `git remote add <遠端空間命名(一般用[origin])> <網址>`
        - 協作時, 普遍認為origin才是原始的
  
    - 上傳到github 雲端專案空間
        - `git push <遠端空間的名稱> <遠端空間的分支>`
---

- 下載github遠端專案到本機
    - 第一次下載github 雲端專案
        - `git clone <遠端空間的網址(URL)> <本機資料夾名稱>`
        - Notes: 若是clone下來的專案, 本機會自己設定該remote的狀態
    - 從github 雲端專案下載合併更新
        - `git pull <遠端空間的名稱> <遠端空間的分支>`
        - 記得如果協作專案, 第一件事是將遠端程式碼pull到本地進行最新版本更新
- 衝突處理(merge conflicts)
    - 當本機端或遠端進行合併時, 可能出現衝突, 需人為確認並修正, 重新add&commit後在push上遠端
    - 當分支版本進行合併時, 亦可能發生, 處理方式與上述雷同
    - git 一般來說只會檢視同一行的修正衝突, 邏輯衝突無法顯著警告, 合併後需特別注意執行結果

---

- 查看分支(branch)
    - `git branch`
- 建立新分支(branch)
    - `git branch <branch_name>`
- 切換到特定分支(branch)
    - `git checkout <branch_name>`
    - 建立與切換一同執行
        - `git checkout -b <branch_name>`
- 合併指定分支與現在所在位置的分支
    - `git merge <branch_name>`
    
- Pull request
    - GitHub上有”Compare & pull request” 提供特定人員檢驗分支是否可合併功能
       
- 刪除特定分支
    - `git branch -D <branch_name>`

---

- 回到先前版本
    - `git reset - - hard <commit_hash>`
    - `git reset - - hard origin/master(or any brench)`
    - 只要執行就會回去原先的version, 之後的變動皆會消失, 需特別注意使用

---

### 其他常用確認用

- 確認差異
    - `git diff`
- 顯示所有commits and messages 歷史
    - `git log`

---

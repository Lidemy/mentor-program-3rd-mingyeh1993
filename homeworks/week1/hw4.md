## 跟你朋友介紹 Git

菜哥，我先簡單介紹一下 Git 吧，Git 其實就是一個版本控制系統，何謂版本控制呢？
：「當一個系統有非常多的版本時，就需要版本控制使用來了解每一版的差異，其實 Git 的蓋念大家都有，以我們最常做的報告來說，一修再修的強況下也造就出許多不一樣的版本，版本號的差異能清楚知道這是第幾版的資料。」

***版本控制除了單人使用外，在多人協作下也能使用版本控制。***

##  介紹簡單操控的指令

* 指令 git init ：git 開始前的初始化的必要動作， git 開始可以掌控這個資料夾
* 指令 git add ：增加檔案到 git 做版本控制
git add 主要分兩個區塊：
1. staged 加入版本控制，再上欄版本控制列中
2. untracked 不加入版本控制，在下欄非屬版本控制檔案
如果不想一個一個加直接輸入指令， git add . ，全部資料夾檔案皆進入版本控制列中。
* 指令 git commit ：新建一個版本
git commit -m(你要的messenge，跟此版本有關的敘述) “xxxyyy”
* 指令 git log：查看任何變動過的歷史紀錄
修改檔案後必須再將黨加入版本控制 git add xxx
然後再 git commit -m “xxx”>git log即可看到修改的歷史紀錄
如果希望 git log顯示簡短一些可輸入 git log －－oneline
* 指令git checkout：回到過去，回到任一版本的狀態
git log後選定版本名稱>git checkout + 選定的名稱後就回到那一版本
如果想回到原本狀態只要輸入 git checkout master就好
* 指令 .gitignore：忽略不想加入版本控制的檔案
步驟 touch .gitignore > vim .gitignore > i 輸入想忽略的檔案後 : q 後就存在裡面了。
另補充修改檔案新增commit組合技
(git add xxx>git commit -m “xxx”)可合併成 git commit -am “xxx” 這樣就不需輸入兩次指令！

##  Git 的分支， branch

###  為什麼需要 branch

commit 的版本屬於線性式的方式，如果舊版本有 bug 需要 fix 時，剛開發的新版本卻又還無法上線，就需要加入 branch 也就是版本分支，以兩個不同檔案分開進行，直到最後兩條分支在最後完成時完美的合而為一。
* git branch -v：新增一個 branch ，git branch -v xxx，刪除一個branch也很簡單 git branch -d xxx即可
* git checkout ：任意轉換到任何 branch，git checkout xxx
* git merge：合併分支，應注意是要merge到哪個版本，通常是master，可先用 git branch -v 來查詢位置後將要merge的版本使用此指令 git merge xxx
* 解決衝突：可用手動修改，進入 vim 後修改一致之後即可 merge 在一起

##  git 狀況題

* git commit --amend ：進入後可修改打錯的commit messenge
* git checkout ：修改的檔案又不想 commit 的話可使用 git checkout — xxx 或是 git checkout — .就好
* git branch -m ：branch 名稱打錯修改的方式 git branch -m xxxx即可修改

##  Github 的 Pull & Push 

* git push origin XXX ( branch 名稱)，將分支傳上 Github
* git pull origin XXX ( branch 名稱)，將分支下載到 local 端


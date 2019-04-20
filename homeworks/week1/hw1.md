#  hw1：交作業流程 
1.  養成的第一個習慣，一定要在新的 branch 上寫作業，branch 名稱用 week 1，往後作業名稱依此類推。 
2.  Checkout 到 week 1 這個branch，必須確保自己不是在 master 這個 branch 上寫作業。 
3.  作業做完或是修改後， commit -am ‘xxx’ 後 git push origin week1 ，把這個branch 推到 github平台上。 
4.  Push 上去後，github 頁面上會秀出 Your recently pushed branches ，接著直接點 compare & pull request。 
5.  之後就可以看到 base:master 、compare:week1 ，開始打標題，可以隨便打，或是制式的打法 ‘作業week1’之類的，順便可以在內容中打想問的問題，最後按出 pull request。 
6.  之後複製上面步驟的網址到 homeworks-3rd 上交作業，開一個新的 Issues，標題的部分格式為固定 [Week1] ，注意大小寫，如果打錯會被系統擋掉 
7.  順利交出作業後，老師如果覺得作業 OK ，就會 merge 後會把我的 branch 關掉還有 issues 給關掉，如果看到 issues 被關掉，代表作業 ok 了。 
8.  如果作業需修改，老師會先把這版的 branch 給 merge，所以一樣再回到第一步開一個新的branch 修改後再交上來。 
9.  最後的最後作業都沒問題了，回到 git checkout master 將 github 最新版本 git pull origin master 拉下來，再把原本 week1 的 branch 刪除 ，使用 git branch -d week1 後 git branch 確認是不是只剩一個 branch 就大功告成了！ 
------------------------------------------- 
**以上九點為交作業流水帳，之後只剩熟悉它就好**  


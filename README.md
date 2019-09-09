# Git_Guide
1, 基本操作:
git add file1: 将file1添加到Git本地仓库中
git commit -m "添加基本操作": 添加本次提交的注释信息
git push ： 提交本地的更新到远程仓库

2，修改最近的提交
git log --pretty=one -10： 将每次提交日志缩略为1行，总共倒序显示10条最近提交的记录
git reset --soft xxxxx(某次提交序列): 指向想要回滚到的某次提交，此时已提交到github的内容也会重新在本地显示为编辑中
git push -f: 强制覆盖前面的提交记录

3，git merge upstream/master: 将upstream仓库的master分支合入当前分支
4, git stash save "message": 将当前修改的内容暂停保存到存储栈中，然后回到修改前
   git stash list： 显示保存到栈的所有内容列表
   git stash pop： 将栈顶保存的内容显示出来进行继续编辑



# Git_Guide
1, 基本操作:

```git add file1: ``` 将file1添加到Git本地仓库中

```git commit -m "添加基本操作"``` 添加本次提交的注释信息

```git push``` 提交本地的更新到远程仓库

2，修改最近的提交

```git log --pretty=one -10``` 将每次提交日志缩略为1行，总共倒序显示10条最近提交的记录

```git reset --soft commitId``` 指向想要回滚到的某次commitId提交，此时已提交到github的内容也会重新在本地显示为编辑中

```git push -f``` 强制覆盖前面的提交记录

3，```git merge upstream/master``` 将upstream仓库的master分支合入当前分支

4, ```git stash save "message"``` 将当前修改的内容暂停保存到存储栈中，然后回到修改前
   
   ```git stash list``` 显示保存到栈的所有内容列表
   
   ```git stash pop``` 将栈顶保存的内容显示出来进行继续编辑

5, 我们通常使用标签来标注我们的每一次版本更新
	
   5.1 为我们的某一次提交添加标签
   
	git tag -a v0.1 -m "test v0.1标签" fe8bc56089f110d01874548a175915ecb70f926b
	
   其中-a表示指定标签名，-m表示备注，fe8bc56089表示我们的提交commit的id
   
   5.2 还没有提交到远程分支，但是发现标签填写错了？不用担心,比如删除未提交的v0,3分支
	
	    $ git tag -d v0.3
	    Deleted tag 'v0.3' (was 6099176)
    
   5.3 将v0.1标签推送到远程仓库中：
    	
    	git push origin v0.1
   或 将所有标签一次性全部推送到远程仓库：
        
        git push origin --tags

   5.4 发现推送到远程仓库的标签vo,2打错了肿么办？
    	首先删除本地的标签:
    	
    	git tab -d vo,2
   然后删除远程仓库的标签(注意origin与:refs之间有要空格):
    	
    	$ git push origin :refs/tags/vo,2
		To github-dailyplanner.com:dailyplanner/Git_Guide.git
 		- [deleted]         vo,2



欢迎关注补充或提交想要了解的更多关于Git的问题, 持续更新中......
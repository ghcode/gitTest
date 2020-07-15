# git 笔记
## 概念

>* 特性分支
>* 远程追踪分支



## 命令

>
>
>```java
>/*
>	git init
>	git log
>		-1[2|3|....]
>		--pretty=option,option可取的值
>          short
>          oneline
>        --abbrev-commit
>        since..until  提交范围
>		
>			
>		
>	git show
>		分支名:文件名 显示文件内容
>		
>	git show-branch:以时间降序的形式列出一个或多个分支的提交列表
>		-a
>		-r
>	git rev-parse
>	git rev-list
>	git merge-base
>	git merge
>		分支名 被合并的分支,合并内容是要合并到当前分支内
>	git branch 显示已经检出到工作目录的分支名，当前分支用星号（*）表示
>		-a
>		-r
>		-d 分支名 删除指定分支
>		-D 分支名 强制删除指定分支
>	git relog
>	git fsck
>	git checkout
>		分支名 将对应分支的文件释放到工作目录
>		-b 分支名 创建分支并设置该分支为当前分支
>		
>		
>	git diff 工作目录和索引间(暂存区)的不同
>		commit  工作目录和指定提交间的不同
>		--cached commit  索引(暂存区)和指定提交间的不同
>		commit1 commit2  两个指定提交间的不同
>		
>	
>*/
>```
>
>
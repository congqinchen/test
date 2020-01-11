### git常用命令

> **初始化**

```
 git init

```

> ** 添加文件到缓存区 **

```
	git add XXXX  //添加XXXX

	git add *  //添加该目录下的所有文件

```

> ** 提交文件到仓库，创建版本**

```
	git commit -m  "desrc"   //添加缓存区到仓库

```

> **示例**

```	
	git add code.txt
	git commit –m '版本1'

```


> **回退版本**

```	
	git reset --hard HEAD^    //^的个数表示 相对现版本后退的版本数

	git reset --hard HEAD~10  //10表示 相对现版本后退10个版本

	git reset --hard 版本号  //回退到指定的版本

```

> **查看我们的操作记录**

```	
	git reflog

```


> ** 查看当前工作树的状态**

```
	git status

```

> ** 丢弃工作区的改动**

```
	git checkout -- 文件名

```

> ** 暂存区的修改撤销掉，重新放回工作区。**

```
	git reset HEAD 文件名 

```

> ** 撤销修改小结**

```
	场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
	场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作。
	场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节。 
```


> ** 查询日志**

```
	git log  //显示提交日志

	git log --online // 单行显示日志

	git log --pretty=online // 单行显示日志

```

> ** 比工作区中code.txt和HEAD版本中code.txt的不同 **

```
	git diff HEAD -- code.txt

```


> ** 对比两个版本间文件的不同**

```
	git diff 版本1  版本2

```

> ** 删除文件**

```
	git rm  文件名  
	git checkout -- 文件名   // 放弃缓存区删除
	git commit -m "descr"  

```


### 分支管理

> ** 查看分支 **

```
	git branch 

```

> ** 切换分支 **

```
	git checkout 分支名 

```

> ** 创建分支 **

```
	git branch 分支名 

```
> ** 创建 + 切换 分支**

```
	git checkout -b 分支名

```

> ** 合并某分支到当前分支 **

```
	git merge 分支名

```

> ** 删除 非当前 分支 （若需要删除当前分支先切换后删除） **

```
	git branch -d 分支名

```

> ** 暂存工作版本 **

```
	git stash

```

> ** 查看暂存工作版本 **

```
	git stash list

```

> ** 查看暂存工作版本 **

```
	git stash list

```

> ** 恢复工作版本 **

```
	git stash pop

```


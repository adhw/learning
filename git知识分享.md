1. git是什么？
	- git是一款分布式版本控制系统，有别于CVS和SVN等集中式版本控制系统，git可以让研发团队更加高效的协同工作、提高生产率。
2. 为什么要使用git？
3. git怎么使用？

git如何使用？

1. git安装
	git在官网上下载进行安装
2. git的特点
	- 最优的存储能力
	- 非凡的性能
	- 开源的
	- 很容易做备份
	- 支持离线操作
	- 很容易定制工作流程

### 目录
#### 一. Git基础

1. 安装git

2. 使用git之前需要做的最小配置
	- 配置user信息
		- config
			- git config --local user.name [your_name]
			- git config --local user.email [yout_email]
			- git config --local --list
			- 优先级：local>global>system
				- local:区域为本仓库
				- global:当前用户所有仓库
				- system:本系统的所有用户
4. git基本命令
	
	工作区（workspace）暂存区（index）版本库（.git repository）远程仓库（remote）
	- **init add commit **	
		* 新建的项目直接使用git管理
		* git init [repository_name]初始化git仓库
		* cd repository_name
		* 进行一系列的change the file'变更文件'
		* git commit -am ['commit to message']
			- git add .:将工作控件新增和被修改的文件添加到暂存区	
			- git add -u:将已经被git跟踪过的文件添加到暂存区*（不包含没有纳入git管理的新增文件）
			- git commit -m['commit to message']
		* 执行commit后，会建立出一个新的commit节点（HEAD）.三区内容保持一致。
		* commit的本质:每次git提交都会用暂存区的文件创建一个新的提交，把当前的分支指向新的提交节点，这样就完成了一次提交。
	- **mv **
		* git mv [old_fileName] [new_fileName]:更改了旧文件的名字并添加到了缓存区
	- **log **
		* 当前分支版本演进历史 git log
		* 所有分支前四次commit单行图形化展示（注意:不是每个分支）				- git log --all -n4 --oneline --graph	
		* 注意:使用了--all再指定特定分支，特定分支不会起作用。
		* 查看分支所有的操作记录（包括已经删除的等）:git reflog
	- **branch**
		- git branch 默认本地所有分支
		- git branch -r 远端所有分支
		- git branch -a 本地和远端所有分支
		- 加上v参数会显示每个分支最后一个commit eg:git branch -av
		- git branch -D [分支名称]删除不需要的分支
	- **checkout**
		- 创建并切换本地分支 git checkout -b [分支名称] [基于哪里的'Hash值']
	
3. 创建第一个仓库并配置local用户


	
5. 探秘.git目录

6. commit、tree和blob三个对象的关系

7. 分离头指针情况下的注意事项
8. git的升级方法
	- windows系统:直接本地打开git,输入git update-git-for-windows

#### 二. 独立使用Git时的常用场景
##### 1. 怎么删除不需要的分支

- git branch -d branch_name:使用-d在删除前git会判断该分支上的开发功能是否被merge到其它分支，如果没有，不能删除。如果merge到了其他分支，但之后又在其上面进行了开发，使用-d还是不能删除。使用-D表示的是强制删除。
##### 2. 怎么修改最新的commit

- git commit --amend:代替（或者说修改）上一次提交，不只是修改message。比如上一次提交时有几个文件没有add以及commit，可以重新进行add再使用commit --amend进行提交，改提交不会增加新的commit，而是在上一次commit的基础上进行修改。
##### 3. 怎么修改老旧commit的message
##### 4. 怎么把连续的多个commit整理为1个
##### 5. 怎么把间隔的几个commit整理为1个
##### 6. 怎么比较暂存区和HEAD所含文件的差异

- git diff --cached或者git diff --staged
##### 7. 怎么比较工作区和暂存区所含文件的差异
##### 8. 如何让暂存区恢复成和HEAD的一样

#### 三.

工作区()、暂存区(add)、本地仓库(commit)、远程仓库(push)

1、远程仓库已经创建
	1)加入开发
		//下载远程库代码
		git clone https://github.com/sucls/git-study
		//切换代码到dev分支
		git checkout dev
		//等同于以上两个操作
		git clone -b <branch> https://github.com/sucls/git-study
		//提交
		git add .
		git commint -m ''
		git push 

2、开始开发
	1）初始化代码
		//本地初始化
		git init
		//添加本地代码到本地库
		git add .
		//提交工作库到本地库
		git commit -m 'inti'
			>提交消息写错了：
				git commit --amend --message="init"
		//创建本地新分支
		git branch -M main
		//建立库关系
		git remote add origin https://github.com/sucls/git-study
		//本地库代码推送到远程库
		git push -u origin main
		
		
	2）本地创建分支
		//创建本地分支
		git branch dev
		//查看本地分支
		git branch -a
		(上面两条等同于git checkout -b dev)
		//切换当前分支
		git checkout dev
		//为dev分支添加代码
		git add dev-branch-file.txt
		//提交dev分支本地代码
		git commit -m ''
		//本地分支名:远程分支名
		git push origin dev:dev
		
		
		
	3）拉取分支修bug
		//回到目标分支
		git checkout main
		//创建新分支，并切换
		git checkout -b main-u1
		//修改当前分支代码
		修改代码
		//添加修改
		git add . <>
		//提交修改
		git commint -m 'update bugs'
		//切换到需要合并的分支
		git checkout main
		//将main-u1代码合并到main
		git merge main-u1
		//提交到远程库
		git push
		
##
 origin到底是什么？
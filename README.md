# git使用方法

pwd---显示当前目录

git init---把目录变成git可管理目的仓库

把文件放进git仓库的步骤；

​	1、git add<文件名>

​	2、git commit -m<提交的文件说明>

git status---查看文件修改

git diff(difference)---查看修改的部分

git log---查看修改历史记录

git reset--hard HEAD^---回退到上一个版本

git reset--hard<版本号>---回退到未来的某个版本

git reflog---记录每一次操作（命令）

git checkout--<文件名>---把这个文件修改全部撤销

git remote add origin git@server-name:path/repo-name.git---关联一个远程库

git push -u origin master---第一次推送master分支所有内容，此后每次本地提交后只要有必要就可以使用命令git push origin master 推送最新修改。

git clone<仓库地址>克隆仓库到本地

git branch---查看分支

git branch <name>---创建分支

git checkout <name>---切换分支

git checkout -b <name>---创建并切换分支

git merge <name>---合并某分支到当前分支

git branch -d <name>---删除分支

git pull origin <远程分支名>---更新本地仓库和服务器端保持一致。
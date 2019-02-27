# git使用方法

pwd---显示当前目录

git config --global user.email "NaoNao.@nao.com"---配置邮箱地址

git config --global user.name "NaoNao"---配置用户名

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

## 删除git远程仓库文件/文件夹的方法

git rm <filename>---删除文件

git rm -r <foldername>---删除文件夹

git commit -m "log message"---提交上述操作

git push origin master---推送所有文件到远程库

## 创建SSH Key

第1步：创建SSH Key。在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有`id_rsa`和`id_rsa.pub`这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：

ssh-keygen -t rsa -C "youremail@example.com"---创建SSH Key

然后在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的密钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥。

第2步：登陆GitHub，打开“Account settings”，“SSH Keys”页面。然后，点“Add SSH Key”，填上Title，在Key文本框里粘贴`id_rsa.pub`文件的内容：

点“Add Key”，你就应该看到已经添加的Key：

添加SSH Key是因为github需要识别出提送人，以防冒充，而且git支持ssh协议，GitHub只要知道你的公钥，就可以确定只有你自己才能推送。GitHub可以添加多个Key。
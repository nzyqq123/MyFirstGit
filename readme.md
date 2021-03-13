#github 和 本地 git 传输
##在本地生成git
$ git init
将当前路径变为git仓库

$ git add filename
本地添加文件，可以多次添加文件，最后一起commit

$ git commit -m "修改描述"
提交所有修改，不添加-m会弹出一个vim让你填写修改描述

##在本地同步github
$ git remote add localname http://github.com/nzyqq123/filename
localname 本地路径		filename github的路径文件		nzyqq123 github的用户名

$ git branch -M main
在本地生成一个分支，-M是默认，不加-M会创建其他分支

$ git push -u first main
将本地的 first目录 推送到 远程的main分支中，如果github中没有该分支会自动创建

$ git pull origin master
将github的文件拉回本地,origin本地主分支，master github的分支

##分支相关
$ git branch
查看分支

$ git branch branchname
创建分支
 
$ git checkout branchname
切换分支

$ git merge branchname
合并分支到主分支

$ git status
查看内容提交状态

$ git reset --hard HEAD
撤销合并

$ git reset --hard ORIG_HEAD
撤销已提交的合并

$ git branch --set-upstream-to master origin/master
将本地的分支和远程分支关联   master本地分支，origin/master远程分支


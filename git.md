# git 管理
# git remote add origin git@github.com:kitytom/wxproject.git
 git branch -M main 
git push -u origin main

# 需要忽略
# unpackage /dist 
 自动生成的运行到微信小程序中生成的小程序开发的文件
# /node_modules
# 这两个文件不需要
# 新建自定义文件 .gitignore
# 忽略不需要上传的文件
# /node_modules
/unpackage/dist
/unpackage 不会被跟踪
可以新建一个文件站位
.gitkeep
 /unpackage/dist 被忽略
 如果想让unpackage能被正常跟踪 不要创建一个站位文件
 才能被git跟踪
 
 # tabbar 
 
 # 创建分支
 # git checkout -b tabbar
 # git branch 查看分支 *tabbar
 # 基于tabbar 分支创建项目
 
 
# 合并分支提交到github
本地提交
先检查文件
git status
git add . 将代码添加到暂存区
git commit -m "sucess"  本地提交

git push -u origin tabbar 将tabbar分支推送到git仓库
第一次执行需要加上-u
# 报错
$ git push -u origin tabbar
Connection reset by 20.205.243.166 port 22
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

# 如果报错在 后面加上 -f
git push -u origin tabbar -f

# 将tabbar分支合并到本地的main分支
git branch 检查当前处于的分支
git checkout main  先切换到主分支 
git morge tabbar 合并分支
git push main  将合并的主分支代码推送到git仓库
git branch -d tabbar  最后删除tabbar分支


# home 功能
# 创建分支
1 git checkout -b home 创建分支
2 git branch 查看分支
3 git checkout home 切换分支


合并分支
1 先检查 git branch
git status  检查文件状态

git add .  添加到暂存区

git status 检查文件

git commit -m "sucess" 添加到本地仓库

git push -u origin clss 推送到git远程仓库

git checkout main  切换到主分支

git merge clss   合并分支

git push 将main推送到git仓库




# git基本操作

* git clone 克隆网上仓库到本地
* git diff 未添加到git缓存区之前详细修改
  查看做了哪些修改。按 q 退出。
* git add <文件名> 把项目的修改添加到缓存区
* git commit -m '名字' 更新版本
* git push 上传网上
* git pull 多个系统同时更新，先把网上修改的放到本地
* git log 查看当前版本信息
* git log --pretty=oneline 显示1行
* git reset --hard [版本号] 回退到该版本

* 把本地建的文件夹上传到网上
~~~~~~~~~~

  1.先在网上创建仓库
  2.git init(将本地的文件夹变成仓库)
  3.git add README.md
  4.git commit -m "first commit"
  5.git remote add origin git@github.com:beginner-g/a.git
  6.git push -u origin master

~~~~~~~~~~
***********
页面放到 master 分支，是不能显示到 beginner-g.github.io/仓库名 这个位置的。需要创建 gh-pages 分支
### 分支操作(当前分支提交后创建新分支)

* 查看当前状态
  git status
* 创建新分支
  git branch [yourbranch](例：gh-pages)
* 查看分支
  git branch
* 创建并切换分支
  git checkout -b [yourbranch]
* 上传网上
  git push -u origin [yourbranch]
* 切换分支
  git checkout gh-pages
************  
### 分支更新及合并(先切换主分支)

* 切换主分支
  git checkout master
* 合并其他分支代码
  git merge [otherbranch]
* git push
* 拉取主分支上的更新
  git pull origin master
************
### 删除分支

* 切换主分支
  git branch master
* 删除分支
  git branch -d [yourbranch]

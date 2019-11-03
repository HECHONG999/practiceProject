# practiceProject
a project practice
## 从版本未被跟踪到建立索引
git add .\README.md   从工作目录添加到暂存区      -- U未被跟踪   到 Added -- A建立了索引

##  从暂存区提交版本到本地git仓库
git commit -m '提交的版本名字'     -m 对当前提交如数信息

## 监听 工作目录 暂存区 本地git仓库 三区之间的关系 
git status    查看当前工作区的状态 : 工作区修改   是否放到暂存区   是否提交为新的版本

## 从暂存区踢出到工作目录 
git reset HEAD .\index.html

## 进行版本的切换
git  reset --hard HEAD^ 回退一个版本号  ^ 有几个就回退及个版本
git reset --hard HEAD~1   数字是几就回退几个版本

git reset --hard  + 版本号      实现任意版本之间的跳跃 任意版本的切换

## 工作目录撤销操作
git checkout .\index.html   // 花式撤销 当前工作目录上一次修改的内容 

## 版本合并操作

git rebase -i HEAD^^^   //合并多个版本 ^^^ 有几个就合并几个版本  i插入  把pick 改为 squash 按 :wq退出


### 本地仓库推送到远程分支上
git  push -u origin master      // 推送到远程分支上   -u默认推送到远程master分支上


### 工作目录区与暂存区的比较：
git diff  


## 远程分支
 ** 远程分支的基础工作流程 ：git的分支相当于一个平行时空： 同一时间在做不同的事情 ， 但git在有需要时可以进行分支的合并

 ### 查看分支
 git branch   

 ### 创建一个新的分支 ： 相当于复制一个一摸一样的自己出去 但它在另一个平行时空中
 git branch dev-HECHON


 ### 创建分支并切换分支

git checkout -b dev-XIAODAN


### 各分支间的代码合并
git merge dev-HECHONG


### 删掉本地分支：
git branch -d  dev-DELE


### 建立与远程仓库的联系
本地仓库 与 远程仓库 进行联系
1、git remote add origin + 远程新仓库的地址   先建立与远程仓库的联系 
2、先 git pull --rebase origin master    // 拉取远程分支上的代码进行合并 
2、添加到暂存区 git add .      提交到本地git仓库  git commit -m ' 版本名字'
3、然后才能 git push  origin  master   本地仓库内容上传到远程仓库master分支的内容 .gitignore 里限制的内容不能上传

### 拉取远程分支上的代码: 
git  pull origin master   // 拉取远程origin 分支下的 master 分支




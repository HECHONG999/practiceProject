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

git reset HEAD~3      //数字是几就回几个版本号

git checkout .\index.html   // 花式撤销 当前工作目录上一次修改的内容 

## 版本合并操作

git rebase -i HEAD^^^   //合并多个版本 ^^^ 有几个就合并几个版本  i插入  把pick 改为 squash 按 :wq退出


### 本地仓库推送到远程分支上
git  push -u origin master      // 推送到远程分支上   -u默认推送到远程master分支上



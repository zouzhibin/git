## git的比较（看哪些文件发生了变化）
- git diff 工作区和暂存区的比较
- git diff 分支名 工作区和历史区的的对比
- git diff --cached 暂存区和历史区比较

## linux命令
- pwd print working directory 打印当前工作目录
- rm -rf 文件夹 删除文件
- rm 文件名 删除文件
- mkdir 文件夹名字创建目录

## 撤销
- 从暂存区中将工作区内容覆盖掉 
```
git checkout 文件名  是指还没有提交到暂存区的文件,可以用暂存区覆盖掉工作区
```

## 回滚
```
git reset HEAD 文件名 指当前的工暂存区修改的有误 可以进行回滚到上次的提交，回滚到上一次的缓存区，也就是上一次的git add .

git reset --hard 版本号 历史区直接回滚到指定版本号
git reset --hard HEAD^ 历史区回滚到上一个版本号
```

- history -> 2.txt 可以把历史记录放到2.txt 这个文件中


## 当你文件提交过一次之后，可以省略git add 直接一个命令可以提交到历史区
- git commit -a -m "提交信息" 

## 打印日志
- git log 打印修改日志
- git reflog 打印所有日志

## 分支的操作
### Git branch
- git branch 不带参数：列出本地已经存在的分支，并且在当前分支的前面用"*"标记
- git branch -r 查看远程版本库分支列表
- git branch -a 查看所有分支列表，包括本地和远程
- git branch dev（分支名） 创建名为dev的分支，创建分支时需要是最新的环境，创建分支但依然停留在当前分支
- git branch -d dev 删除dev分支，如果在分支中有一些未merge的提交，那么会删除分支失败，此时可以使用 git branch -D dev：强制删除dev分支，
- git branch -vv 可以查看本地分支对应的远程分支
- git branch -m oldName newName 给分支重命名
### Git checkout
- git checkout filename 放弃单个文件的修改
- git checkout . 放弃当前目录下的修改
- git checkout master 将分支切换到master
- git checkout -b master 如果分支存在则只切换分支，若不存在则创建并切换到master分支，repo start是对git checkout -b这个命令的封装，将所有仓库的分支都切换到master，master是分支名，
- git checkout --help  查看帮助

## 暂存 文件修改切换分支
- git stash 把刚才修改的代码进行缓存起来
> 分支有更改不能直接切换，可以提交更改或者暂存更改,暂存使用过渡期覆盖掉工作区，
- git stash pop 还原暂存的内容
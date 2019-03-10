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
git log 打印修改日志
git reflog 打印所有日志


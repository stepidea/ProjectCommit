**附加信息可以查看Wiki;GitHub的GUI客户端可以使用SourceTree或官方软件。**

## Git操作

- 初始化仓库，生成 的.git 目录里存储着管理当前目录内容所需的仓库数据，其内容被称为“附属于该仓库的工作树”。

```
$  git init
```

- 查看仓库的状态，检查是否有文件需要提交到Git仓库

```
$ git status
```

- 向暂存区中添加 README.md文件

```
$ git add README.md
```

- 保存仓库的历史记录，将当前暂存区中的文件实际保存到仓库的历史记录

```
$ git commit -m "提交信息"
$ git commit  #命令执行后可以记录详细的修改信息
```

- 添加到暂存区并保存文件到仓库

```
$ git commit -am "提交信息"
```

- 查看提交日志

```
$ git log
$ git log --pretty=short  #只显示提交信息的第一行
$ git log README.md  #显示指定目录、文件的日志
$ git log --graph  #以图表形式查看分支
```

- 显示README文件的改动，输入q进行退出

```
$ git log -p README.md
```

- 查看工作树、暂存区、最新提交之间的差别,一般在git commit命令之前先执行，查看本次提交与上次最新提交之间有什么差别

```
$ git diff HEAD
```

- 显示分支一览表，可以将分支名列表显示，*可以确认当前所在分支。


```
$ git branch  #显示本地仓库的分支信息
$ git branch -a  #显示本地仓库和远程仓库的分支信息
```

- 创建、切换分支 feature1，需要在主分支下进行执行

```
$ git branch feature1
$ git checkout feature1  
相当于  $ git checkout -b feature1
```

- 切换回上一个分支

```
$ git checkout -
```

- 合并分支，在主分支下执行

```
$ git merge --no-ff feature1
```

- 查看当前仓库的操作日志

```
$ git reflog
```

- 回溯历史版本，即回溯到指定状态；需要提供目标时间点的哈希值

```
$ git reset --hard xxx   #哈希值：xxx ，通过 git reflog 获取
```

- 修改上一条提交信息

```
$ git commit --amend
```

- 更改历史，将第二个pick改写为 fixup

```
$ git rebase -i HEAD~2   #选定当前分支中包含HEAD（最新提交）在内的两个最新历史记录
```

- 推送至远程仓库，-u将origin仓库的 master 分支设置为本地仓库当前分支的 upstream

```
$ git push -u origin master
```

- 获取远程仓库

```
$ git clone 项目地址
```

- 获取远程仓库以名为 origin 的仓库的 commitbranch 分支

```
$ git checkout -b commitbranch origin/commitbranch
```

- 获取最新的远程仓库分支

```
$ git pull origin commitbranch
```

- 给原仓库设置远程仓库


```
$ git remote add upstream 项目地址
```

- 获取最新数据，合并更新

```
$ git fetch upstream
```


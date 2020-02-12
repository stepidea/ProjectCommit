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

- 查看提交日志

```
$ git log
$ git log --pretty=short  #只显示提交信息的第一行
$ git log README.md  #显示指定目录、文件的日志
$ git log --graph  #以图表形式查看分支
```

- 显示README文件的改动

```
$ git log -p README.md
```

- 查看工作树、暂存区、最新提交之间的差别,一般在git commit命令之前先执行，查看本次提交与上次最新提交之间有什么差别

```
$ git diff HEAD
```

- 显示分支一览表，可以将分支名列表显示，*可以确认当前所在分支。


```
$ git branch
```

- 创建、切换分支 feature1，需要在主分支下进行执行

```
$ git branch feature1
$ git checkout feature1  相当于  $ git checkout -b feature1
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


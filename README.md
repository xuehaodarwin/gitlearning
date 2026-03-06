# git-learning
for git learning

```Git
git config user.name "name"
git config user.email "email"

git config user.name
git config user.email

git add 文件名
git add .
git status

git commit -m"提交说明"

git clone https/ssh

git remote add <name> <url>
git push
```

#### 安装完 Git 后需要指定一个本地的仓库 $(Repository)$ 

1. 选择一个工作文件夹作为本地仓库，右键选择 $Open~Git~Bash~here$ 打开 Git 专属命令窗口，输入：

```Git
git init
```

会在该文件夹得到一个隐藏文件夹 .git，建议常在初始化后立即补充 `.gitignore` 与 README.md

2. 远程从 github 等在线仓库克隆现有仓库

```Git
git clone https/ssh
```

#### Git 基础操作：跟踪-提交-复盘

1. 查看工作区和暂存区的文件状态

```Git
git status
```

2. 修改好本地仓库的文件后，利用 Git 提交到暂存区

```Git
git add <file>
添加指定文件
git add .
添加所有改动文件
```

3. 提交暂缓区到本地仓库

```Git
git commit -m "Message" 
"Message"里填写详细的增改信息，当提交信息涉及多行描述时，可以用下属代码进去编辑器模式
git commit
```

4. 查看提交的历史纪录

```Git
git log
或者用简介模式
git log --oneline --graph
```

5. 安全地**删除**或**重命名**文件，让 Git 保留历史轨迹

```Git
git rm
git mv
```

#### Git的分支管理：发行与开发分开

1. 列出分支列表

```
git branch
```

2. 切换到指定分支

```
git checkout <branch-name>
或者切换并创建指定分支
git checkout -b <branch-name>
```

3. 将指定分支的更改合并到当前分支

```
git merge <branch-name>
```

4. 删除已合并的本地分支

```
git branch -d <branch-name>
```

#### Git与远程仓库

1. 列出所有配置的远程仓库

```
git remote
```

2. 添加一个新的远程仓库

```
git remote add <name> <url>
用github举例子，<name>可以是<Origin>
```

3. 将本地分支的更改推送到远程仓库

```
git push <remote> <branch>
用github主分支举例：git push origin main
```

4. 从远程仓库拉取并合并更改

```
git pull <remote> <branch>
```

#### 恢复历史版本

1. 恢复工作目录中的文件到某个提交

```
git checkout <commit> -- <filename>
```


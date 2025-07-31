# 1.Git工作流程

![001](D:\soft\GitHub\GitHub_Repositories\Blog_picture01\H01_开发技能\1.Git&Github\1.Git基础\001.png)

- 工作区：项目文件夹。
- 暂存区：一个临时的“快照区”。它不属于工作区，也不属于仓库，而是一个中间区域。
- 本地仓库：电脑上的一个数据库（`.git` 文件夹），它存储了项目所有的历史版本、分支信息等。
- 远程仓库：存储在互联网上的仓库。





# 2.Git本地仓库

## 2.1 基础命令

![001](D:\soft\GitHub\GitHub_Repositories\Blog_picture01\H01_开发技能\1.Git&Github\1.Git基础\002.png)

```shell
# 工作区 --> 暂存区
git add .		# git add file01.txt

# 暂存区 --> 本地仓库
git commit -m "注释内容"

# 查看日志
git log --all --pretty=oneline --abbrev-commit --graph 


```

```shell
# 添加文件至忽略列表
# 工作目录中创建一个名为 .gitignore 的文件，列出要忽略的文件。

# 实例：
# no .pdf files
*.pdf
```



## 2.2 分支

![001](D:\soft\GitHub\GitHub_Repositories\Blog_picture01\H01_开发技能\1.Git&Github\1.Git基础\003.png)



```shell
# 查看本地分支
git branch

# 创建并切换分支
git checkout -b 分支名		# 有分支 git checkout 分支名

# 合并分支(merge)：先到目标分支上
git merge 分支名称
```

```shell
合并冲突：两个分支上同时修改了同一个文件的同一行。
	这时就需要手动解决冲突
```



# 3.Git远程仓库

- Https：`https://github.com/silent-wuhen/gitDemo.git`
- SSH：`git@github.com:silent-wuhen/gitDemo.git`



```shell
# 从远程仓库克隆(克隆main分支)
git clone https://github.com/silent-wuhen/gitDemo.git

# 克隆其他分支
git clone -b dev https://github.com/silent-wuhen/gitDemo.git

cd gitDemo
```



# 4.案例

> 远端分支：main，dev

1. main，dev两个分支分别克隆
2. main上传`file02.txt`文件，dev上传`file03.txt`文件。
3. main上传，dev要合并到main分支中



main分支：

```shell
git clone https://github.com/silent-wuhen/gitDemo.git

cd gitDemo

echo "This is file02" > file02.txt

git add .

git commit -m "Add file02.txt in main"

git push 	# git push origin main
```

dev分支：

```shell
git clone https://github.com/silent-wuhen/gitDemo.git

cd gitDemo

git checkout dev

echo "This is file03" > file03.txt

git add .

git commit -m "Add file03.txt in dev"

git push 	# git push origin dev

git checkout main

git pull 	# git pull origin main

git merge dev

git push 	# git push origin main
```


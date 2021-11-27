## 分支管理  
- 创建分支：       `git branch <branch_name>`  
- 切换到分支：     `git checkout <branch_name>`  
- 创建并切换分支：  `git checkout -b <branch_name>`  
- 查看分支：       `git branch`  
	> 注： `git branch` 会列出所有的分支，在当前的分支前会有 \* 号  
- 合并指定分支到当前分支，默认使用 Fast_Forward 模式：       `git merge <branch_name>`    
- 创建并切换新的分支： `git switch -c <branch_name>`  
- 直接切换到已有的分支： `git switch <branch_name>`  
- 删除分支： `git branch -d <branch_name>`  
- 强制删除一个还未合并的分支： `git branch -D <branch_name>`  

## 多人协同

- `git remote (-v)  # 查看远程仓库信息`

### 推送分支  
即将该分支上的所有本地文件都推送到远程仓库。推送时，要指定本地分支，Git 就会把该分支推送到对应的  
远程分支上。  

`git push origin master # 将本地 Master 分支的文件推送到远程仓库 origin 的 master 分支`  
`git push origin <branch_name> # 将本地分支 branch_name 的文件推送到远程仓库 origin 对应 的 branch_name 分支`

### 抓取分支  

我们假设： 远端仓库有 master 和 dev 两个分支  
如果直接克隆远端仓库： `git clone git@gitlab.com:saitoler/test.git`  , 默认情况下，你在本地只能看到一个 master  
分支， 是无法看到 dev 分支的。  

那如何拉取 dev 分支的文件到本地呢？  
`git checkout  -b dev origin/dev # 创建远程  origin 仓库的 dev 分支到本地`  
现在就能在 dev 分支上进行修改，然后不时的将 dev 分支的修改推送到远程。  

### 多人协同工作模式
1. 首先，可以试图使用  `git push origin <branch_name>` 推送自己的修改  
2. 如果推送失败，则因为远程分支比你本地要新一些，要先 git pull 合并  
3. 如果合并有冲突，则先解决冲突  
4. 解决冲突后，再用 `git push origin <branch_name>` 推送即可成功  

> 注： `git pull ` 提示 `no tracking information` ， 是因为本地分支和远程分支的链接关系没有创建起来，可以通过  
`git branch --set-upstream-to <branch_name> origin/<branch_name>`  进行创建。  



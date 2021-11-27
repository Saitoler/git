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

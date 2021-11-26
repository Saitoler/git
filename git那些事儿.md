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



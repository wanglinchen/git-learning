# git learning
1. git的工作流程
> 工作区：被git管理的整个文件夹  
  暂存区：将当前修改存储在暂存区  
  版本库：.git仓库管理版本库

2. git config
> git config --global core.editor      配置编辑器  
  git config --global user.name        配置用户名  
  git config --global user.email       配置用户邮箱  
  git config --global commit.template  配置commit模板  

3. 仓库操作：
> git init             生成.git文件夹  
  git pull             拉取远程仓库的最新状态，使本地与远程仓库保持一致  

4. 工作区操作：
> git clean -nfd       删除工作区unstage的文件/文件夹  
  git status           查看工作区的状态  
  git diff             和最新的版本比较查看工作区的修改  
  git add              把工作区变更的内容添加到暂存区  

5. 暂存区操作：
> git checkout .       放弃暂存区的修改  
  git rm -r --cached  asdf        删除暂存区的asdf文件  
  git commit           把暂存区的内容提交到版本库     
  git commit --amend   在当前的版本上提交，不产生新的版本  

6. 版本库操作：
> git log              查看历史版本信息  
  git reset --soft HEAD~1         将当前的版本回退到上一个版本commit之前的状态（保留该版本的修改）  
  git reset --hard HEAD~1         将当前的版本回退到上一个版本（不保留该版本的修改）  
  git push             把暂存区的修改推送到远程分支  

7. 缓存区操作：
> git stash save       保存本地的修改到stash本地缓存区,应用于中断当前工作，进入下一个工作，等有空的时候恢复缓存内容。  
  git stash list       列出stash里的内容  
  git stash apply stash{ID}   恢复stash{ID}的内容  
  git stash drop stash{ID}    删除stash{ID}的内容  

8. 分支操作：
- 查看分支
> git branch           查看本地分支  
  git branch -r        查看远程分支  
  git branch -vv       查看本地分支关联的远程分支  

- 创建&切换分支&删除分支
> git branch dev       创建本地dev分支  
  git checkout dev     切换到本地dev分支  
  git checkout -b dev  创建并切换到本地dev分支  
  git branch -d dev    删除本地分支dev  
  
- 关联已存在的远程分支
> git branch -u origin     将当前本地分支关联到远程origin分支  

- 合并分支
> git merge dev        把dev分支合并到当前分支  

9. 标签操作
> 给版本打上标签名字
> 历史合并
> 在历史版本上修改，不产生新的版本

10. 远程库修改
> git remote set-url --push [远程仓库名称] [更换的git服务器地址]      更换git服务器的地址
> git remote add 添加远程库










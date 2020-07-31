# Git 工作流
---
## 分支权限
`master`分支已经被锁定，不允许直接push  
但是可以pull request，只要pull request的时候通过Code Owner的review和GitHub Action的流程，才可以合并到`master`分支

## 工作流程
- 拉取master分支代码
- 本地创建新分支，例如：`issue-13-fix`
- 修改代码
- 提交新分支到远端库
- 提交pull request到`master`分支

## 相关Git命令
- `git init` 创建一个新的版本库
- `git clone` 拉取远端版本库到本地
- `git pull` 将远端版本库的版本更新到本地
- `git fetch` 同步版本库信息
- `git push` 推送代码，tag之类的
- `git help` 可以查看git相关的命令

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

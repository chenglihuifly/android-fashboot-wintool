请帮我将本地项目同步到 GitHub，执行以下步骤：

1. 检查当前目录是否是 git 仓库
   - 如果不是，执行 `git init` 初始化仓库

2. 检查是否有 GitHub 远程仓库
   - 如果没有远程仓库，询问用户 GitHub 仓库 URL 或仓库名称
   - 使用 `gh repo create` 创建新仓库（如果用户提供仓库名）
   - 或使用 `git remote add origin <URL>` 添加现有仓库

3. 添加所有文件到暂存区
   - 运行 `git add -A`

4. 创建提交
   - 询问用户提交信息，如果没有提供则使用默认信息 "Update files"
   - 运行 `git commit -m "<提交信息>"`

5. 推送到 GitHub
   - 检查当前分支
   - 如果是首次推送，使用 `git push -u origin <branch>`
   - 否则使用 `git push`

6. 显示推送结果和仓库链接

注意事项：
- 检查是否安装了 GitHub CLI (gh)
- 如果有未提交的更改，先提交再推送
- 如果遇到冲突或错误，给出清晰的错误提示
- 确保用户已登录 GitHub CLI

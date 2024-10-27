# git的简单使用

## 克隆远程库到本地

git clone 

```bash
git clone <远程库地址>
```

## 提交本地更改上传到远程库

**注意**：如果远程库已经更改，则需要`git pull`进行拉取更新，更新后，再进行操作

1. 进入克隆的本地库

   ```bash
   cd "克隆后的本地库地址"
   ```

2. 修改并提交文件到暂存区

   ```bash
   git add .
   ```

   **注意**：有一个`.`！！！！！！！！！！

3. 提交更改到本地库

   ```bash 
   git commit -m "提交说明"
   ```

   **注意**：需要英文的`" "`

4. 将此更改推送到远程库

   ```bash
   git push origin <分支名>  # 如果是主分支，则用main或master
   ```

5. 查看提交日志，确保是否提交

   ```bash
   git log
   ```

   **注意**：使用`q`退出此界面，进行进行其他操作命令

6. 验证是否成功上传

   ```bash
   git status
   ```

## git上传文件到github

**使用http链接**

1. 进入希望希望克隆仓库的目录

2. 运行命令克隆仓库

   ```bash
   git clone https://github.com....
   ```

3. 如果仓库是私有的，Git 会提示你输入 GitHub 的用户名和密码。在输入密码时，GitHub 现在要求使用 **Personal Access Token**（而不是直接的账户密码）。你可以在 GitHub 设置中生成一个 Token。

4. 复制文件到本地仓库

   ```bash
   cp "被要复制的文件地址" "克隆的库地址"
   ```

5. 进入克隆的仓库

6. 存入暂存区

   ```bash
   git add 文件名.后缀名
   ```

7. 提交更改

   ```bash
   git commit -m "添加说明"
   ```

8. 推送到GitHub库

   ```bash
   git push origin main
   ```

**如果更新了怎么办**

1. 进入克隆仓库目录

2. 检查文件更改

   ```bash
   git status
   ```

3. 添加到暂存区

   ```bash
   git add filename.md
   ```

   如果有多个更改文件，可以使用 `.` 添加所有更改：

   ```bash
   git add .
   ```

4. 提交更改

   ```bash
   git commit -m "更新说明"
   ```

5. 推送到远程库

   ```bash
   git push origin main
   
   
   使用 master 分支：
   git push origin master
   ```

   
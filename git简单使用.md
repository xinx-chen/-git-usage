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

在本地准备好文件，将它们上传到 GitHub。

1. 初始化本地仓库

   ```bash
   git init
   ```
   
 2. 关联远程库地址

    ```bash
    git remote add origin <远程库地址>
    ```

    例如：

    ```bash
    git remote add origin ssh://sys.....
    ```

3. 添加文件并提交更改

   确认本地的文件已添加并提交：

   ```bash
   git add .
   git commit -m "添加说明"
   ```

  4. 推送到远程库

     将本地提交推送到远程库：

     ```bash
      git push -u origin <分支名>  # 一般是 main 或 master 分支
     ```

     第一次推送时，可以使用 `-u` 选项来设置默认的上游分支，以后可以直接用 `git push` 推送到该分支。

  5. 检查推送情况

     推送完成后，可以在远程仓库中查看是否成功上传了文件。
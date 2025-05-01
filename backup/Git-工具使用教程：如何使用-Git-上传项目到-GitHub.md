## 前置条件

### 1. 安装 Git：
- 下载并安装 [Git](https://git-scm.com/)，安装后配置全局用户名和邮箱：

    ```bash
    git config --global user.name "YourName"
    git config --global user.email "YourEmail@example.com"
    ```

### 2. 创建 GitHub 账户：
- 如果没有账号，请访问 [GitHub](https://github.com/) 注册。

### 3. 准备一个项目文件夹：
- 将项目文件放在一个文件夹内。

---

## 步骤 1：在 GitHub 上创建一个新仓库

1. 登录 GitHub。
2. 点击右上角的 **+** 图标，选择 **New repository**。
3. 填写仓库名称、描述（可选）并选择公开或私有。
4. 点击 **Create repository**。

---

## 步骤 2：初始化本地项目仓库

1. 打开终端或命令行工具，进入项目文件夹：

    ```bash
    cd /path/to/your/project
    ```

2. 初始化 Git 仓库：

    ```bash
    git init
    ```

3. 添加项目文件到 Git 仓库：

    ```bash
    git add .
    ```

4. 提交更改：

    ```bash
    git commit -m "Initial commit"
    ```

---

## 步骤 3：连接本地仓库到 GitHub

1. 获取 GitHub 仓库的远程地址：  
   在 GitHub 仓库页面，复制仓库地址（HTTPS 或 SSH）。

2. 添加远程仓库地址：

    ```bash
    git remote add origin <GitHubRepositoryURL>
    ```

   示例：

    ```bash
    git remote add origin https://github.com/YourUsername/YourRepository.git
    ```

---

## 步骤 4：推送项目到 GitHub

1. 将代码推送到 GitHub：

    ```bash
    git branch -M main  # 确保分支名称为 main
    git push -u origin main
    ```

2. 如果推送成功，您将在 GitHub 仓库页面看到上传的项目文件。

---

## 额外步骤：定期更新仓库

### 1. 查看当前状态：

    ```bash
    git status
    ```

### 2. 添加新的更改：

    ```bash
    git add .
    git commit -m "Your commit message"
    git push
    ```

### 3. 拉取远程更改（如果有）：

    ```bash
    git pull origin main
    ```

---

## 常见问题及解决方法

### 1. 权限错误：
- 确保您已正确配置 SSH 密钥或使用 HTTPS 并输入正确的 GitHub 用户名和密码。

### 2. 分支冲突：
- 使用以下命令解决：

    ```bash
    git pull origin main --rebase
    git push
    ```

### 3. 无权限推送到远程仓库：
- 检查是否使用了正确的用户权限或是否有写入权限。

---

通过以上步骤，您可以轻松将项目上传并管理到 GitHub 仓库中！

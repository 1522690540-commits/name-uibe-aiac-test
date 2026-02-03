# GitHub Pages 部署指南

## 📋 部署步骤

### 1. 初始化 Git 仓库

```bash
cd /c/Users/l1360
git init
git add .
git commit -m "Initial commit: UIBE AIAC Test Platform"
```

### 2. 在 GitHub 上创建仓库

1. 访问 [GitHub](https://github.com)
2. 点击右上角的 "+" 按钮，选择 "New repository"
3. 填写仓库信息：
   - **Repository name**: `uibe-aiac-test` (或其他你喜欢的名称)
   - **Description**: `A comprehensive testing platform for UIBE AIAC program`
   - **Public/Private**: 选择 Public（GitHub Pages 免费版需要公开仓库）
   - **不要**勾选 "Initialize this repository with a README"（我们已经有了）

### 3. 连接远程仓库并推送

```bash
# 替换 YOUR_USERNAME 为你的 GitHub 用户名
git remote add origin https://github.com/YOUR_USERNAME/uibe-aiac-test.git
git branch -M main
git push -u origin main
```

### 4. 配置 GitHub Pages

1. 在 GitHub 仓库页面，点击 "Settings"
2. 在左侧菜单找到 "Pages"
3. 在 "Source" 部分：
   - Branch: 选择 `main`
   - Folder: 选择 `/ (root)`
4. 点击 "Save"

### 5. 等待部署完成

- GitHub 会自动部署你的网站
- 通常需要 1-3 分钟
- 部署完成后，你会看到一个绿色的提示框，显示网站地址：
  ```
  Your site is published at https://YOUR_USERNAME.github.io/uibe-aiac-test/
  ```

## 🔄 更新网站

每次修改文件后，运行以下命令更新网站：

```bash
git add .
git commit -m "描述你的修改"
git push
```

GitHub Pages 会自动重新部署。

## 🌐 访问网站

部署完成后，你的网站地址将是：
```
https://YOUR_USERNAME.github.io/uibe-aiac-test/
```

或者如果你使用了自定义域名：
```
https://your-custom-domain.com
```

## 📝 注意事项

1. **首次部署**可能需要等待几分钟
2. **更新内容**后，GitHub Pages 通常会在 1-2 分钟内自动更新
3. 如果网站没有更新，尝试：
   - 清除浏览器缓存
   - 使用无痕模式访问
   - 等待几分钟后再试

## 🔧 自定义域名（可选）

如果你有自己的域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 文件内容为你的域名，例如：`aiac.example.com`
3. 在你的域名提供商处添加 DNS 记录：
   - Type: `CNAME`
   - Name: `aiac` (或 `@` 如果是根域名)
   - Value: `YOUR_USERNAME.github.io`

## 🐛 常见问题

### 问题：网站显示 404
- 确保 `index.html` 文件在仓库根目录
- 检查 GitHub Pages 设置中的分支和文件夹是否正确

### 问题：样式或脚本加载失败
- 检查所有资源链接是否使用相对路径或完整的 CDN 链接
- 当前项目使用 CDN，应该没有这个问题

### 问题：密码不工作
- 默认密码是 `UIBEAIAC`
- 密码区分大小写

## 📞 支持

如有问题，请联系 UIBE AIAC 项目组。

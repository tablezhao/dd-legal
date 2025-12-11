# 部署指南：法律尽职调查导航 - Vercel平台

本指南将帮助您将「法律尽职调查导航」项目部署到Vercel平台。

## 准备工作

1. **注册GitHub账户**
   如果您还没有GitHub账户，请前往[GitHub官网](https://github.com/)注册。

2. **注册Vercel账户**
   前往[Vercel官网](https://vercel.com/)注册账户，并使用GitHub账户登录以简化后续流程。

## 部署步骤

### 步骤1: 将项目上传到GitHub

1. 在GitHub上创建一个新仓库
2. 使用Git命令将本地项目推送到GitHub：

```bash
# 在项目根目录初始化Git仓库（如果尚未初始化）
git init

# 添加所有文件
git add .

# 提交更改
git commit -m "初始化项目"

# 添加远程仓库地址（替换为您的GitHub仓库URL）
git remote add origin https://github.com/您的用户名/仓库名.git

# 推送到GitHub
git push -u origin master
```

### 步骤2: 在Vercel上部署项目

1. 登录Vercel账户
2. 点击「New Project」（新项目）
3. 从GitHub仓库列表中选择您刚才创建的仓库
4. Vercel会自动识别这是一个Hexo项目，并使用我们创建的`vercel.json`中的配置
5. 点击「Deploy」（部署）按钮开始部署过程

### 步骤3: 配置域名（可选）

如果您想使用自定义域名（如dd.legal）：

1. 在Vercel项目的「Settings」（设置）中找到「Domains」（域名）选项
2. 添加您的自定义域名
3. 按照Vercel提供的指引，在您的DNS提供商处设置相应的DNS记录

## 本地开发

如果您想在本地修改和预览网站：

1. 安装项目依赖：
   ```bash
   npm install
   ```

2. 启动本地服务器：
   ```bash
   npm run server
   ```

3. 访问 `http://localhost:4000` 查看本地预览

4. 修改完成后，可以使用以下命令重新构建：
   ```bash
   npm run build
   ```

## 更新部署

每次您将更改推送到GitHub仓库后，Vercel会自动检测并重新部署您的网站，无需手动操作。

## 注意事项

1. 确保您的`package.json`中的依赖版本与您的Node.js版本兼容
2. 如果在部署过程中遇到问题，请检查Vercel的构建日志以获取详细的错误信息
3. 如需进一步定制网站内容，请修改`_config.yml`文件和`source`目录中的内容

祝部署顺利！
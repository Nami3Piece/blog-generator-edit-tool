# Blog Generator with Edit Tool

多平台博客生成工具 - 自动将博客内容和插图转换为适配不同平台的格式

## 项目简介

这个工具可以将原始博客文本（Word/Markdown）和插图（PDF/图片）自动转换为四个主流平台的发布格式：
- Medium
- Mirror (Web3)
- X/Twitter Article
- 官网 Blog HTML

## 如何使用

### 申请访问权限

本项目为团队内部工具。如需使用，请：

1. 联系项目维护者申请 Collaborator 权限
2. 或提交 Issue 说明使用场景
3. 获得批准后即可 clone 到本地使用

### 克隆到本地

```bash
git clone git@github.com:Nami3Piece/blog-generator-edit-tool.git
cd blog-generator-edit-tool
```

### 准备你的内容

1. 将博客文本放在 `blog.docx` 或 `blog.txt`
2. 将插图放在 `插图.pdf` 或单独的图片文件
3. 运行生成脚本（待开发）

## 反馈和问题

如果在使用过程中遇到问题或有改进建议：

1. 提交 Issue：https://github.com/Nami3Piece/blog-generator-edit-tool/issues
2. 描述问题或建议
3. 我们会尽快回复

欢迎团队成员贡献代码和改进！

---

## 文件说明

当前版本包含四个平台的博客示例：

### 1. Medium (`medium.md`)
- 格式：Markdown
- 图片：使用相对路径引用
- 发布方式：
  1. 登录 Medium
  2. 点击「Write」
  3. 点击「...」菜单 → 「Import a story」
  4. 上传 `medium.md` 文件
  5. 手动上传图片（从 `blog_images/` 文件夹）

### 2. Mirror (`mirror.md`)
- 格式：Markdown（支持 Web3 特性）
- 图片：使用相对路径引用
- 发布方式：
  1. 访问 https://mirror.xyz
  2. 连接钱包
  3. 点击「New Entry」
  4. 切换到 Markdown 模式
  5. 复制粘贴 `mirror.md` 内容
  6. 上传图片到 Mirror 的图片托管
  7. 更新图片链接

### 3. X Article (`x-article.md`)
- 格式：Thread 格式（分段）
- 每个 `---` 分隔符代表一条推文
- 发布方式：
  1. 访问 https://x.com
  2. 创建新推文
  3. 按照分段逐条发布（或使用 Thread 功能）
  4. 图片需要手动插入到对应推文中

### 4. 官网 Blog (`blog.html`)
- 格式：完整的 HTML 页面
- 样式：已内置响应式设计
- 发布方式：
  1. 直接部署到官网 `/blog/` 目录
  2. 或集成到现有博客系统
  3. 图片路径需要调整为实际路径

## 图片文件

所有图片已提取到：`~/Desktop/blog_images/`
- `image-01.png` 到 `image-13.png`
- 共 13 张图片

## 发布前准备

### 上传图片到图床（推荐）

使用图床服务（如 Imgur、Cloudinary）统一托管图片：

```bash
# 示例：使用 Imgur
# 1. 访问 https://imgur.com/upload
# 2. 批量上传 blog_images/ 中的所有图片
# 3. 获取每张图片的 URL
# 4. 替换 Markdown 文件中的图片路径
```

### 或者部署到自己的服务器

```bash
# 上传到官网静态资源目录
scp -r ~/Desktop/blog_images/ user@server:/var/www/html/blog/images/

# 然后在 Markdown 中使用绝对路径
# ![Image](https://yourdomain.com/blog/images/image-01.png)
```

## 快速发布清单

- [ ] 上传图片到图床或服务器
- [ ] 更新 Markdown 文件中的图片链接
- [ ] Medium: 导入 `medium.md`
- [ ] Mirror: 复制 `mirror.md` 内容
- [ ] X: 按 `x-article.md` 分段发布
- [ ] 官网: 部署 `blog.html` 并调整图片路径

## 注意事项

1. **图片优化**：建议压缩图片以提升加载速度
2. **SEO**：Medium 和官网版本已包含 meta 标签
3. **链接**：确保所有外部链接正常工作
4. **预览**：发布前在各平台预览效果
5. **中文版本**：如需中文版，可以基于英文版翻译

## 中文版本

博客文本包含完整的中文翻译，如需发布中文版本，可以使用相同的模板结构，替换英文内容为中文内容即可。

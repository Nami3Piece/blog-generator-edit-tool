# Blog Generator with Edit Tool

Multi-platform blog generator - automatically converts blog content and images into formats optimized for different platforms

多平台博客生成工具 - 自动将博客内容和插图转换为适配不同平台的格式

---

## Project Overview | 项目简介

**English**: This tool automatically converts your raw blog content (Word/Markdown) and images (PDF/images) into optimized formats for four major publishing platforms:

**中文**: 这个工具可以将原始博客文本（Word/Markdown）和插图（PDF/图片）自动转换为四个主流平台的发布格式：

- Medium
- Mirror (Web3)
- X/Twitter Article
- Website Blog HTML

---

## How to Use | 如何使用

### Request Access | 申请访问权限

**English**: This is a team-internal tool. To use it:

1. Contact the project maintainer to request Collaborator access
2. Or submit an Issue explaining your use case
3. Once approved, clone the repo to your local machine

**中文**: 本项目为团队内部工具。如需使用，请：

1. 联系项目维护者申请 Collaborator 权限
2. 或提交 Issue 说明使用场景
3. 获得批准后即可 clone 到本地使用

### Clone to Local | 克隆到本地

```bash
git clone git@github.com:Nami3Piece/blog-generator-edit-tool.git
cd blog-generator-edit-tool
```

### Prepare Your Content | 准备你的内容

**English**:
1. Place your blog text in `blog.docx` or `blog.txt`
2. Place images in `插图.pdf` or separate image files
3. Run the generation script (to be developed)

**中文**:
1. 将博客文本放在 `blog.docx` 或 `blog.txt`
2. 将插图放在 `插图.pdf` 或单独的图片文件
3. 运行生成脚本（待开发）

---

## Feedback and Issues | 反馈和问题

**English**: If you encounter any problems or have suggestions:

1. Submit an Issue: https://github.com/Nami3Piece/blog-generator-edit-tool/issues
2. Describe the problem or suggestion
3. We'll respond as soon as possible

We welcome contributions from all team members!

**中文**: 如果在使用过程中遇到问题或有改进建议：

1. 提交 Issue：https://github.com/Nami3Piece/blog-generator-edit-tool/issues
2. 描述问题或建议
3. 我们会尽快回复

欢迎所有团队成员贡献代码和改进！

---

## File Descriptions | 文件说明

**English**: Current version includes blog examples for four platforms:

**中文**: 当前版本包含四个平台的博客示例：

### 1. Medium (`medium.md`)

**English**:
- Format: Markdown
- Images: Relative path references
- Publishing steps:
  1. Log in to Medium
  2. Click "Write"
  3. Click "..." menu → "Import a story"
  4. Upload `medium.md` file
  5. Manually upload images from `blog_images/` folder

**中文**:
- 格式：Markdown
- 图片：使用相对路径引用
- 发布方式：
  1. 登录 Medium
  2. 点击「Write」
  3. 点击「...」菜单 → 「Import a story」
  4. 上传 `medium.md` 文件
  5. 手动上传图片（从 `blog_images/` 文件夹）

### 2. Mirror (`mirror.md`)

**English**:
- Format: Markdown (Web3 features supported)
- Images: Relative path references
- Publishing steps:
  1. Visit https://mirror.xyz
  2. Connect wallet
  3. Click "New Entry"
  4. Switch to Markdown mode
  5. Copy and paste `mirror.md` content
  6. Upload images to Mirror's image hosting
  7. Update image links

**中文**:
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

**English**:
- Format: Thread format (segmented)
- Each `---` separator represents one tweet
- Publishing steps:
  1. Visit https://x.com
  2. Create new tweet
  3. Post segment by segment (or use Thread feature)
  4. Manually insert images into corresponding tweets

**中文**:
- 格式：Thread 格式（分段）
- 每个 `---` 分隔符代表一条推文
- 发布方式：
  1. 访问 https://x.com
  2. 创建新推文
  3. 按照分段逐条发布（或使用 Thread 功能）
  4. 图片需要手动插入到对应推文中

### 4. Website Blog (`blog.html`)

**English**:
- Format: Complete HTML page
- Style: Built-in responsive design
- Publishing steps:
  1. Deploy directly to website `/blog/` directory
  2. Or integrate into existing blog system
  3. Adjust image paths to actual paths

**中文**:
- 格式：完整的 HTML 页面
- 样式：已内置响应式设计
- 发布方式：
  1. 直接部署到官网 `/blog/` 目录
  2. 或集成到现有博客系统
  3. 图片路径需要调整为实际路径

## Image Files | 图片文件

**English**: All images extracted to: `blog_images/`
- `image-01.png` to `image-13.png`
- Total: 13 images

**中文**: 所有图片已提取到：`blog_images/`
- `image-01.png` 到 `image-13.png`
- 共 13 张图片

---

## Pre-Publishing Preparation | 发布前准备

### Upload Images to Image Hosting (Recommended) | 上传图片到图床（推荐）

**English**: Use image hosting services (like Imgur, Cloudinary) to host images uniformly:

```bash
# Example: Using Imgur
# 1. Visit https://imgur.com/upload
# 2. Batch upload all images from blog_images/
# 3. Get URL for each image
# 4. Replace image paths in Markdown files
```

**中文**: 使用图床服务（如 Imgur、Cloudinary）统一托管图片：

```bash
# 示例：使用 Imgur
# 1. 访问 https://imgur.com/upload
# 2. 批量上传 blog_images/ 中的所有图片
# 3. 获取每张图片的 URL
# 4. 替换 Markdown 文件中的图片路径
```

### Or Deploy to Your Own Server | 或者部署到自己的服务器

```bash
# Upload to website static resources directory
# 上传到官网静态资源目录
scp -r ~/Desktop/blog_images/ user@server:/var/www/html/blog/images/

# Then use absolute paths in Markdown
# 然后在 Markdown 中使用绝对路径
# ![Image](https://yourdomain.com/blog/images/image-01.png)
```

---

## Quick Publishing Checklist | 快速发布清单

- [ ] Upload images to image hosting or server | 上传图片到图床或服务器
- [ ] Update image links in Markdown files | 更新 Markdown 文件中的图片链接
- [ ] Medium: Import `medium.md` | 导入 `medium.md`
- [ ] Mirror: Copy `mirror.md` content | 复制 `mirror.md` 内容
- [ ] X: Publish segments from `x-article.md` | 按 `x-article.md` 分段发布
- [ ] Website: Deploy `blog.html` and adjust image paths | 部署 `blog.html` 并调整图片路径

---

## Notes | 注意事项

**English**:
1. **Image Optimization**: Recommend compressing images for faster loading
2. **SEO**: Medium and website versions include meta tags
3. **Links**: Ensure all external links work properly
4. **Preview**: Preview on each platform before publishing
5. **Chinese Version**: Use the same template structure, replace English content with Chinese

**中文**:
1. **图片优化**：建议压缩图片以提升加载速度
2. **SEO**：Medium 和官网版本已包含 meta 标签
3. **链接**：确保所有外部链接正常工作
4. **预览**：发布前在各平台预览效果
5. **中文版本**：如需中文版，可以基于英文版翻译

---

## Bilingual Content | 双语内容

**English**: The blog text includes complete Chinese translation. If you need to publish a Chinese version, use the same template structure and replace English content with Chinese content.

**中文**: 博客文本包含完整的中文翻译，如需发布中文版本，可以使用相同的模板结构，替换英文内容为中文内容即可。

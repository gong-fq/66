# 英语语法AI助教 🎓

龚凤乾老师的智能英语语法学习平台

## 项目简介

这是一款专为中国学生设计的英语语法学习应用，采用DeepSeek大语言模型，提供智能化、个性化的语法辅导服务。

## 主要功能

### ✨ 核心特性

- **🤖 AI智能助教**: 采用DeepSeek大语言模型，提供专业准确的语法讲解
- **💬 文字交互**: 支持文字输入，快速获取语法解答
- **🎤 语音对话**: 支持语音输入输出，实现自然流畅的对话体验
- **🎯 精准分析**: 深入剖析句子结构，帮助学生理解语法规则
- **✏️ 语法纠错**: 即时发现并纠正语法错误
- **🌐 双语支持**: 中英双语界面和讲解
- **📚 丰富例句**: 提供大量真实例句，加深理解

### 🎨 用户体验

- 简洁优雅的界面设计
- 流畅的动画效果
- 响应式布局，支持移动端
- 快捷标签，一键输入常见问题

## 部署指南

### 前置要求

- Node.js 18+
- Netlify账号
- DeepSeek API密钥

### 部署步骤

#### 方法一：通过Netlify网站部署（推荐）

1. **获取DeepSeek API密钥**
   - 访问 [DeepSeek平台](https://platform.deepseek.com/)
   - 注册/登录账号
   - 在API Keys页面创建新的密钥

2. **准备代码**
   ```bash
   # 下载或克隆项目到本地
   cd english-grammar-ai-tutor
   ```

3. **部署到Netlify**
   - 登录 [Netlify](https://www.netlify.com/)
   - 点击 "Add new site" → "Import an existing project"
   - 选择 "Deploy manually"
   - 将项目文件夹拖拽上传

4. **配置环境变量**
   - 进入站点设置 (Site settings)
   - 点击 "Environment variables"
   - 添加环境变量：
     - Key: `DEEPSEEK_API_KEY`
     - Value: 你的DeepSeek API密钥

5. **重新部署**
   - 点击 "Deploys" 标签
   - 点击 "Trigger deploy" → "Deploy site"

#### 方法二：通过Git部署

1. **创建Git仓库**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. **推送到GitHub**
   ```bash
   # 在GitHub创建新仓库后
   git remote add origin YOUR_REPO_URL
   git push -u origin main
   ```

3. **在Netlify连接仓库**
   - 登录Netlify
   - "Add new site" → "Import an existing project"
   - 选择GitHub，授权并选择仓库
   - 配置构建设置（默认即可）
   - 添加环境变量 `DEEPSEEK_API_KEY`
   - 点击 "Deploy site"

### 本地开发

```bash
# 安装依赖
npm install

# 创建.env文件
echo "DEEPSEEK_API_KEY=your_api_key_here" > .env

# 启动本地开发服务器
npm run dev
```

访问 http://localhost:8888

## 项目结构

```
english-grammar-ai-tutor/
├── index.html                          # 主页面
├── netlify/
│   └── functions/
│       └── deepseek-proxy.js          # DeepSeek API代理函数
├── netlify.toml                        # Netlify配置
├── package.json                        # 项目配置
└── README.md                           # 项目文档
```

## 技术栈

- **前端**: HTML5, CSS3, JavaScript (ES6+)
- **AI模型**: DeepSeek Chat
- **部署平台**: Netlify
- **语音功能**: Web Speech API
- **字体**: Google Fonts (Crimson Pro, Noto Sans SC)

## 使用说明

### 文字交互模式

1. 点击"文字交流"标签
2. 在输入框输入语法问题或句子
3. 可使用快捷标签快速输入常见问题
4. 点击"发送问题"获取AI回复
5. 支持连续对话，保留上下文

### 语音对话模式

1. 点击"语音对话"标签
2. 点击麦克风按钮开始录音
3. 说出你的问题（支持中文）
4. AI会自动识别并回复
5. 回复会自动朗读，也可点击播放按钮重听

## 注意事项

### API密钥安全

- ⚠️ **切勿**将API密钥直接写入代码
- ✅ 使用Netlify环境变量存储
- ✅ 不要将.env文件提交到Git

### 浏览器兼容性

- 语音功能需要Chrome、Edge等支持Web Speech API的浏览器
- Safari部分支持，可能需要额外配置
- Firefox暂不支持语音识别功能

### API调用限制

- DeepSeek API有调用频率限制
- 建议监控API使用量
- 可在DeepSeek平台查看用量统计

## 常见问题

### Q: 语音识别不工作？
A: 确保使用Chrome浏览器，并允许网站访问麦克风权限。

### Q: API调用失败？
A: 检查环境变量是否正确配置，API密钥是否有效。

### Q: 如何修改AI助教的回复风格？
A: 编辑 `netlify/functions/deepseek-proxy.js` 中的 `systemPrompt`。

### Q: 如何添加更多快捷标签？
A: 在 `index.html` 的 `.quick-tags` 部分添加新的 `<span>` 元素。

## 更新日志

### v1.0.0 (2026-01-05)
- ✅ 初始版本发布
- ✅ 实现文字交互功能
- ✅ 实现语音对话功能
- ✅ 集成DeepSeek AI模型
- ✅ 响应式设计
- ✅ 双语支持

## 后续规划

- [ ] 添加用户认证系统
- [ ] 保存对话历史
- [ ] 语法练习题库
- [ ] 学习进度追踪
- [ ] 移动应用版本
- [ ] 支持更多语音引擎

## 贡献

欢迎提交Issue和Pull Request！

## 许可证

MIT License

## 联系方式

项目作者：龚凤乾老师（Mr. Gong）

---

⭐ 如果这个项目对你有帮助，请给它一个星标！

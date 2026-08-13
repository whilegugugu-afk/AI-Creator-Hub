# AI Creator Hub

一个基于 Vue 3 + Vite + Node.js 的真实 AI 创作平台。

## 功能

- AI 写作：真实大模型生成，可根据自然语言完成文章、文案、脚本、邮件等任务
- AI 绘画：真实图片生成 API
- AI 简历：真实大模型优化经历，禁止虚构信息
- AI 代码：真实大模型生成代码、解释方案和调试建议
- 作品管理、Prompt 库、历史记录、个人资料、深色模式
- API Key 仅放在后端 `.env`，不会提交到 GitHub

## 本地运行

### 1. 安装依赖

```bash
npm install
```

### 2. 配置 API Key

复制 `.env.example` 为 `.env`，填写：

```env
OPENAI_API_KEY=你的API_Key
OPENAI_MODEL=gpt-5.4-mini
OPENAI_IMAGE_MODEL=gpt-image-1
PORT=3001
```

不要把 `.env` 上传到 GitHub。

### 3. 启动后端

```bash
npm run server
```

看到 `AI Creator API running at http://localhost:3001` 即可。

### 4. 新开一个终端启动前端

```bash
npm run dev
```

打开 Vite 显示的地址。

## GitHub

项目已经配置 `.gitignore`，`.env`、`node_modules` 和构建产物不会上传。


## 启动顺序
1. 在项目目录运行 `npm run server`，保持窗口开启。
2. 另开终端运行 `npm run dev`。
3. 打开 Vite 提供的网页地址。

开发环境已配置 Vite `/api` 代理到 `http://localhost:3001`，避免浏览器直接跨端口请求造成连接/CORS问题。

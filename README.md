# 神秘塔罗 · 命运之牌

在线地址：**https://tarot-magic.pages.dev**

## 项目简介

一个交互式塔罗牌占卜网页，支持 1 张 / 3 张 / 5 张抽牌模式。包含全部 78 张塔罗牌的完整释义（牌面意象、正位含义、逆位含义、占卜结论、数字·元素·星象），支持 AI 智能解读和本地静态解析两种模式。适配电脑端和手机端。

## 文件结构

```
塔罗牌/
├── index.html          # 主页面（单文件，内含 HTML+CSS+JS）
├── _redirects           # Cloudflare Pages 部署配置
├── photo/               # 78张正面牌 + 1张背面牌
│   ├── card_00.jpg ~ card_77.jpg
│   └── card_back.jpg
└── README.md            # 本说明文档
```

## 功能特性

- **抽牌模式**：单张直断、圣三角（3张）、二择一（5张）
- **78张完整释义**：占卜结论、牌面意象、正位含义、逆位含义、数字·元素·星象
- **综合分析**：3张牌给出感情/事业/心态三方面建议；5张牌扩展为五方面
- **AI 解读**：支持接入硅基流动等免费 API，自动解读占卜结果
- **收藏系统**：localStorage 存储收藏牌
- **分享图生成**：一键生成占卜结果图片
- **每日一牌**：每日运势卡片
- **响应式布局**：适配电脑端和手机端

## 部署方法

### 本地运行
用浏览器直接打开 `index.html` 即可。推荐用本地服务器：
```
python -m http.server 8000
```
然后访问 `http://localhost:8000/index.html`

### Cloudflare Pages 部署
1. 将 `index.html`、`_redirects`、`photo` 文件夹打包为 zip
2. 进入 Cloudflare Workers & Pages → Create application → Pages → Upload assets
3. 拖入 zip 包，点击 Deploy

## 技术栈

- 纯前端 HTML + CSS + JavaScript（无框架依赖）
- CSS 3D 翻转动效
- Canvas 粒子背景
- localStorage 数据持久化

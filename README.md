# 情书页 - Valentine Love Letter

一个精美的情人节告白网页，带有打字机效果、飘落爱心、烟花和背景音乐。

[English](README_en.md)

## 效果预览

页面加载后会自动绽放烟花，配有飘落的爱心动画。进入信件后可以看到打字机效果，逐字显示情书内容。

## 功能特点

- **打字机效果** — 信件内容逐字显示，营造浪漫氛围
- **飘落爱心** — 持续的爱心从天而降
- **烟花特效** — 点击页面边缘或爱心触发烟花
- **背景音乐** — 循环播放你喜欢的音乐
- **深色/浅色主题** — 一键切换明暗模式
- **响应式设计** — 完美适配手机、平板和电脑
- **无障碍支持** — 支持减弱动效偏好

## 如何自定义

### 修改情书内容

打开 `index.html`，找到第 707 行的 `CONFIG.text` 对象，修改以下内容：

```javascript
text: {
    browserTitle: '致我最爱的你 - 情人节快乐',  // 浏览器标签标题
    pageTitle: 'To My Dearest',                  // 页面大标题
    subtitle: '情人节快乐！',                      // 副标题
    greeting: '亲爱的宝贝：',                       // 信件称呼
    signature: '永远爱你的',                       // 签名
    signatureName: 'Your Love',                   // 签名人名
    // ...
}
```

### 修改信件正文

找到第 726 行的 `loveLetter` 变量，直接修改信件内容：

```javascript
loveLetter: `今天是情人节，我想用这封信，把平时说不出口的话都告诉你。
...
`
```

### 更换音乐

将你的音乐文件（如 `love.mp3`）放在 `index.html` 同级目录，然后修改配置：

```javascript
music: {
    src: 'love.mp3',  // 改为你的音乐文件名
    // ...
}
```

### 调整动画效果

在 `CONFIG` 对象中可以找到以下配置：

| 配置项 | 说明 | 默认值 |
|--------|------|--------|
| `hearts.interval` | 爱心生成间隔（毫秒） | 850 |
| `hearts.probability` | 爱心生成概率（0-1） | 0.66 |
| `fireworks.burstCount` | 每次烟花数量 | 5 |
| `typing.normalDelay` | 普通字符打字速度（毫秒） | 62 |

数值越大动画越密集，但可能导致手机卡顿。

## 文件结构

```
love-page/
├── index.html    # 主页面（所有代码都在里面）
├── music.mp3     # 背景音乐（需自行添加）
└── README.md     # 说明文档
```

## 部署

本页面为纯静态 HTML，可直接上传到任意静态托管服务：

- GitHub Pages
- Vercel
- Netlify
- 阿里云 OSS
- 腾讯云 COS

## 浏览器兼容

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## 本地预览

双击 `index.html` 即可在浏览器中打开。若音乐无法播放，请确保 `music.mp3` 文件与 HTML 在同一目录。

---

Made with ❤️
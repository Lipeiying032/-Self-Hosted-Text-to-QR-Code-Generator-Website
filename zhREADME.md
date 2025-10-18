# 在线二维码生成器

> 基于 Cloudflare Workers 的轻量级在线二维码生成器，支持任意文本、网址、中文内容的即时生成。

[![Cloudflare Workers](https://img.shields.io/badge/Cloudflare-Workers-orange?logo=cloudflare)](https://workers.cloudflare.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/yourusername/qrcode-generator/pulls)

---

## 特性

- **极速部署** - 一键部署到 Cloudflare Workers，全球 CDN 加速
- **现代 UI** - 响应式设计，渐变背景，流畅动画效果
- **多语言支持** - 完美支持中文、日文、韩文等 Unicode 字符
- **移动友好** - 自适应手机、平板、桌面各种屏幕尺寸
- **无需存储** - 所有处理在前端完成，不存储任何用户数据
- **零依赖** - 所有代码内嵌，无需外部 CDN 或库文件
- **完全免费** - 基于 Cloudflare Workers 免费额度（每日 10 万次请求）

---

## 快速开始

### 部署到 Cloudflare Workers

1. 注册并登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. 进入 `Workers & Pages` > `Create Application` > `Create Worker`
3. 删除默认代码，将 `worker.js` 中的完整代码粘贴进去
4. 点击 `Save and Deploy`
5. 访问分配的 URL 即可使用

### 本地开发
1 直接复制代码
2 访问cloudflare，创建一个worker项目
3.点击"从Hello，world开始“
4.随便起个worker项目名称
5.点击下一步>保存并部署
6.跳转到worker主界面后点击>编辑代码
7.把默认代码删掉并粘贴worker.js内容
8.保存并部署
9.用cloudflare默认域名访问或者绑定自定义域名访问
10.使用该网站
---

## 使用说明

1. 在输入框中输入任意文本（网址、文本、中文、emoji 等）
2. 点击"生成二维码"按钮或按下 `Enter` 键
3. 二维码立即显示在下方，可右键保存或截图

### 支持的内容类型

- URL链接：`https://example.com`
- 纯文本：`Hello World`
- 中文内容：`你好世界`
- 联系方式：`tel:+8613800138000`
- 邮箱地址：`mailto:example@email.com`
- WiFi 配置：`WIFI:S:NetworkName;T:WPA;P:password;;`
- 任意 Unicode 字符

---

## 技术栈

- **运行环境**: Cloudflare Workers
- **前端**: HTML5 + CSS3 + Vanilla JavaScript
- **二维码生成**: QRCode.js (内嵌版本)
- **样式**: 响应式设计 + CSS3 动画

---

## 项目结构

```
qrcode-generator/
├── worker.js          # Cloudflare Worker 完整代码
├── README.md          # 项目说明文档
├── LICENSE            # MIT 许可证
└── .gitignore         # Git 忽略文件
```

---

## 自定义配置

### 修改二维码尺寸

在 `worker.js` 中找到以下代码并修改：

```javascript
new QRCode(qrcodeDiv, {
  text: text,
  width: 300,    // 修改宽度
  height: 300,   // 修改高度
  colorDark: "#000000",
  colorLight: "#ffffff"
});
```

---

## 多语言支持

该项目完美支持各种语言的二维码生成：

- 中文简体/繁体
- 日语（平假名/片假名/汉字）
- 韩语
- 俄语
- 阿拉伯语
- 所有 Unicode 字符

---

## 性能指标

| 指标 | 数值 |
|------|------|
| 首次加载 | < 500ms |
| 二维码生成 | < 100ms |
| 资源大小 | ~50KB |
| 全球延迟 | < 50ms |

---

## 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本项目
2. 创建特性分支 `git checkout -b feature/AmazingFeature`
3. 提交更改 `git commit -m 'Add some AmazingFeature'`
4. 推送到分支 `git push origin feature/AmazingFeature`
5. 开启 Pull Request

---

## 开发计划

- [ ] 支持自定义二维码颜色
- [ ] 添加 Logo 水印功能
- [ ] 支持批量生成
- [ ] 添加二维码下载功能
- [ ] 支持更多二维码样式
- [ ] 添加历史记录功能（本地存储）
- [ ] 暗黑模式支持

---

## 常见问题

**Q: 二维码生成失败怎么办？**

A: 请检查输入内容是否过长，建议单次生成内容不超过 2000 字符。


**Q: Cloudflare Workers 有流量限制吗？**

A: 免费版每天 10 万次请求，对个人使用完全够用。

**Q: 如何保存生成的二维码？**

A: 在二维码上右键选择"图片另存为"，或使用截图工具。

---

## 许可证

本项目采用 MIT 开源协议。

---

## 致谢

- [QRCode.js](https://github.com/davidshimjs/qrcodejs) - 二维码生成库
- [Cloudflare Workers](https://workers.cloudflare.com/) - 无服务器平台
- 所有贡献者和使用者

---

## 联系方式

如有问题或建议，欢迎通过以下方式联系：

- 提交 [Issue](https://github.com/Lipeiying032/qrcode-generator/issues)
- 发起 [Discussion](https://github.com/Lipeiying032/qrcode-generator/discussions)
- 邮件: shabishabia1976@gmail.com

---

<div align="center">

**如果这个项目对你有帮助，请给一个 ⭐ Star！**

Made with ❤️ by [Lipeiying032](https://github.com/Lipeiying032)

</div>

# Dycookie

一个**纯本地**的抖音 Cookie 获取工具（Android）。

> **无后门、无联网上传、无任何数据收集。**  
> 所有操作均在本地完成，Cookie 仅保存在你手机的剪贴板中。

## 功能说明

- 内置 WebView 打开抖音创作者中心（https://creator.douyin.com/）
- 使用桌面 UA，方便登录
- 登录成功后，点击右上角 **「获取Cookie」** 按钮
- 自动提取当前 Cookie + localStorage
- 生成标准 `state.json` 格式（可直接用于 Playwright / Puppeteer 等工具）
- 一键复制完整 JSON 到剪贴板

## 使用方法

1. 下载并安装 [Dycookie.APK](./Dycookie.APK)
2. 打开 APP，等待页面加载完成
3. 正常登录你的抖音账号
4. 登录成功后点击左上角橙色按钮 **「获取Cookie」**
5. 在弹窗中点击 **「复制」**，即可得到完整的 state.json

## 输出格式示例

```json
{
  "cookies": [
    {
      "name": "sessionid",
      "value": "xxxxxx",
      "domain": ".douyin.com",
      "path": "/",
      "expires": 1735689600,
      "httpOnly": true,
      "secure": true,
      "sameSite": "None"
    }
  ],
  "origins": [
    {
      "origin": "https://www.douyin.com",
      "localStorage": [
        {
          "name": "key",
          "value": "value"
        }
      ]
    }
  ]
}
```

## 安全声明

- **完全本地运行**：不请求任何第三方服务器
- **无后门**：代码开源，可自行审计
- **无数据上传**：提取的 Cookie 只会复制到你手机的剪贴板
- **仅供个人学习研究使用**，请遵守相关平台服务条款

## 系统要求

- Android 5.0 及以上
- 需要允许「未知来源」安装

## 作者

- GitHub: [SCARZQ](https://github.com/SCARZQ)

## 许可证

本项目仅供学习与个人使用，禁止用于任何商业或违法用途。

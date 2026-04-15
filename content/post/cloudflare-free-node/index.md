---
title: "2026 最强 Cloudflare 免费节点：永久可用 + 免费域名（10分钟搭建）"
description: "教你如何利用 Cloudflare Pages 搭建稳定节点，解锁 ChatGPT / Gemini，无需服务器成本。"
date: 2026-04-15
image: cover.jpg
categories:
    - 免费资源
tags:
    - Cloudflare
    - VPN
    - 科学上网
---

如果你在找一种真正“长期可用”的免费节点方案，那么 2026 年这套基于 **Cloudflare Pages** 的搭建方式，是目前最值得尝试的选择。

### 核心优势
* **完全免费**：无需购买服务器，利用 CF 的边缘计算能力。
* **极度稳定**：依托 Cloudflare 全球加速网络，不容易被封。
* **解锁能力**：轻松解锁 ChatGPT、Gemini 等 AI 平台。

---

## 🛠 准备工作

### 1. 注册免费域名
你需要一个属于自己的域名来托管到 Cloudflare：
* **方案 A**：[前往注册免费域名](https://ccwu.cc)（推荐选择 `.ccwu.cc` 或 `.us.ci` 结尾，永久免费）。
* **方案 B**：[备用注册地址](https://us.ci)。

### 2. 托管至 Cloudflare
注册并登录 [Cloudflare 官网](https://dash.cloudflare.com/)，将你获取到的免费域名添加并托管进去。

---

## 🚀 部署步骤

### 第一步：创建 KV 空间
在 CF 后台找到：**存储和数据库** -> **Workers KV**，创建一个名为 `KV` 的空间备用。

### 第二步：创建 Pages 并上传源码
1.  在 CF 后台找到 **Workers 和 Pages**，选择 **创建 Pages**。
2.  上传由 **CMliu** 开源的程序包（即 `main.zip`）。
3.  部署完成后，点击“继续处理站点”。

### 第三步：设置环境变量
1.  进入 **设置** > **环境变量** > **添加变量**。
2.  **变量名称**：`ADMIN`
3.  **变量值**：设置你的管理员登录密码。
4.  **绑定 KV**：在设置中选择 **绑定** > **KV 命名空间**，变量名称填 `KV`，并关联你第一步创建的空间。
5.  **重新部署**：返回“部署”选项卡，重新上传一次 `main.zip` 使变量生效。

### 第四步：绑定自定义域
1.  在 Pages 的 **自定义域** 选项卡，点击“设置自定义域”。
2.  输入你的次级域名（例如：`link.yourdomain.ccwu.cc`）。
3.  按照提示完成 CNAME 记录解析。

---

## 🌐 访问与使用

* **管理后台**：访问 `https://你的域名/admin`，输入你设置的 `ADMIN` 密码。
* **获取节点**：在后台可以直接复制 VLESS/Trojan 链接，或者获取自动订阅地址。
* **客户端推荐**：建议使用 [V2RayN](https://github.com/2dust/v2rayN/releases) 或 Clash Verge。

### ⚡️ 高级优选（高手进阶）
如果你追求更快的速度，可以在后台配置以下优选订阅地址：
* **优选订阅**：`Sub.Cmliussss.Net`
* **ProxyIP 订阅**：`ProxyIP.SG.CMLiussss.Net`（新加坡节点，低延迟）

---

> **结语**：这套方案真正实现了“零成本”科学上网。如果你在搭建过程中遇到 KV 绑定失败或其他问题，欢迎在下方留言，钱途哥为你解答！

# 陆壹的房间

一个基于静态资源构建的个人作品集网站，当前站点内容已调整为陆壹的个人展示页，可直接部署到静态托管平台。

当前线上目标域名：

https://hlpeng.cn/

## 项目特点

- 纯静态站点，无后端依赖
- 主页包含 3D 场景、动画和滚动交互效果
- 可直接通过 GitHub + Vercel 部署
- 页面文案、链接和站点信息已替换为个人版本

## 项目结构

```text
.
├─ index.html
├─ README.md
├─ vercel.json
├─ assets/
│  ├─ css/
│  ├─ font/
│  ├─ img/
│  └─ js/
└─ _assets/
   ├─ draco/
   ├─ images/
   ├─ models/
   └─ videos/
```

说明：

- index.html：站点主入口，主要页面文案、SEO 信息、链接入口都在这里
- assets/：前端样式、脚本、字体和图片等编译后的静态资源
- _assets/：运行时依赖资源，例如 3D 模型、视频、图片和 Draco 解码文件
- vercel.json：Vercel 静态部署配置，包含资源缓存策略

## 本地预览

这是一个静态网站，直接启动本地 HTTP 服务即可预览。

如果本机安装了 Python，可以在项目根目录运行：

```bash
python -m http.server 5500
```

然后在浏览器中访问：

```text
http://localhost:5500/
```

注意：

- 不建议直接双击打开 index.html
- 项目中存在以 /_assets/ 开头的绝对路径资源，必须通过本地服务器访问才能正常加载

## 部署方式

推荐使用 GitHub + Vercel：

1. 将项目推送到 GitHub 仓库
2. 在 Vercel 中导入该仓库
3. Framework Preset 选择 Other
4. 不需要填写 Build Command
5. Output Directory 保持默认或留空
6. 直接部署

当前项目不需要：

- Node.js 构建流程
- 数据库
- 后端接口
- 服务端渲染

## 已完成的定制内容

- 站点名称已改为“陆壹的房间”
- 首页英文标题已改为“LUYI PORTFOLIO”
- 页面主要日文内容已替换为中文
- 作品按钮已指向 https://hlpeng.cn
- 联系方式已改为邮箱 8135925@qq.com
- SEO 中的 canonical、og:url、og:image 已更新到 hlpeng.cn

## 常用修改入口

如果你后续还要继续修改，优先看这些位置：

- 首页文案与站点元信息：index.html
- Vercel 部署配置：vercel.json
- 资源缓存策略：vercel.json
- 样式外观：assets/css/index.70Gwt324.css
- 交互与 3D 行为：assets/js/Wrapper.astro_astro_type_script_index_0_lang.CWKz2Y_a.js

## 维护建议

- 修改前先备份 index.html
- 由于部分资源和结构来自构建产物，修改时尽量做小范围替换
- 如果需要长期维护，建议后续补一套可编辑的源代码工程，而不是只维护构建后的静态文件

## 版权说明

本仓库当前内容用于个人作品集展示。若继续公开部署，请确保你有权使用其中所有模型、图片、视频、字体及其他第三方资源。
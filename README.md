# 规划工作台 · 部署说明

这是一个纯静态网页应用（HTML + CSS + JS），无后端依赖，数据全部存在浏览器本地。

## 文件清单
- `index.html` — 主应用（全部功能都在这一个文件里）
- `manifest.json` — PWA 配置（添加到主屏幕用）
- `icon192.png` / `icon512.png` — 应用图标
- `apple-touch-icon.png` — iPhone 主屏幕图标

## 方式一：GitHub Pages（推荐，永久免费）

1. 注册/登录 https://github.com
2. 点右上角「+」→「New repository」
   - 仓库名随意，比如 `planner`
   - 选 **Public**
   - 勾选「Add a README file」
   - 点「Create repository」
3. 把这 5 个文件全部上传：
   - 点「Add file」→「Upload files」→ 拖入所有文件 →「Commit changes」
4. 开启 Pages：
   - 进入仓库「Settings」→ 左侧「Pages」
   - 「Source」选 `Deploy from a branch`
   - 「Branch」选 `main`，文件夹选 `/ (root)` →「Save」
5. 等待 1~2 分钟，页面顶部会出现你的链接：
   ```
   https://你的用户名.github.io/planner/
   ```

这个链接**永久免费、永不过期**，只要 GitHub 在它就在。

## 方式二：Vercel（全球 CDN，更快）

1. 注册 https://vercel.com（可用 GitHub 账号一键登录）
2. 点「Add New」→「Project」→「Import」你的 GitHub 仓库
   - 或选「Deploy」直接拖拽上传整个文件夹
3. 不用改任何设置，点「Deploy」
4. 几秒后得到链接：`https://你的项目名.vercel.app`

## 方式三：腾讯云 / 阿里云 静态网站

1. 开通「对象存储 COS / OSS」
2. 创建 Bucket，权限设为「公有读」
3. 上传所有文件
4. 开启「静态网站托管」，得到一个访问域名

## 添加到手机主屏幕

部署好之后，用手机浏览器打开链接：

- **iPhone**：Safari 打开 → 点底部「分享」→「添加到主屏幕」
- **安卓**：Chrome 打开 → 点右上角「⋮」→「添加到主屏幕」

添加后桌面会出现青瓷绿图标，点开全屏运行，无浏览器地址栏，像原生 App 一样。

## 数据说明

所有数据（打卡、记账、阅读进度）保存在浏览器本地（localStorage）。
- 同一浏览器/同一设备下数据持续保留
- 清除浏览器缓存会丢失数据
- 换设备或换浏览器数据不互通

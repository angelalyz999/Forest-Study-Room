# 森林自习室 · 部署说明（只需做一次）

## A. 建一个免费的 Firebase 项目（约 10 分钟）
1. 打开 https://console.firebase.google.com ，用 Google 账号登录 → 添加项目（名字随意，Google Analytics 可关闭）。
2. 左侧 Build → **Firestore Database** → 创建数据库 → 选「生产模式」→ 选离你近的地区。
3. 进入 Firestore 的 **规则 (Rules)** 页：把 `firestore.rules` 文件的全部内容粘贴进去，点「发布」。
4. 左侧 Build → **Authentication** → 开始使用 → 「登录方法」→ 启用 **Google** 和 **电子邮件/密码** 两项（Google 需要选一个支持邮箱）。
5. 项目设置（左上齿轮）→「你的应用」→ 点 `</>` 添加网页应用 → 注册后会显示 `firebaseConfig`。
6. 用文本编辑器打开 **`config.js`**，把里面的 `const firebaseConfig=...` 整行替换成你复制的 `firebaseConfig` 块，保存。（以后更新 index.html 时不要动 config.js。）

## B. 把网站放到网上（约 2 分钟）
1. 打开 https://app.netlify.com/drop ，把整个 `forest-study-room` 文件夹拖进去。
2. 它会给你一个网址，把网址发给朋友即可。

## 朋友怎么用
打开网址 → 用 Google 一键登录（或用邮箱注册）→ 首次输入昵称 → 点空位入座。同一个账号在任何设备登录，学习记录都在。

## 注意
- **必做**：Firebase → Authentication → 设置 → 已获授权的网域，把 Netlify 给你的网址（如 xxx.netlify.app）加进去，否则 Google 登录会报 unauthorized domain。
- 微信内置浏览器打不开 Google 登录，请用邮箱注册，或在手机浏览器里打开。
- Google 和 Firebase 在中国大陆通常需要特殊网络才能访问，大陆的朋友可能打不开。
- 「仅自己可见」的心得仍只是页面上隐藏；任务明细是真正私密的（规则已限制）。
- Firebase 免费额度对一个小自习室足够。

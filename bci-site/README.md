# 🧠 BCI 每日简报

> 脑机接口行业产品动态 · 学术前沿 · 市场洞察

**每工作日 12:00 自动更新**

---

## 📁 目录结构

```
bci-site/
├── index.html          ← 报告列表首页
├── CNAME               ← 自定义域名配置（bci.renue.com）
├── reports/            ← 各期报告HTML文件
│   ├── bci-report-2026-04-27-light.html
│   └── bci-report-2026-04-28-light.html
└── README.md
```

---

## 🚀 部署步骤

### Step 1：创建 GitHub 仓库

1. 打开 [github.com](https://github.com)，登录账号
2. 点击右上角 **+ → New repository**
3. 填写：
   - **Repository name**: `bci-daily`
   - **Description**: `🧠 BCI 每日简报 — 脑机接口行业产品动态与学术前沿`
   - 选择 **Public**（公开仓库才能用 GitHub Pages）
   - ✅ 勾选 **Add a README file**
4. 点击 **Create repository**

---

### Step 2：上传文件

在仓库页面点击 **Add file → Upload files**，拖入以下文件/文件夹：

- `index.html`
- `CNAME`
- `reports/` （整个文件夹）

然后点击 **Commit changes**

---

### Step 3：启用 GitHub Pages

1. 进入仓库 → **Settings**（顶部菜单）
2. 左侧菜单找到 **Pages**
3. 配置：
   - **Source**: Deploy from a branch
   - **Branch**: main / (root)
   - 点击 **Save**
4. 等待 1-2 分钟，页面会显示：`Your site is live at https://[your-username].github.io/bci-daily/`

---

### Step 4：绑定自定义域名 bci.renue.com

> ⚠️ 前提：你已拥有 `renue.com` 域名

#### 在 GitHub 端：
1. 进入仓库 → **Settings → Pages**
2. **Custom domain** 输入框填入：`bci.renue.com`
3. ✅ 勾选 **Enforce HTTPS**（会自动申请SSL证书）

#### 在域名 DNS 端（阿里云 / 腾讯云 / DNSPod）：
添加一条 **CNAME 记录**：

| 主机记录 | 记录类型 | 记录值 |
|---------|---------|--------|
| `bci`   | CNAME   | `[your-username].github.io.` |

> ⚠️ 记录值末尾的 `.` 不要漏

#### 验证：
DNS 生效后（约5分钟-24小时），访问 `https://bci.renue.com` 即可看到报告首页。

---

## ⚙️ 自动化更新（可选）

每天 12:00 的报告更新可以通过以下方式同步到仓库：

### 方式A：手动复制
报告生成后，将 `bci-report-YYYY-MM-DD-light.html` 复制到 `reports/` 目录，push 到 GitHub。

### 方式B：自动化脚本（进阶）
在 GitHub Actions 中添加定时任务，每次运行后自动 push 更新。
如需此方案，告知我，我来帮你写 `.github/workflows/deploy.yml`。

---

## 📝 发布内容规范

- 报告仅供行业交流，禁止未授权的商业转载
- 如需对外分享，请注明来源：**BCI每日简报 | bci.renue.com**
- 报告中引用的论文数据均来自公开学术资料

---

*由 WorkBuddy 自动化生成 · 2026年4月*

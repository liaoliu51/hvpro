# hv-analysis-pro 上传指南

## 📦 安装包位置

- **压缩包**: `/root/.openclaw/workspace/skills/hv-analysis-pro.tar.gz` (42KB)
- **源代码**: `/root/.openclaw/workspace/skills/hv-analysis-pro/`

---

## 🚀 上传到 GitHub 的方法

### 方法一：使用 GitHub Token（推荐）

1. **获取 GitHub Token**
   - 访问：https://github.com/settings/tokens
   - 点击 "Generate new token (classic)"
   - 勾选 `repo` 权限
   - 生成并复制 token

2. **配置 Token**
   ```bash
   # 将 token 保存到临时文件
   echo "ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" > ~/.github_token
   chmod 600 ~/.github_token
   ```

3. **推送代码**
   ```bash
   cd /root/.openclaw/workspace/skills/hv-analysis-pro
   
   # 创建 GitHub 仓库（手动或自动）
   # 访问 https://github.com/new 创建仓库 hv-analysis-pro
   
   # 添加远程仓库
   git remote add origin https://liaoliu51:YOUR_TOKEN@github.com/liaoliu51/hv-analysis-pro.git
   
   # 推送
   git push -u origin main
   ```

### 方法二：使用 SSH Key

1. **生成 SSH Key**
   ```bash
   ssh-keygen -t ed25519 -C "liaoliu51@users.noreply.github.com"
   ```

2. **添加 SSH Key 到 GitHub**
   - 访问：https://github.com/settings/keys
   - 点击 "New SSH key"
   - 粘贴 `~/.ssh/id_ed25519.pub` 内容

3. **推送代码**
   ```bash
   cd /root/.openclaw/workspace/skills/hv-analysis-pro
   git remote add origin git@github.com:liaoliu51/hv-analysis-pro.git
   git push -u origin main
   ```

### 方法三：手动上传（最简单）

1. **下载压缩包**到本地电脑
   ```bash
   # 通过 lightclaw_upload_file 上传到云存储
   # 或直接复制文件
   ```

2. **解压到本地**
   ```bash
   tar -xzvf hv-analysis-pro.tar.gz
   cd hv-analysis-pro
   ```

3. **通过 GitHub 网页上传**
   - 访问：https://github.com/new
   - 创建仓库 `hv-analysis-pro`
   - 点击 "uploading an existing file"
   - 拖拽文件到网页
   - 提交

---

## 📁 文件结构

```
hv-analysis-pro/
├── SKILL.md          # 技能定义（10KB）
├── README.md         # 使用说明（2.3KB）
├── _meta.json        # 元数据（636B）
├── scripts/
│   └── md_to_pdf.py  # PDF 生成脚本（14KB）
└── references/       # 参考资料目录
```

---

## ✅ 新增功能清单（v2.0 Pro）

### 4 个新增分析维度

1. **最赚钱业务分析** ⭐
   - 分业务收入构成
   - 分业务毛利率
   - 收入占比变化
   - 第二增长曲线识别

2. **转型情况分析** ⭐
   - 转型历史与动因
   - 转型路径（并购/自研/合作）
   - 转型成效评估
   - 转型风险分析

3. **同行优势劣势对比** ⭐
   - SWOT 分析框架
   - 6 大维度对比（技术/产品/市场/成本/管理/财务）
   - 竞品核心指标对比表

4. **股价弹性对比** ⭐
   - 历史涨幅对比（1 年/3 年/5 年）
   - 波动率与 Beta 值
   - 估值弹性（PE/PB 分位）
   - 资金偏好（机构/北向/融资）

### 优化项

- 金融数据维度从 3 个扩展到 6 个
- 篇幅上限从 30,000 字提升至 35,000 字
- 新增 Pro 版专项质检清单

---

## 🔗 GitHub 仓库信息

- **仓库名**: `hv-analysis-pro`
- **描述**: 横纵分析法 Pro - 廖势无双个人增强版，新增 4 个分析维度
- **主页**: https://github.com/liaoliu51/hv-analysis-pro
- **许可证**: MIT

---

## 📝 下一步

上传完成后，你可以：

1. **在 ClawHub 发布技能**（可选）
   - 访问：https://clawhub.ai
   - 提交技能包审核

2. **分享给其他人使用**
   - 通过 GitHub 仓库链接
   - 或直接发送压缩包

3. **持续更新维护**
   - 根据使用反馈优化分析维度
   - 更新版本号（v2.1, v2.2...）

---

_作者：廖势无双 🐢_
_更新时间：2026-04-23_

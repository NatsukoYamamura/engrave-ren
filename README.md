# 星语铭 GitHub Pages 静态版本

基于 data-main 结构的无后端静态纪念网站。

## 目录结构

```
github pages/
├── people/                  # 人物数据目录
│   └── example/            # 示例人物
│       ├── info.yml        # 人物信息配置
│       ├── page.md         # 生平介绍 (Markdown)
│       ├── page.zh_hant.md # 繁体中文版本
│       ├── page.en.md      # 英文版本
│       └── photos/         # 照片目录
│           └── profile.jpg # 头像
├── public/                 # 公共资源
│   ├── css/style.css       # 样式文件
│   └── js/main.js          # JavaScript
├── scripts/
│   └── build.js           # 构建脚本
├── package.json
├── index.html              # 主页 (构建生成)
└── about.html              # 关于我们
```

## 添加新人物

1. 在 `people/` 目录下创建新文件夹（如 `zhang-san/`）
2. 创建 `info.yml` 配置文件
3. 创建 `page.md` 生平介绍文件
4. 在 `photos/` 目录下添加头像

### info.yml 格式

```yaml
id: zhang-san
profileUrl: ${path}/photos/profile.jpg
info:
  出生: 2000-01-01
  去世: 2024-01-01
  年龄: 24
  地点: 北京
websites:
  Twitter: https://twitter.com/example
  Bilibili: https://bilibili.com
```

### page.md 格式

```yaml
---
name: 张三
desc: 一句话简介
---
# 生平介绍

在这里写人物的生平故事...

---

*本条目由XXX贡献*
```

## 构建和部署

```bash
# 安装依赖
npm install

# 构建
npm run build

# 本地预览
npm run serve
```

## 部署到 GitHub Pages

1. 创建 GitHub 仓库
2. 推送所有文件
3. 运行 `npm run build`
4. Settings → Pages → Source 选 `main` branch
5. 访问 `https://用户名.github.io/仓库名/`

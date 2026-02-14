# 星语铭 (engrave.ren)

一个基于 GitHub Pages 的纪念网站，用于纪念那些已经离开的人。

## 网址

https://NatsukoYamamura.github.io/engrave-ren

## 目录结构

```
/
├── index.html              # 首页 - 显示纪念人物列表
├── profile.html           # 个人纪念页面
├── about.html             # 关于页面
├── 404.html               # 404 错误页面
├── favicon.svg            # 网站图标
├── css/
│   └── style.css         # 样式文件
├── js/
│   ├── main.js           # 首页 JavaScript
│   └── profile.js        # 个人页面 JavaScript
├── images/
│   └── default-avatar.svg # 默认头像
└── data/
    ├── profiles.json      # 纪念人物 ID 列表
    └── people/
        └── [人物ID]/
            ├── info.json  # 基本信息
            ├── bio.md     # 生平介绍
            └── avatar.jpg # 头像图片
```

## 添加新人物

1. 在 `data/people/` 下创建新文件夹，文件夹名称即为人物 ID
2. 创建 `info.json` - 基本信息
3. 创建 `bio.md` - 生平介绍（支持 Markdown）
4. 添加 `avatar.jpg` - 头像图片（可选）

### info.json 格式

```json
{
  "id": "gqt",
  "name": "Ara",
  "handle": "aragqt",
  "aliases": "Gqt, Aragqt",
  "location": "法国巴黎",
  "birthDate": "2003-02-21",
  "passDate": "2025-06-22",
  "website": "https://example.com"
}
```

### 更新人物列表

在 `data/profiles.json` 中添加人物 ID：

```json
["gqt", "zheermao101", "新人物ID"]
```

## 评论系统

使用 [Utterances](https://utteranc.es) 基于 GitHub Issues 提供评论功能。

配置位于 `js/profile.js` 中的 `COMMENT_CONFIG`。

## 部署

1. 将文件推送到 GitHub 仓库
2. 进入仓库 Settings → Pages
3. 选择 Source 为 `main` 分支
4. 保存后即可访问

## 技术支持

由 [Novi的导航站](https://novihare.cn/) 提供技术支持

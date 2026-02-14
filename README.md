# 星语铭 - GitHub Pages 版本

## 项目结构

```
├── index.html          # 主页 - 显示人物列表
├── profile.html       # 个人资料页面模板
├── about.html         # 关于我们页面
├── 404.html           # 404错误页面
├── favicon.svg        # 网站图标
├── .nojekyll         # GitHub Pages 配置
├── css/
│   └── style.css     # 样式文件
├── js/
│   ├── main.js       # 主页JavaScript
│   └── profile.js    # 个人页面JavaScript
├── data/
│   └── profiles.json # 人物数据
└── images/
    └── default-avatar.svg  # 默认头像
```

## 数据格式

人物数据存储在 `data/profiles.json` 中，格式如下：

```json
{
  "id": "unique-id",
  "name": "姓名",
  "handle": "昵称/用户名",
  "aliases": "别名",
  "location": "地点",
  "birthDate": "出生日期",
  "passDate": "离开日期",
  "age": "年龄",
  "website": "网站链接",
  "bio": "生平介绍 (支持Markdown)",
  "summary": "一言总结",
  "contributor": "贡献者",
  "avatar": "头像路径"
}
```

## 添加新人

1. 编辑 `data/profiles.json` 文件
2. 添加新的人物对象
3. 提交更改到 GitHub

## 注意事项

- GitHub Pages 不支持服务端数据库，所有数据通过 JSON 文件存储
- 头像等图片文件应放在 `images/` 目录下
- 使用 URL 参数 `?id=xxx` 或 `?name=xxx` 访问个人页面

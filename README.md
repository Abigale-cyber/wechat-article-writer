# WeChat Article Writer

Claude Code Skill — 按 content-brief 写公众号完整文章。

## 功能

- 读取 content-brief.md，按大纲写公众号文章
- 分两阶段：先出 3 个标题候选 + 确认大纲，用户确认后再写全文
- 写前门控：检查 brief 的核心判断、读者定义、素材充足度
- 遵循公众号排版规范（字号15、段不超5行、蓝加粗）
- 遵循去AI痕迹规则
- 写后自检（标题、开头、正文、结尾、排版、AI痕迹）
- 完稿后自动串联 adversarial-content-review

## 安装

```bash
git clone https://github.com/Abigale-cyber/wechat-article-writer.git
ln -s /path/to/wechat-article-writer/wechat-article-writer ~/.claude/skills/wechat-article-writer
```

## 目录结构

```
├── _shared/                           # 与其他 writing skills 共享
│   ├── intermediate-format.md         # 中间产物格式规范
│   ├── core-workflow.md               # 七步写作流程 + 五大框架
│   ├── hook-and-ending.md             # 8种开头 + 5种结尾模板
│   ├── title-and-packaging.md         # 标题5大原则 + 8种标题模板
│   └── wechat-channel-profile.md      # 公众号排版规范
├── wechat-article-writer/
│   ├── SKILL.md                       # 主入口
│   └── references/
│       ├── framework-selection.md     # 框架选择 + 分段写作法 + 去AI痕迹
│       └── pre-write-checks.md        # 写前门控 + 写后自检清单
└── README.md
```

## 使用

```
用 wechat-article-writer skill，按 content-brief-xxx.md 写公众号文章
```

## 配套 Skills

- [content-brief-builder](https://github.com/Abigale-cyber/media-skills) — 选题 → Brief
- `adversarial-content-review` — 对抗式审稿（待构建）
- `wechat-draft-publisher` — 配图 + 发布草稿箱（待构建）

## License

MIT

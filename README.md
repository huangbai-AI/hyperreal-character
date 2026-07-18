# hyperreal-character

超真实人物生图 + 生视频提示词工作流 Skill（配合可灵 Kling CLI/MCP 使用）。

从一套经过验证的"超写实人物素材"提示词方法论中提炼：

- **图片提示词十层模板**：风格定调 → 构图机位 → 人物基础 → 发型头饰 → 服装配饰 →
  五官锚点 → 妆容 → 皮肤真实感（最高优先级）→ 光线 → 背景+质量词
- **视频提示词八段模板**：画面配置 → 首帧一致性锚定 → 皮肤质感重申 → 人设+声音 →
  情绪设定+强度分 → 分秒拆解 → 台词口型 → 表演要求+反向提示词
- **两段式生成流程**：`text_to_image` 生首帧 → 用户确认 → `image_to_video` 生情绪视频

## 安装

```bash
# Claude Code 个人 skill
cp -r hyperreal-character ~/.claude/skills/hyperreal-character
```

## 依赖

- [kling-cli skill](https://skills.sh/klingai-tech/skills)（可灵官方 CLI skill）：
  `npx skills add klingai-tech/skills`
- 可灵 CLI：中国区 `npm i -g @klingai/cli-cn`，海外区 `npm i -g @klingai/cli-global`，
  然后 `kling login`

## 文件结构

```
hyperreal-character/
├── SKILL.md                      # 主 skill：工作流 + 模板速查 + 翻车修复表
├── references/
│   ├── image-prompt.md           # 图片提示词十层模板详解 + 可复制骨架
│   ├── video-prompt.md           # 视频提示词八段模板详解 + 可复制骨架
│   └── examples.md               # 已验证范例对（现代哭戏 / 古装贵妇）
└── README.md
```

## License

MIT

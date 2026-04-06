# Skills

本项目包含自定义技能，用于扩展 AI 助手能力。

## 复制技能到 Openclaw

```bash
mkdir -p /Users/milestian/.openclaw/workspace/skills && for dir in */; do [ -d "$dir" ] && cp -r "${dir%/}" /Users/milestian/.openclaw/workspace/skills/; done
```

**说明：**
- 自动复制当前目录下所有子目录（技能）到目标位置
- 自动忽略普通文件，仅复制目录
- 若目标目录不存在则自动创建

**注意：** `${dir%/}` 用于移除目录名末尾的斜杠，确保复制的是目录本身而非其内容

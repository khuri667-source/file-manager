# File Manager — Claude Code Skill

管理输出目录的智能文件管家。扫描临时文件、同名版本混乱、无归属文件，逐项确认后清理。

## 安装

```bash
# 克隆到 Claude Code skills 目录
git clone https://github.com/khuri667-source/file-manager.git ~/.claude/skills/file-manager
```

或通过 Skills CLI：

```bash
npx skills add khuri667-source/file-manager
```

## 触发方式

### 手动触发
```
清理文件 / 整理文件 / 文件管家 / ClaudeJobs 太乱了
```

### 半自动触发
使用 `/remember` 保存偏好后自动提醒。

## 工作流程

1. **三层扫描**：临时文件 → 同名版本 → 无归属散落文件
2. **逐项确认**：每类问题列出后等待用户决定
3. **执行清理**：确认一项执行一项，输出总结

## 核心原则

- 不自动删除任何文件
- 不做归档/压缩
- 文件名判重，不做内容 hash
- 每步操作前展示大小，让用户判断值不值得删

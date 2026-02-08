# Landing 输出目录

本目录存放由 Landing Maker 生成的页面与需求文档。

## 目录结构

```
tests/
  YYYYMMDD-HHMMSS/      # 每个新上下文一个子文件夹
    demand.md           # 用户需求文档（生成前必填，便于后续使用和沟通）
    landing.html        # 初版
    landing-v2.html     # 第一次调整后
    landing-v3.html     # 第二次调整后
```

- **新上下文**：新会话、新需求 → 创建新时间戳文件夹
- **demand.md**：记录用户需求，生成前必须存在且用户已最终确认
- **调整**：同一需求的修改 → 同文件夹内生成新版本文件，不覆盖；同时更新 demand.md

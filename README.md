# 项目管理与协作平台

> 存放需求、设计、代码、测试等文档

## 目录结构

```
project-docs/
├── docs/
│   ├── 需求/          # PRD、产品需求文档
│   ├── 设计/          # 架构设计、技术方案
│   └── 测试/          # 测试用例、测试报告
├── src/               # 源代码
└── database/          # 数据库设计文件
```

## 角色分工

| 角色 | 职责 |
|------|------|
| 产品 / 需求专家 | 输出 PRD 等需求文档 → 放在 `docs/需求/` |
| 技术开发专家 | 架构设计、代码开发、数据库设计 → 放在 `docs/设计/`、`src/`、`database/` |
| 测试 / 质量专家 | 测试用例、测试报告 → 放在 `docs/测试/` |

## 如何贡献

1. 克隆仓库：`git clone https://github.com/jay870423/project-docs.git`
2. 创建分支：`git checkout -b feature/your-feature`
3. 提交更改：`git commit -m "描述你的更改"`
4. 推送分支：`git push origin feature/your-feature`
5. 创建 Pull Request

---

**项目仓库**: https://github.com/jay870423/project-docs

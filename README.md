# 类比修辞收集库

一个持续增补的经典类比修辞数据库，收录文学、哲学、管理、科技等跨领域的中英文精妙类比，当前 **120 条**。

## 项目结构

```
analogy-data.js         # 纯数据层：const analogies = [...] 数组
analogy-collection.html # 展示层：CSS Columns 布局 + 毛玻璃控制栏
```

数据与展示分离，更新只动 `analogy-data.js`，HTML 页面引数据后自动渲染。

## 字段说明

每条类比包含：

| 字段 | 说明 |
|------|------|
| `quote` | 类比原文（中英对照用 `\n` 分隔） |
| `source` | 作者/出处 |
| `type` | 分类：人生哲理、文学艺术、商业经济、治理管理、科技创新、教育学习、哲学思辨、自然宇宙、人际情感 |
| `concept` | 核心概念（一句话概括） |
| `interpretation` | 深度解读：为什么这个类比精彩 |
| `alsoUse` | 可复用场景 |
| `lang` | 语言标识 |
| `date` | 入库日期 |

## 数据更新

- 每次增量更新 5–15 条
- 来源：公开文章、书籍、演讲的经典类比
- 去重后通过脚本追加到 `analogy-data.js` 末尾
- 提交前经 `node --check` 语法验证

## 与博客联动

此仓库同步部署在个人博客：

👉 **[luowenpeng.com/analogy-collection.html](https://luowenpeng.com/analogy-collection.html)**

博客基于 GitHub Pages + Docsify 构建，引用同一 `analogy-data.js` 数据源。以 CSS Columns 多栏布局 + 毛玻璃筛选栏呈现，支持按类型、语言过滤。

## 许可证

数据整理归本项目，引用的类比原文版权归原作者所有。

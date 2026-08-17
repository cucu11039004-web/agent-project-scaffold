# 架构决策记录 (ADR)

本目录存放架构决策记录（Architecture Decision Record）。每个重大、难以推翻、有真实
取舍的决策一份文件，按 `0001-xxx.md` 编号；**只追加不回改**，改主意时写新篇并注明
supersedes 旧篇。由 grill-with-docs / domain-modeling 在拷打过程中产出。

命名：`NNNN-<短横线标题>.md`（如 `0001-use-event-sourcing-for-orders.md`）。

建议每篇包含：背景（Context）、决策（Decision）、备选方案（Alternatives）、
后果（Consequences）。仅当"难以推翻 + 无背景会困惑 + 是真实取舍"三者都成立时才建。

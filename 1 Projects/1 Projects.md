---
aliases:
  - 项目
para: project
tags:
  - project
---

> [!abstract] 摘要
> 项目（有明确开始‑结束日期），例如任务清单、进度报告、和结果总结。

## No. of Projects 

```dataview
list without id length(rows.file.name)
from "1 Projects"
where para = "project" AND file.name != this.file.name
GROUP BY 1
```

```dataview
TABLE without id domain as "Area", rows.file.link as "Projects"
FROM "1 Projects"
WHERE file.name != "1 Projects" AND para = "project" AND domain
FLATTEN domain
GROUP BY domain
SORT domain
```

```dataview 
TABLE start_date as "开始日期", by-when as "截止日期", status as "状态"
FROM "1 Projects"
WHERE file.name != "1 Projects" AND para = "project"
SORT file.mtime desc
LIMIT 10
```

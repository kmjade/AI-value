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
where para = "projects"
group by 1
```

```dataview
Table without id domain as "Area", sort(rows.file.link) as Projects
FROM "1 Projects"
WHERE file.name != "1 Projects" and contains(para, "project")
FLATTEN domain
GROUP BY domain
SORT domain
```

```dataview 
table start_date, by-when, status from "1 Projects"
SORT file.mtime desc
LIMIT 10
```

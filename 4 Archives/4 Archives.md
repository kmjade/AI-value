---
aliases:
  - 归档
para: archives
---

> [!info]
> 已完成的项目、领域或资源，我不再需要或感兴趣项目、过期的方案

## No. of Archives [[归档]] 🗑️ 
```dataview
list without id length(rows.file.name)
from "4 Archives"
where para = "archive" AND file.name != this.file.name
group by 1
```

```dataview
TABLE WITHOUT ID file.link as "Archive", length(file.inlinks) as "No. of Linked Files"
FROM "4 Archives"
WHERE para = "archive" AND file.name != this.file.name
SORT length(file.inlinks) desc
```

> [!tldr]- Detailed
> ```dataview
> table file.inlinks as "Linked Files"
> from "4 Archives" 
> where para = "archive"  AND file.name != this.file.name
> sort file.name
> ```

 
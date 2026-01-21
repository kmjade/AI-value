# AI-value

PARA Methodology

> Projects, Areas, Resources, Archives

---

## English

### Overview

PARA is a productivity methodology by [Tiago Forte](https://fortelabs.co/) for organizing personal knowledge and tasks.

### The Four Categories

| Category | Description | Example |
|----------|-------------|---------|
| **Projects** | Short-term efforts with a clear goal and deadline | "Launch new website", "Complete tax return" |
| **Areas** | Long-term responsibilities with no deadline | "Health", "Finance", "Professional development" |
| **Resources** | Topics of ongoing interest | "Productivity tips", "Cooking recipes", "Marketing research" |
| **Archives** | Completed or inactive items | Old projects, outdated resources |

### How to Use

1. **Projects**: Create a new markdown file for each project. Use the `_template.md` as a starting point.
2. **Areas**: Add files for ongoing responsibilities you need to maintain.
3. **Resources**: Store information on topics you're interested in or researching.
4. **Archives**: Move completed projects or inactive items here when done.

### Tips

- Review Projects weekly
- Review Areas monthly
- Archive items regularly to keep your system clean
- Keep file names descriptive and concise

---

## Folder Structure

```
AI-value/
├── 0 Personals/
│   └── 📥 00_InBox/    - Inbox for quick capture of ideas
├── 1 Projects/         - Active projects with deadlines
├── 2 Areas/            - Ongoing responsibilities
├── 3 Resources/        - Topics of interest and reference materials
├── 4 Archives/         - Completed/inactive items
├── 5 Zettels/         - Atomic notes (Zettelkasten system)
├── _Template/          - Templates for new notes
├── _meta/             - System metadata and configuration
├── _Cache/            - PARA library cache
└── .obsidian/         - Obsidian plugin settings
```

### Extended Structure

- **InBox** (`0 Personals/📥 00_InBox/`): Temporary collection for quick capture of ideas, notes, and references before organizing them into PARA categories
- **Zettels** (`5 Zettels/`): Atomic notes system for creating a knowledge network using the Zettelkasten methodology

---

## Workflow

### 1. Capture
- Add new information to `0 Personals/📥 00_InBox/` for quick capture
- Don't worry about organization during capture phase

### 2. Process
- Regularly review InBox items
- Categorize each item into one of the four PARA categories:
  - Is it a **Project**? → `1 Projects/`
  - Is it an **Area** of responsibility? → `2 Areas/`
  - Is it a **Resource** or reference material? → `3 Resources/`
  - Is it completed or inactive? → `4 Archives/`

### 3. Organize
- Create descriptive file names
- Use proper folder structure
- Add relevant tags and metadata

### 4. Connect
- Use wikilinks `[[Note Name]]` to connect related notes
- Create atomic notes in `5 Zettels/` for knowledge networking
- Link Zettels to PARA categories as needed

### 5. Review
- **Weekly**: Review active Projects
- **Monthly**: Review Areas
- **Quarterly**: Clean up and archive

---

## Obsidian Integration

This vault is optimized for Obsidian with the following features:

### Frontmatter Properties

Add metadata to your notes:

```yaml
---
title: My Note
date: 2024-01-15
tags:
  - project
  - important
status: in-progress
priority: high
---
```

### Wikilinks

- `[[Note Name]]` - Internal link to another note
- `[[Note Name|Display Text]]` - Link with custom display text
- `[[Note Name#Heading]]` - Link to specific heading
- `![[Embedded Note]]` - Embed note content

### Callouts

Use callouts for emphasized content:

```markdown
> [!note] Note
> Important information

> [!tip] Tip
> Helpful suggestion

> [!warning] Warning
> Caution needed
```

### Tags

Use tags for categorization:
- `#project` - Project-related notes
- `#area` - Area-related notes
- `#resource` - Resource-related notes
- `#archive` - Archived items

---

## Zettelkasten System

### What is Zettelkasten?

Zettelkasten (German for "slip box") is a method of note-taking and personal knowledge management. It emphasizes creating atomic, self-contained notes that are heavily interlinked.

### Creating Atomic Notes

1. Keep notes focused on a single idea
2. Make notes self-contained (don't assume context)
3. Use unique IDs for reference
4. Link related concepts using wikilinks

### Example

```markdown
# 2024-01-15 - Atomic Note

The Zettelkasten method emphasizes creating atomic notes that focus on a single idea.

Related:
- [[2024-01-16 - Linking Notes]]
- [[3 Resources/Productivity]]
```

---

## PARA Commands

Use Claude Code commands to manage your PARA library:

| Command | Purpose |
|---------|---------|
| `/para-库概览` | Display PARA library overview and statistics |
| `/para-整理收集` | Organize InBox contents by PARA principles |

---

## Best Practices

1. **Start Simple**: Don't overcomplicate. Begin with basic capture and organize.
2. **Consistent Naming**: Use descriptive, consistent file names.
3. **Regular Review**: Schedule regular reviews of your PARA system.
4. **Link Everything**: Use wikilinks to create connections between notes.
5. **Keep It Active**: Move items to Archives only when truly inactive.
6. **Use Templates**: Start with `_template.md` for consistent formatting.
7. **Tag Wisely**: Use tags thoughtfully for easy retrieval.

---

## License

This project is licensed under the Apache 2.0 License.

---

## Credits

- [PARA Method](https://fortelabs.co/) by Tiago Forte
- [Obsidian](https://obsidian.md/) - Knowledge base application
- [Zettelkasten](https://zettelkasten.de/) - Note-taking methodology



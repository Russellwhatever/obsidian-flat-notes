[English](README.md) | [中文](示例库/Archive/示例库说明.md)

# Obsidian Flat Notes

An example Obsidian vault demonstrating how to manage notes without folders,
using links, tags, and index notes instead of hierarchical structures.

---

## Background

Although Obsidian has grown into one of the most powerful bidirectional note-taking tools,  
with countless plugins and configuration options, its co-founder **Steph Ango (kepano)** follows a few minimalist principles when managing his own vault[^1].

One of them is simple but radical:

> Do not build complex folder hierarchies.  
> Organize notes with links and tags instead.

This repository provides a **practical, working example** of such a system.

---

## What This Vault Demonstrates

This example vault shows how to manage notes in a **non-hierarchical (flat) structure**, mainly based on:

- **Index Notes**
- **Tags (with hierarchy)**
- **Bidirectional links**

Core plugins used:

- **Index Notes**
- **Templater**
- **QuickAdd**

Folders exist only for technical or archival purposes, not as the primary organizational method.

---

## Entry Point

This vault has **a single main entry point**:

- [[Dashboard]]

The Dashboard is divided into two parts:
- **Pinned notes** (top)
- **Project-based or thematic index notes** (bottom), such as:
  - Projects
  - Literature
  - Work logs

If you use daily notes, your workflow can also start from the daily note and link back into the system.

---

## Creating Notes (Folderless Workflow)

Without relying on folders, you no longer need to decide *where* a note belongs.

Recommended ways to create notes:
- `Ctrl + O` → type a new note name
- Create a new note directly using `[[New Note]]` from an existing note

After creating a note:
- Add **tags** to describe its meaning and context
- Optionally set a `title` field in frontmatter for better previews

---

## Index Notes & Tag Hierarchy

Index notes (e.g. `[[Archive/Project A|Project A]]`) automatically collect notes using tags.

How it works:
- Add a tag like `#projects/project-a` to your notes
- In the corresponding index note, add a tag:
  - `#projects/project-a/idx`

This index note will then aggregate all related notes.

To create a **meta-index** (like the Dashboard):
- Add an additional tag:
  - `#projects/meta_idx`

This allows index notes themselves to be collected and displayed.

---

## Work Logs

Work logs are created via a **QuickAdd template**.

Usage:
- Press `Alt + Q`
- Press Enter
- A timestamp-based work log note is created automatically

Features:
- Tags link logs to projects
- `title` metadata enables preview in index notes

---

## Daily Notes Template

The daily note template is located at:

- `[[Archive/Templates/日记模板|Daily Note Template]]`

It is created automatically when clicking a date in the calendar.

Each daily note provides:
1. **Notes of the Day** – newly created or modified notes
2. **Literature of the Day** – newly added references
3. **Tasks Completed Today**

Implementation:
- Notes & literature: Obsidian **Base** (official plugin)
- Tasks: **Dataview**

All entries are clickable and link back to their original notes.

---

## Literature & Task Management

From the pinned notes on the Dashboard, you can access:

- `[[Archive/任务汇总|Task Overview]]`

This page shows:
- Unread literature (via Base queries)
- Pending tasks (via Dataview)

All items link back to their source notes for quick context switching.

---

## Optional but Recommended

The following components are **not strictly required**, but highly recommended:

- Daily notes for temporal context
- Literature management via **Citations**
  - `Alt + E` to insert a reference
  - `Ctrl + Shift + O` to open literature notes

When used together, they significantly improve discoverability and reduce cognitive load.

---

## Philosophy

This vault is designed to:
- Reduce over-classification
- Avoid premature structure
- Let structure **emerge from usage**
- Support notes belonging to multiple contexts naturally

It reflects a workflow refined through continuous personal use and iteration.

---

## Who This Is For

- Obsidian users curious about **folderless workflows**
- PKM / Zettelkasten practitioners
- Users overwhelmed by complex folder trees
- Anyone who wants a **scalable, link-first note system**

---

## References

[^1]: https://stephango.com/vault  
[^2]: This vault: https://github.com/Russellwhatever/obsidian-flat-notes

# Navigation Rules

The lifecycle folders answer where files live. A separate navigation layer answers how humans and AI should enter and move through the workspace.

## Three Navigation Surfaces

| Surface | Purpose | Where |
| --- | --- | --- |
| Home | Launch page for common actions | `00_System/00-Home.md` |
| Maps | Cross-folder routes, topic maps, project maps | `00_System/10_Maps/` |
| Guides | Local folder instructions | `00_Guide/` inside each lifecycle folder |

## Writing Principles

- Navigation pages use links, short descriptions, reading paths, and question lists.
- Do not copy full content into navigation pages.
- A content page can appear in multiple maps.
- Map titles should clearly state their navigation scope.
- Links may be followed by a one-sentence explanation of why the target matters.

## What Belongs Where

- **Home**: common actions, today's entry points, recent changes. Keep short.
- **Maps**: topic routes, project routes, source routes, output routes. Organize by theme, not by folder.
- **Guides**: folder purpose, common entry points, local rules. One guide per lifecycle folder.

## Prohibited

- Do not copy entire articles or raw notes into navigation pages.
- Do not move content files just to make a map look clean.
- Do not write unverified AI output as confirmed conclusions in maps.
- Do not use navigation pages as operation logs.

## AI Maintenance

AI may:

- Create map pages.
- Add links and one-sentence descriptions to maps.
- Suggest pages from Inbox/Knowledge/Projects/Outputs to include in maps.
- Identify broken links, duplicate entries, or oversized lists in maps.

AI must not without confirmation:

- Batch move content files referenced by maps.
- Batch rename pages referenced by maps.
- Delete map links unless confirmed broken or replaced.

## Health Check

- Is `00-Home.md` the single launch page?
- Do map pages have descriptions, not just link dumps?
- Are important knowledge pages referenced by at least one map?
- Are Inbox materials lingering in maps without a plan to process them?

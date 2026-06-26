# FAQ

## Is this only for Obsidian?

No. Obsidian is one adapter. The main project is about AI-managed workspaces in general.

## Is this a note-taking method?

Not exactly. It is a governance layer for file workflows: where things go, what AI can do, what needs confirmation, and how changes are logged.

## Why have a centralized rules folder?

Because different AI tools read different entry files. Centralized rules prevent every tool from carrying a slightly different version of the truth.

## Why keep AI entry files short?

Entry files should route agents to the rules. If detailed rules are copied into every entry file, they drift and conflict.

## Why require operation logs?

AI work should be reviewable. A future human should know what changed, why, and under which rules.

## Why not let AI reorganize everything automatically?

Because large automatic migrations hide risk. The safer pattern is review first, confirm, then execute a small batch.

## Can this work with Git repositories?

Yes, especially for documentation and workflow folders. Be careful not to mix workspace governance rules with product code ownership rules unless that is intentional.

## Can teams use it?

Yes, but teams should add ownership, review, permissions, and privacy rules.

## Can I translate the rules?

Yes. Keep path examples stable and update AI prompts accordingly.
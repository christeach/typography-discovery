# Typography Discovery

A Claude Code skill for researching, comparing, and implementing distinctive web typography without automatically falling back to generic font defaults.

## Install

Copy the skill directory into your project:

```text
your-project/
└── .claude/
    └── skills/
        └── typography-discovery/
            └── SKILL.md
```

Then invoke it in Claude Code with:

```text
/typography-discovery
```

For a personal installation available across projects, place it in the user-level Claude skills directory supported by your Claude Code version.

## Test on an existing project

Start with a safe audit and preview. This prompt asks Claude not to modify production files before you approve a direction:

> Use the typography-discovery skill to audit this existing project and run a controlled typography experiment. Do not modify production files yet. Inspect the current typography, identify the project's visual direction, and research alternatives using the resources in the skill. Present three distinct directions with font names, source links, verified license information, and rationale. If possible, create an isolated preview using actual project content. Keep layout, colors, spacing, copy, and functionality unchanged. Wait for approval before implementing.

## What it covers

- Existing-project audit and controlled scope
- Discovery across independent foundries and directories
- License verification and glyph/language coverage
- Typographic directions and specimens
- Self-hosting, font loading, responsive checks, and final reporting

The directories listed in the skill are discovery sources, not blanket guarantees of licensing. Verify the exact license for each font family and version before use.

## Scope

The skill does not automatically redesign a project. It preserves existing UI and waits for approval before production changes unless autonomous implementation was explicitly requested.

---
name: skillsmith
description: Expert architect for designing production-quality Agent Skills. Use when creating new skills, refactoring existing skills, converting reusable prompts into skills, or designing modular skill collections.
license: MIT
metadata:
  author: Vignesh Prasad
  github: https://github.com/ViGi-P/skillsmith
  version: "1.0.0"
  purpose: meta-skill
---

# Skillsmith

Design Agent Skills as reusable software components—not as large prompts.

Your objective is to produce skills that are discoverable, composable, maintainable, and token-efficient.

If official documentation is available, treat it as the source of truth. Otherwise, follow the provided specification.

---

# Principles

| Prefer | Avoid |
|--------|-------|
| Single responsibility | God skills |
| Progressive disclosure | Bloated `SKILL.md` files |
| Focused references | Duplicate documentation |
| Modular design | Overlapping responsibilities |
| Searchable descriptions | Generic descriptions |
| Scripts for executable logic | Large code blocks in markdown |
| Assets for reusable resources | Embedded templates or schemas |
| Deterministic workflows | Ambiguous instructions |
| Token efficiency | Repetition |

---

# Workflow

## 1. Evaluate

Determine whether the request should become a skill.

A skill should represent a reusable capability.

If the request is better solved by a script, template, documentation, or a one-time prompt, recommend that instead.

Define:

- responsibility
- intended users
- activation criteria
- inputs
- outputs
- constraints
- dependencies
- edge cases

If multiple unrelated capabilities exist, split them into separate skills.

---

## 2. Design

Design the directory structure before writing files.

Create only the directories that add value.

Typical layout:

```
skill-name/
├── SKILL.md
├── references/
├── scripts/
└── assets/
```

Decide where each piece of information belongs.

### SKILL.md

Keep concise.

Include only:

- activation criteria
- workflow
- important rules
- validation
- references to supporting files

### references/

Store:

- technical documentation
- APIs
- algorithms
- schemas
- FAQs
- workflows

### scripts/

Store executable logic.

Scripts should validate inputs, document dependencies, and fail predictably.

### assets/

Store reusable resources such as:

- templates
- sample data
- configuration files
- diagrams
- example documents

---

## 3. Implement

Generate:

- directory tree
- valid frontmatter
- concise `SKILL.md`
- supporting reference files
- scripts when appropriate
- assets when appropriate

Descriptions should explain:

- what the skill does
- when another agent should activate it

Assume the description will be used for discovery.

---

## 4. Review

Before finalizing, verify:

- specification compliant
- single responsibility
- discoverable
- modular
- maintainable
- progressively disclosed
- minimal duplication
- token efficient

Validate against:

`references/constraints.md`

If any issue is found, revise before returning the skill.

---

# Output

Unless instructed otherwise, always provide:

1. Complete directory tree
2. Complete contents of every generated file
3. Valid relative file references
4. Brief design notes explaining important architectural decisions

---

# Final Check

Before returning the skill, ask:

> If this were published in a large public registry, would another agent reliably discover it, understand when to activate it, compose it with other skills, and successfully execute it without additional explanation?

If the answer is not an unqualified **yes**, continue refining the design.

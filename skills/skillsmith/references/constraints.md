# Constraints

Use this document to validate generated skills.

## Directory

| Required | Optional |
|----------|----------|
| `SKILL.md` | `references/` |
| | `scripts/` |
| | `assets/` |

Create optional directories only when needed.

---

## Frontmatter

| Field | Required | Rules |
|--------|----------|------|
| `name` | ✓ | 1–64 chars, lowercase letters/numbers/hyphens, no leading/trailing/consecutive hyphens, matches directory |
| `description` | ✓ | Explains **what** the skill does and **when** to use it (≤1024 chars) |
| `license` | | Include only if applicable |
| `compatibility` | | Include only when environment requirements exist |
| `metadata` | | Optional metadata |
| `allowed-tools` | | Optional |

---

## SKILL.md

Keep concise.

Contains:

- activation criteria
- workflow
- constraints
- validation
- references

Move detailed content elsewhere.

---

## File Placement

| Content | Location |
|---------|----------|
| APIs | `references/` |
| Algorithms | `references/` |
| Schemas | `references/` |
| Templates | `assets/` |
| Example documents | `assets/` |
| Executable logic | `scripts/` |

---

## References

- Use relative paths.
- Avoid deep reference chains.
- Prefer multiple focused files.

---

## Validation

Before returning:

- ✓ Valid frontmatter
- ✓ Directory matches `name`
- ✓ Useful description
- ✓ Correct file placement
- ✓ No duplicate documentation
- ✓ Progressive disclosure

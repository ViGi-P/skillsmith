# Skill Patterns

Choose the simplest pattern that fully represents the capability.

| Pattern | Primary Value | Typical Structure |
|---------|---------------|-------------------|
| Documentation | Instructions | `SKILL.md` + `references/` |
| Script-backed | Executable logic | `SKILL.md` + `scripts/` |
| Template | Reusable resources | `SKILL.md` + `assets/` |
| Reference Library | Large documentation | `SKILL.md` + `references/` |
| Review | Validation | `SKILL.md` + `references/` |

---

## Pattern Selection

| If the capability is primarily... | Choose... |
|-----------------------------------|-----------|
| Teaching | Documentation |
| Executing | Script-backed |
| Generating reusable files | Template |
| Explaining technical material | Reference Library |
| Evaluating quality | Review |

Use a hybrid only when a single pattern is insufficient.

---

## Typical Layouts

### Documentation

```
SKILL.md
references/
```

### Script-backed

```
SKILL.md
scripts/
references/
```

### Template

```
SKILL.md
assets/
```

### Hybrid

```text
SKILL.md
references/
scripts/
assets/
```

---

## Design Rules

- Prefer single responsibility.
- Minimize directory count.
- Create only useful files.
- Separate instructions from reference material.
- Keep `SKILL.md` as the entry point.
- Optimize for progressive disclosure.

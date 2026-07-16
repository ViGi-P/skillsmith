# Skill Smells

Review every generated skill before returning it.

| Smell | Preferred Fix |
|-------|----------------|
| God skill | Split into focused skills |
| Multiple responsibilities | Separate capabilities |
| Generic description | Add searchable activation criteria |
| Bloated `SKILL.md` | Move details into `references/` |
| Embedded templates | Move to `assets/` |
| Embedded schemas | Move to `assets/` |
| Embedded executable logic | Move to `scripts/` |
| Duplicate documentation | Keep one source of truth |
| Hidden assumptions | Document dependencies |
| Empty directories | Remove them |
| Dead references | Link or delete them |
| Undocumented scripts | Document requirements |
| Tight coupling | Separate responsibilities |
| Token waste | Remove repetition |

---

## Final Checklist

Before returning the skill:

- ✓ Reusable
- ✓ Discoverable
- ✓ Single responsibility
- ✓ Modular
- ✓ Maintainable
- ✓ Progressive disclosure
- ✓ Minimal duplication
- ✓ Token efficient

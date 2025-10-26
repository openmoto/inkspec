# Manuscript

This directory contains the final prose output from Inkspec projects.

## Purpose

After story specifications are approved and scene outlines are complete, the actual prose writing happens here. Each manuscript file traces back to approved specifications.

## Structure

Organize your manuscript however works best for your project:

### Option 1: Single File
```
manuscript/
└── the_last_lighthouse.md
```

### Option 2: By Chapter
```
manuscript/
├── chapter_01.md
├── chapter_02.md
└── chapter_03.md
```

### Option 3: By Story Arc
```
manuscript/
├── act_1_setup/
│   ├── chapter_01.md
│   └── chapter_02.md
├── act_2_confrontation/
│   └── chapter_03.md
└── act_3_resolution/
    └── chapter_04.md
```

## Linking to Specs

At the top of each manuscript file, reference the relevant specifications:

```markdown
<!-- Story Specs -->
<!-- Premise: PR-001 -->
<!-- Characters: CH-001, CH-002, CH-003 -->
<!-- Scenes: SC-001, SC-002, SC-003 -->
<!-- World: WB-001 -->

# Chapter 1: The Storm

[Your prose here...]
```

## Workflow

1. **Specs First** - Ensure all relevant story specs (PR, CH, SC, WB) are approved
2. **Scene Outline** - Create detailed SC-### for each scene before writing
3. **Draft Prose** - Write the actual narrative based on approved outlines
4. **Review** - Verify consistency with character voices, plot logic, and world rules
5. **Revise** - Implement feedback while maintaining spec integrity
6. **Finalize** - Merge approved prose to main manuscript

## Branching

Create branches for new writing work:

```bash
# For new scenes
git checkout -b story/1-SC-001-opening-storm

# For character development
git checkout -b revision/2-CH-001-protagonist-arc

# For revisions
git checkout -b revision/3-SC-001-dialogue-polish
```

## Commit Messages

Follow the Inkspec commit conventions:

```bash
git commit -m "scene(SC-001): add opening storm sequence"
git commit -m "character(CH-002): develop antagonist motivation"
git commit -m "revision(SC-001): strengthen dialogue and conflict"
```

## Remember

- ✅ **DO** write prose after specs are approved
- ✅ **DO** maintain consistency with character voices
- ✅ **DO** follow approved scene outlines
- ❌ **DON'T** write prose without scene specifications
- ❌ **DON'T** contradict established character or world specs
- ❌ **DON'T** merge unreviewed changes to main

**Specifications drive the story. Prose brings it to life.**

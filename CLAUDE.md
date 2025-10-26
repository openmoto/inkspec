# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

<!-- OPENSPEC:START -->
# OpenSpec Instructions

These instructions are for AI assistants working in this project.

Always open `@/openspec/AGENTS.md` when the request:
- Mentions planning or proposals (words like proposal, spec, change, plan)
- Introduces new capabilities, breaking changes, architecture shifts, or big performance/security work
- Sounds ambiguous and you need the authoritative spec before coding

Use `@/openspec/AGENTS.md` to learn:
- How to create and apply change proposals
- Spec format and conventions
- Project structure and guidelines

Keep this managed block so 'openspec update' can refresh the instructions.

<!-- OPENSPEC:END -->

## Project Purpose

This is a **collaborative fiction writing project** using a structured, specification-driven approach called **Specification-Driven Storytelling (SDS)**. The methodology ensures story consistency, character development, and thematic coherence through a rigorous workflow that requires all narrative development to be preceded by clear, mutually-agreed-upon story specifications.

## Specification-Driven Storytelling Protocol

The core protocol is defined in `00_spec_driven_storytelling_protocol.md`. As an AI assistant working on this project, you MUST follow this protocol without exception:

### Fundamental Principles

1. **Never write prose without approved specifications** - All scenes, dialogue, and narrative must have traceable story requirements
2. **Story specification is the single source of truth** - Refuse any writing that contradicts established character motivations, plot logic, or world rules
3. **Character consistency is mandatory** - Every line of dialogue and action must feel authentic to established personalities
4. **Show, don't tell** - Prioritize dramatic scenes, sensory details, and character actions over exposition
5. **Collaborative partnership** - Offer suggestions while respecting the author's vision and voice

### Three-Phase Workflow

#### Phase 1: Story Discovery & Specification
Before any writing begins, you must:
- Ask clarifying questions about central conflict, protagonist goals, genre conventions, emotional journey, themes, target word count, and story structure
- Propose comprehensive story specification including:
  - Story premise (one-sentence logline)
  - Character profiles (protagonist, antagonist, supporting characters)
  - Plot structure (beginning, middle, end with turning points)
  - Setting details (time, place, world-building)
  - Thematic elements and how they'll be explored
  - Style guidelines (tone, voice, POV, tense)
- Wait for author approval before proceeding
- Save approved spec to `/docs/story-spec/`

#### Phase 2: Scene Planning & Implementation
- Create detailed scene outlines specifying:
  - Scene purpose (plot advancement, character development, theme exploration)
  - Character goals within the scene
  - Conflict and obstacles
  - Character arc progression
  - Sensory details and atmosphere
- Draft scenes according to approved outlines
- Maintain consistency with character voices and story world

#### Phase 3: Revision & Refinement
- Verify story consistency with character motivations, plot logic, and world rules
- Implement author feedback while maintaining story integrity
- Only merge to main manuscript after final approval

### Story Spec Organization

Story specifications live under `/docs/story-spec/` with the following structure:

- **Premise specs**: `/docs/story-spec/premise/PR-###_story_title.md`
- **Character specs**: `/docs/story-spec/characters/CH-###_character_name.md`
- **Scene outlines**: `/docs/story-spec/scenes/SC-###_scene_description.md`
- **World-building**: `/docs/story-spec/world/WB-###_world_element.md`

### Branch and Commit Conventions

**Branch naming:**
- `story/[IssueNum]-SC-###-scene-description` - For new scenes
- `revision/[IssueNum]-CH-###-character-development` - For character work

**Commit messages:**
- `scene(SC-101): add opening confrontation scene`
- `character(CH-205): develop protagonist's backstory reveal`
- `revision(SC-101): strengthen dialogue and conflict`

### Mandatory Confirmation Prompts

**After drafting story spec:**
> "Here is the story specification for '[Story Title]'. It outlines the central conflict, character arcs, and thematic elements. Does this capture your vision for the story? Should I proceed with scene planning?"

**Before writing scenes:**
> "The story spec is approved. I'm ready to outline Scene SC-101: '[Scene Description]'. My plan is to focus on [character goal] while introducing [conflict/tension]. Does this scene outline align with your vision?"

**Before character development:**
> "I'm planning to develop [Character Name]'s backstory/motivation in this section. Based on our character spec CH-###, I'll reveal [specific character element]. Does this character development serve the story's needs?"

### Absolute Prohibitions

You MUST NOT:
- Begin writing prose without approved scene outline and character specifications
- Introduce new characters, plot elements, or world details that contradict the story spec
- Write dialogue inconsistent with established character voices
- Include scenes that don't serve plot progression, character development, or thematic exploration
- Make major plot or character changes without explicit author approval and spec updates

## Creative Writing Principles

Apply these principles to all narrative work:

- **Conflict in every scene** - Include tension through external conflict, internal struggle, or dramatic irony
- **Character agency** - Protagonists should drive the plot through choices and actions, not be passive
- **Emotional truth** - All reactions and dialogue should feel genuine to human experience and character psychology
- **Sensory immersion** - Use specific, concrete details to help readers experience the story world
- **Thematic integration** - Weave themes naturally through actions, dialogue, and plot events
- **Pacing variety** - Balance action, dialogue, introspection, and description
- **Stakes escalation** - Ensure consequences become increasingly important as the story progresses

## OpenSpec Integration

This project uses OpenSpec for change management. Story development follows the same spec-driven approach:

### Key Commands

```bash
# View active story changes
openspec list

# View existing story specifications
openspec list --specs

# Validate a story proposal
openspec validate [change-id] --strict

# Archive completed story work
openspec archive <change-id> --yes
```

### When to Create Proposals

Create OpenSpec proposals for:
- New story arcs or major plot developments
- Character arc changes or additions
- World-building that affects multiple scenes
- Breaking changes to established canon

Skip proposals for:
- Minor dialogue revisions
- Typo fixes
- Formatting changes
- Scene polish that doesn't change plot or character

## Working with This Repository

This is a **Windows environment** (platform: win32) located at `D:\personal-projects\novel-writing`.

The repository is **not a git repository** currently. If version control is needed, it should be initialized first.

### Directory Structure

```
novel-writing/
├── .claude/                    # Claude Code configuration
│   └── commands/               # Custom slash commands
├── openspec/                   # OpenSpec framework
│   ├── AGENTS.md              # OpenSpec workflow instructions
│   ├── project.md             # Project conventions (template)
│   ├── specs/                 # Current implemented capabilities
│   └── changes/               # Active and archived proposals
├── docs/                      # (To be created) Documentation
│   └── story-spec/            # Story specifications
│       ├── premise/           # Story premises (PR-###)
│       ├── characters/        # Character profiles (CH-###)
│       ├── scenes/            # Scene outlines (SC-###)
│       └── world/             # World-building (WB-###)
├── 00_spec_driven_storytelling_protocol.md  # Core SDS protocol
├── AGENTS.md                  # Agent instructions
└── CLAUDE.md                  # This file
```

### Custom Slash Commands

Available slash commands (from `.claude/commands/`):
- `/openspec:proposal` - Scaffold a new OpenSpec change and validate strictly
- `/openspec:archive` - Archive a deployed OpenSpec change and update specs
- `/openspec:apply` - Implement an approved OpenSpec change and keep tasks in sync

## Key Files to Reference

- **`00_spec_driven_storytelling_protocol.md`** - The authoritative protocol for all fiction writing work
- **`openspec/AGENTS.md`** - Detailed OpenSpec workflow instructions
- **`openspec/project.md`** - Project-specific conventions (currently template)

## Working with the Author

1. **Always ask before writing** - Confirm scene outlines, character decisions, and plot developments
2. **Provide options** - Offer multiple approaches for the author to choose from
3. **Explain your reasoning** - Share why certain narrative choices serve the story
4. **Respect the author's voice** - Match their tone, style, and creative vision
5. **Track progress transparently** - Use the TodoWrite tool for complex story work to give visibility into progress

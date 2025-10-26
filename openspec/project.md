# Inkspec Project Context

## Purpose

**Inkspec** is a specification-driven storytelling framework that applies software engineering discipline to fiction writing. The goal is to ensure story consistency, character authenticity, and thematic coherence by requiring all narrative development to be preceded by clear, mutually-agreed-upon specifications.

### Core Objectives
- Prevent plot holes and continuity errors through traceable requirements
- Maintain character consistency across all scenes and dialogue
- Enable collaborative fiction writing between human authors and AI assistants
- Track story evolution with the same rigor as software development
- Support multiple concurrent stories with independent specifications

## Framework Stack

### Core Technologies
- **OpenSpec** - Change management and specification tracking
- **Claude Code** - AI-assisted writing and spec validation
- **Git** - Version control for manuscripts and specifications
- **Markdown** - Documentation format for all specs and prose

### Story Specification Types
- **Premise Specs (PR-###)** - Story loglines, themes, structure
- **Character Specs (CH-###)** - Personalities, motivations, arcs
- **Scene Specs (SC-###)** - Scene outlines, conflict, sensory details
- **World Specs (WB-###)** - Settings, rules, world-building elements

## Project Conventions

### Specification Style

All story specifications MUST follow OpenSpec format:
- Use `## ADDED|MODIFIED|REMOVED|RENAMED Requirements` for deltas
- Every requirement MUST have at least one `#### Scenario:` block
- Scenarios use `**WHEN**` and `**THEN**` format
- Requirements use `SHALL` for normative statements

**Example:**
```markdown
### Requirement: Character Motivation
The protagonist SHALL be driven by a clear, consistent goal.

#### Scenario: Protagonist makes difficult choice
- **WHEN** forced to choose between safety and goal
- **THEN** protagonist chooses pursuit of goal, revealing core motivation
```

### File Naming Conventions

#### Story Specifications
- **Premise**: `PR-001_story_title.md` (lowercase, underscores)
- **Character**: `CH-001_character_name.md` (lowercase, underscores)
- **Scene**: `SC-001_brief_description.md` (lowercase, underscores)
- **World**: `WB-001_element_name.md` (lowercase, underscores)

**Examples:**
- `PR-001_the_last_lighthouse.md`
- `CH-001_elena_cross.md`
- `SC-001_opening_storm.md`
- `WB-001_lighthouse_magic_system.md`

#### Manuscript Files
- Single story: `story_title.md`
- By chapter: `chapter_01.md`, `chapter_02.md`
- By act: `act_1/chapter_01.md`

### Story Architecture Patterns

#### Three-Phase Workflow
1. **Story Discovery & Specification** - Define before writing
2. **Scene Planning & Implementation** - Outline before prose
3. **Revision & Refinement** - Verify consistency with specs

#### Specification Hierarchy
```
Premise (PR-###)
├── Characters (CH-###)
│   └── Character arcs and relationships
├── World (WB-###)
│   └── Settings and rules
└── Scenes (SC-###)
    └── Individual scene outlines
```

#### Change Proposal Pattern

**When to create OpenSpec changes:**
- New story arcs or major plot developments
- Character arc changes or new characters
- World-building that affects multiple scenes
- Breaking changes to established canon

**When to skip proposals:**
- Minor dialogue revisions
- Typo fixes or formatting
- Scene polish that doesn't change plot/character
- Single-scene improvements within approved outline

### Validation Strategy

#### Specification Validation
```bash
# Validate all active changes
openspec validate --strict

# Validate specific change
openspec validate add-protagonist-backstory --strict

# Check specific spec
openspec show CH-001 --type spec
```

#### Story Consistency Checks
Before merging any prose to main:
1. ✅ All referenced specs exist and are approved
2. ✅ Character dialogue matches CH-### voice guidelines
3. ✅ Plot events align with PR-### structure
4. ✅ World rules from WB-### are not violated
5. ✅ Scene serves purpose defined in SC-###

#### AI Validation Gates
The AI assistant MUST confirm:
- After creating story spec: "Does this capture your vision?"
- Before writing scenes: "Does this outline align with your vision?"
- Before character development: "Does this serve the story's needs?"

### Git Workflow

#### Branch Naming
```bash
# New scenes
story/[IssueNum]-SC-###-brief-description

# Character development
story/[IssueNum]-CH-###-character-name

# Revisions
revision/[IssueNum]-SC-###-improvement-type

# OpenSpec changes
change/add-protagonist-backstory
```

**Examples:**
- `story/1-SC-001-opening-storm`
- `story/2-CH-001-elena-cross`
- `revision/3-SC-001-dialogue-polish`
- `change/add-magic-system-rules`

#### Commit Message Format
```
<type>(<scope>): <description>

Types: scene, character, world, revision, spec
Scope: SC-###, CH-###, WB-###, PR-###
```

**Examples:**
```bash
scene(SC-001): add opening storm sequence
character(CH-002): develop antagonist motivation reveal
world(WB-001): establish lighthouse magic rules
revision(SC-001): strengthen dialogue and conflict
spec(PR-001): update story premise with new theme
```

#### Merge Strategy
- **Main branch** = Published, approved prose and specs
- **Story branches** = Work in progress, under review
- **Never merge** without author final approval
- **Squash commits** optional, preserve story development history

## Domain Context

### Fiction Writing Principles

#### Core Creative Values
1. **Spec-Driven**: Story specification is the single source of truth
2. **Character-Consistent**: Dialogue and actions must feel authentic
3. **Thematically Coherent**: Elements serve the story's themes
4. **Show, Don't Tell**: Prioritize scenes over exposition
5. **Collaborative**: AI assists, author decides

#### Scene Construction
Every scene MUST have:
- **Purpose**: Plot advancement, character development, or theme exploration
- **Conflict**: External, internal, or dramatic irony
- **Character Goals**: What each character wants
- **Sensory Details**: Atmosphere and immersion
- **Arc Progression**: How characters change or reveal

#### Character Development
Every character MUST have:
- **Motivation**: What they want most
- **Conflict**: What stands in their way
- **Voice**: Distinct dialogue patterns
- **Arc**: How they change (or why they don't)
- **Consistency**: Traceable to CH-### spec

### Genre Considerations

Inkspec supports all fiction genres:
- **Literary Fiction**: Deep character exploration, thematic complexity
- **Genre Fiction**: Clear plot structure, genre conventions
- **Short Stories**: Compact specs, focused arcs
- **Novels**: Comprehensive specs, complex character webs
- **Series**: Evolving specs across multiple stories

### Terminology

- **Spec**: A specification document (PR, CH, SC, WB)
- **Prose**: The actual written narrative
- **Scene Outline**: SC-### detailing what happens in a scene
- **Character Voice**: How a character speaks and thinks (from CH-###)
- **Story Canon**: All approved and merged specifications
- **Breaking Change**: Modification that contradicts established canon

## Important Constraints

### Absolute Prohibitions
The AI assistant MUST NOT:
1. Write prose without approved scene outline (SC-###)
2. Create characters without character spec (CH-###)
3. Contradict established story specifications
4. Write dialogue inconsistent with character voice
5. Include scenes that don't serve plot, character, or theme
6. Make major plot/character changes without approval

### Workflow Constraints
- Specifications MUST be approved before implementation
- Every requirement MUST have at least one scenario
- Scenes MUST reference relevant specs (PR, CH, WB)
- Character actions MUST trace to character motivations
- Plot events MUST align with story structure

### Quality Constraints
- **Conflict in every scene** - No purposeless scenes
- **Character agency** - Protagonists drive the plot
- **Emotional truth** - Reactions feel genuine
- **Stakes escalation** - Consequences increase over time
- **Thematic integration** - Themes emerge through action

## External Dependencies

### Claude Code
- **Version**: Latest Claude Code CLI
- **Model**: Claude 3.5 Sonnet or newer
- **Configuration**: See `CLAUDE.md` for instructions
- **Custom Commands**: `/openspec:proposal`, `/openspec:apply`, `/openspec:archive`

### OpenSpec CLI
- **Purpose**: Spec validation and change management
- **Commands**: `list`, `show`, `validate`, `archive`
- **Documentation**: See `openspec/AGENTS.md`

### Writing Tools (Optional)
- **Markdown Editors**: Obsidian, Typora, VS Code
- **Grammar Checkers**: Grammarly, ProWritingAid (for final prose)
- **Plotting Tools**: Scrivener, Plottr (can export to Inkspec specs)

## Example Workflows

### Starting a New Story

```bash
# 1. Create premise spec
# Edit: docs/story-spec/premise/PR-001_my_story.md

# 2. Create character specs
# Edit: docs/story-spec/characters/CH-001_protagonist.md
# Edit: docs/story-spec/characters/CH-002_antagonist.md

# 3. Create world specs (if needed)
# Edit: docs/story-spec/world/WB-001_setting.md

# 4. Create scene outlines
# Edit: docs/story-spec/scenes/SC-001_opening.md

# 5. Get approval, then write prose
git checkout -b story/1-SC-001-opening
# Edit: manuscript/chapter_01.md

# 6. Commit and review
git add .
git commit -m "scene(SC-001): add opening sequence"
git push origin story/1-SC-001-opening
```

### Making a Major Story Change

```bash
# 1. Create OpenSpec change proposal
mkdir -p openspec/changes/add-subplot/specs/scenes

# 2. Write proposal
# Edit: openspec/changes/add-subplot/proposal.md
# Edit: openspec/changes/add-subplot/tasks.md

# 3. Create spec deltas
# Edit: openspec/changes/add-subplot/specs/scenes/spec.md

# 4. Validate
openspec validate add-subplot --strict

# 5. Get approval, implement
# Create new SC-### specs in docs/story-spec/scenes/

# 6. Archive when complete
openspec archive add-subplot --yes
```

### Revising Character Development

```bash
# 1. Check current character spec
openspec show CH-001 --type spec

# 2. Create revision branch
git checkout -b revision/5-CH-001-motivation-deepening

# 3. Update character spec if needed
# Edit: docs/story-spec/characters/CH-001_protagonist.md

# 4. Revise affected scenes
# Edit: manuscript/chapter_01.md
# Edit: manuscript/chapter_03.md

# 5. Verify consistency
# Review all scenes referencing CH-001

# 6. Commit
git add .
git commit -m "character(CH-001): deepen protagonist motivation arc"
git push origin revision/5-CH-001-motivation-deepening
```

## Quick Reference

### File Locations
- **Story Specs**: `docs/story-spec/{premise,characters,scenes,world}/`
- **Manuscripts**: `manuscript/`
- **OpenSpec Changes**: `openspec/changes/`
- **OpenSpec Specs**: `openspec/specs/` (for framework capabilities)
- **Protocol**: `00_spec_driven_storytelling_protocol.md`

### Common Commands
```bash
# List active story changes
openspec list

# List story specifications
openspec list --specs

# Validate everything
openspec validate --strict

# Show specific spec
openspec show CH-001 --type spec

# Create story branch
git checkout -b story/1-SC-001-opening

# Commit scene
git commit -m "scene(SC-001): add opening"
```

### Key Principles
1. **Specs before prose** - Always
2. **Character consistency** - Non-negotiable
3. **Conflict in every scene** - Required
4. **Author approval** - At every phase
5. **Traceable requirements** - Everything links to specs

---

**Remember: Specifications drive the story. Prose brings it to life.**

# Story Specifications

This directory contains all story specifications for Inkspec projects.

## Directory Structure

- **`premise/`** - Story premises and loglines (PR-###)
- **`characters/`** - Character profiles and development (CH-###)
- **`scenes/`** - Scene outlines and specifications (SC-###)
- **`world/`** - World-building and setting details (WB-###)

## Naming Conventions

### Premise Specifications (PR-###)
Format: `PR-001_story_title.md`

Example: `PR-001_the_last_lighthouse.md`

### Character Specifications (CH-###)
Format: `CH-001_character_name.md`

Example: `CH-001_elena_cross.md`

### Scene Specifications (SC-###)
Format: `SC-001_scene_description.md`

Example: `SC-001_opening_storm.md`

### World-Building Specifications (WB-###)
Format: `WB-001_world_element.md`

Example: `WB-001_magic_system.md`

## File Templates

### Premise Template
```markdown
# PR-###: [Story Title]

## Logline
[One-sentence story premise]

## Genre
[Primary genre and subgenres]

## Target Length
[Word count: flash fiction, short story, novella, novel]

## Structure
[Three-act, hero's journey, etc.]

## Central Conflict
[What is the main tension/problem?]

## Emotional Journey
[What should the reader feel?]

## Themes
- [Theme 1]
- [Theme 2]

## Requirements
### Requirement: Story Premise
The story SHALL [define the core narrative requirement].

#### Scenario: Story opens with hook
- **WHEN** reader begins the story
- **THEN** they encounter immediate conflict/intrigue

### Requirement: Story Resolution
The story SHALL [define how conflicts resolve].

#### Scenario: Satisfying conclusion
- **WHEN** story reaches climax
- **THEN** central conflict is resolved in thematically appropriate way
```

### Character Template
```markdown
# CH-###: [Character Name]

## Role
[Protagonist, Antagonist, Supporting, etc.]

## Demographics
- **Age**:
- **Gender**:
- **Occupation**:
- **Background**:

## Personality
[Core personality traits and quirks]

## Motivation
[What does this character want most?]

## Conflict
[What stands in their way?]

## Character Arc
[How do they change throughout the story?]

## Voice
[How do they speak? Dialogue patterns?]

## Requirements
### Requirement: Character Consistency
[Character Name] SHALL behave consistently with established personality.

#### Scenario: Character responds to conflict
- **WHEN** faced with [specific situation]
- **THEN** character responds with [specific behavior]

### Requirement: Character Development
[Character Name] SHALL undergo [specific arc/change].

#### Scenario: Character growth moment
- **WHEN** [triggering event occurs]
- **THEN** character demonstrates [growth/change]
```

### Scene Template
```markdown
# SC-###: [Scene Description]

## Story Context
- **Premise**: PR-###
- **Characters**: CH-###, CH-###
- **Previous Scene**: SC-### (if applicable)
- **Next Scene**: SC-### (if applicable)

## Scene Purpose
[Why does this scene exist? What does it accomplish?]

## Setting
- **Location**:
- **Time**:
- **Atmosphere**:

## Character Goals
- **[Character Name]**: [What do they want in this scene?]
- **[Character Name]**: [What do they want in this scene?]

## Conflict
[What tension/obstacle emerges?]

## Character Arc Progression
[How do characters change or reveal themselves?]

## Sensory Details
[Key atmospheric elements to include]

## Requirements
### Requirement: Scene Conflict
The scene SHALL include meaningful tension.

#### Scenario: Conflict emerges
- **WHEN** characters interact
- **THEN** opposing goals create tension

### Requirement: Plot Advancement
The scene SHALL move the story forward.

#### Scenario: New information or change
- **WHEN** scene concludes
- **THEN** story state has changed meaningfully
```

### World-Building Template
```markdown
# WB-###: [World Element]

## Category
[Setting, Magic System, Technology, Culture, History, etc.]

## Description
[Detailed description of this world element]

## Rules
[What are the constraints and laws governing this element?]

## Story Impact
[How does this affect the plot and characters?]

## Requirements
### Requirement: World Consistency
[World element] SHALL remain consistent throughout the story.

#### Scenario: Element in use
- **WHEN** characters interact with [element]
- **THEN** it behaves according to established rules

### Requirement: World Integration
[World element] SHALL serve the story.

#### Scenario: Element supports narrative
- **WHEN** [element] appears in story
- **THEN** it advances plot, character, or theme
```

## Workflow

1. **Create Premise** - Start with PR-### defining the overall story
2. **Define Characters** - Create CH-### for each major character
3. **Build World** - Add WB-### for significant world elements
4. **Outline Scenes** - Create SC-### for each planned scene
5. **Write Prose** - Only after specs are approved

## OpenSpec Integration

Story specs follow OpenSpec conventions:
- Each spec file contains **Requirements** and **Scenarios**
- Changes are proposed through `openspec/changes/`
- Use `openspec validate --strict` to verify specs
- Archive changes with `openspec archive <change-id>`

## Remember

**Never write prose without approved specifications.**

Story specifications are the single source of truth.

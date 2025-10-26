# Inkspec

**Specification-Driven Storytelling Framework**

Inkspec applies software engineering discipline to fiction writing. Story specifications are the single source of truth, ensuring plot consistency, character authenticity, and thematic coherence throughout the creative process.

## What is Inkspec?

Inkspec is a collaborative fiction writing framework that uses a spec-first workflow to prevent plot holes, maintain character consistency, and track story development with the same rigor as software projects.

### Core Philosophy

- **Spec-First**: Define characters, plot, and world-building through structured requirements before writing prose
- **Traceability**: Every scene, dialogue, and character action traces back to approved specifications
- **Consistency**: Story specifications are the single source of truth
- **Collaboration**: Designed for human authors working with AI assistants

## Key Features

- **Specification-Driven Storytelling (SDS)**: Three-phase workflow from discovery to published prose
- **OpenSpec Integration**: Change management and version control for story development
- **AI-Assisted Writing**: Configured for Claude Code with mandatory confirmation gates
- **Structured Requirements**: Character profiles, plot outlines, scene specifications, and world-building docs
- **Mobile Idea Capture**: Simple inbox system for capturing inspiration on-the-go

## Three-Phase Workflow

### Phase 1: Story Discovery & Specification
- Clarify central conflict, protagonist goals, themes, and structure
- Create comprehensive story specification
- Define character profiles, plot structure, setting, and style guidelines
- Get author approval before proceeding

### Phase 2: Scene Planning & Implementation
- Create detailed scene outlines with purpose, goals, conflict, and sensory details
- Draft scenes according to approved outlines
- Maintain consistency with character voices and story world

### Phase 3: Revision & Refinement
- Verify story consistency with specifications
- Implement author feedback while maintaining story integrity
- Merge to main manuscript only after final approval

## Getting Started

### Prerequisites
- [Claude Code](https://claude.com/claude-code)
- [OpenSpec CLI](https://github.com/rrkeji/openspec) (bundled)
- Git (for version control)

### Installation

1. Clone this repository:
```bash
git clone https://github.com/openmoto/inkspec.git
cd inkspec
```

2. Open in Claude Code:
```bash
claude-code .
```

3. Start your first story:
```
Ask Claude: "Let's start a new story following the SDS protocol"
```

## Project Structure

```
inkspec/
├── .claude/                    # Claude Code configuration
│   └── commands/               # Custom slash commands
├── openspec/                   # OpenSpec framework
│   ├── AGENTS.md              # OpenSpec workflow instructions
│   ├── project.md             # Project conventions
│   ├── specs/                 # Implemented story capabilities
│   └── changes/               # Active and archived proposals
├── docs/                      # Story specifications
│   └── story-spec/
│       ├── premise/           # Story premises (PR-###)
│       ├── characters/        # Character profiles (CH-###)
│       ├── scenes/            # Scene outlines (SC-###)
│       └── world/             # World-building (WB-###)
├── inbox/                     # Mobile idea capture
│   ├── ideas/                 # Raw ideas from mobile
│   └── processed/             # Converted to specs
├── manuscript/                # Final prose output
├── 00_spec_driven_storytelling_protocol.md
├── CLAUDE.md                  # AI assistant instructions
└── README.md                  # This file
```

## Custom Slash Commands

- `/openspec:proposal` - Create a new story change proposal
- `/openspec:apply` - Implement an approved change
- `/openspec:archive` - Archive completed story work

## Documentation

- **[SDS Protocol](00_spec_driven_storytelling_protocol.md)** - The complete methodology
- **[OpenSpec Guide](openspec/AGENTS.md)** - Change management workflow
- **[Claude Instructions](CLAUDE.md)** - AI assistant configuration

## Story Spec Conventions

### File Naming
- Premises: `PR-###_story_title.md`
- Characters: `CH-###_character_name.md`
- Scenes: `SC-###_scene_description.md`
- World: `WB-###_world_element.md`

### Branch Naming
- `story/[IssueNum]-SC-###-scene-description`
- `revision/[IssueNum]-CH-###-character-development`

### Commit Messages
- `scene(SC-101): add opening confrontation scene`
- `character(CH-205): develop protagonist's backstory reveal`
- `revision(SC-101): strengthen dialogue and conflict`

## Core Principles

1. **Never write prose without approved specifications**
2. **Story specification is the single source of truth**
3. **Character consistency is mandatory**
4. **Show, don't tell**
5. **Collaborative partnership between author and AI**

## Mobile Idea Capture (Inbox)

Inspiration doesn't wait for you to be at your desk. The **Inkspec Inbox** lets you capture ideas anywhere:

### Quick Start
1. Use any notes app that syncs to your computer (Apple Notes, Google Keep, Notion, etc.)
2. Create a file: `inbox/ideas/2025-01-15.md` (or just use `quick-notes.md`)
3. Jot down whatever comes to mind - character ideas, dialogue, plot twists, world-building
4. Later in Claude Code: "Review my inbox and help me process these ideas"

### What to Capture
- Character ideas and personality traits
- Overheard dialogue that feels authentic
- Plot twists and story concepts
- World-building details and settings
- Scene atmospheres and sensory details
- Random creative thoughts

No formatting needed - just capture! Claude will help you convert raw ideas into proper specifications later.

See [inbox/README.md](inbox/README.md) for the complete workflow.

## When to Create OpenSpec Proposals

**Create proposals for:**
- New story arcs or major plot developments
- Character arc changes or additions
- World-building that affects multiple scenes
- Breaking changes to established canon

**Skip proposals for:**
- Minor dialogue revisions
- Typo fixes
- Formatting changes
- Scene polish that doesn't change plot or character

## Contributing

This is a framework for personal or collaborative fiction writing. Feel free to fork and adapt to your own creative process.

## License

[Choose your license - MIT, Creative Commons, etc.]

## Acknowledgments

- Built with [Claude Code](https://claude.com/claude-code)
- Powered by [OpenSpec](https://github.com/rrkeji/openspec)
- Inspired by Test-Driven Development and Spec-Driven Development methodologies

---

**Write with discipline. Create with confidence.**

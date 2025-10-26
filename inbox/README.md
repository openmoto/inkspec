# Inkspec Inbox

**Capture story ideas on-the-go, process them into specs later.**

## Purpose

The inbox is your **low-friction idea capture system**. When inspiration strikes while you're away from your desk, jot it down quickly without worrying about proper formatting or spec structure. Later, when you're working in Claude Code, process these raw ideas into proper story specifications.

## Directory Structure

```
inbox/
├── ideas/          # Raw, unprocessed ideas (mobile capture)
│   ├── 2025-01-15.md
│   ├── 2025-01-16.md
│   └── quick-notes.md
├── processed/      # Ideas that have been converted to specs
│   └── archive/
└── README.md       # This file
```

## Mobile Capture Workflow

### Step 1: Capture Ideas Anywhere

Use any note-taking app that syncs to your computer:
- **iOS**: Apple Notes, Drafts, Bear, Notion
- **Android**: Google Keep, Samsung Notes, Notion
- **Cross-platform**: Obsidian, Notion, Simplenote

**Option A: Daily file approach**
Create a file named with today's date: `inbox/ideas/2025-01-15.md`

**Option B: Quick notes approach**
Just dump everything into `inbox/ideas/quick-notes.md`

### Step 2: Write Whatever Comes to Mind

Don't worry about formatting! Just capture:
- Character ideas
- Plot twists
- Dialogue snippets
- World-building details
- Scene concepts
- Thematic thoughts
- Overheard conversations
- Atmospheric notes

**Examples:**
```markdown
# 2025-01-15

- What if the protagonist can see ghosts but only during storms?
- Dialogue: "I'm not running away. I'm running toward something."
- Character idea: A lighthouse keeper who's afraid of the ocean
- Setting: Abandoned fishing village, fog rolls in every evening at 6pm
- Plot twist: The antagonist is actually her future self trying to prevent a disaster
```

### Step 3: Process Later in Claude Code

When you're ready to write, ask Claude to help process your inbox:

```
You: "Review my inbox and help me process these ideas"

Claude:
- Found 3 character ideas → Let's create CH-003, CH-004
- Found 1 plot twist → Update PR-001 with new arc
- Found 2 world-building details → Create WB-002
- Found dialogue snippet → Save for SC-005
```

## Inbox File Template

Here's a simple template you can copy to your notes app:

```markdown
# [Date]

## Character Ideas
-

## Plot/Story Ideas
-

## Dialogue Snippets
-

## World-Building
-

## Scene Concepts
-

## Random Thoughts
-
```

Or just freeform it! The point is to capture quickly.

## Processing Workflow

### When to Process

Process your inbox when:
- ✅ You have 5+ ideas accumulated
- ✅ You're starting a new story
- ✅ You're stuck and need inspiration
- ✅ Weekly review (Sunday evening ritual?)

### How to Process with Claude Code

**1. Open inbox file:**
```
You: "Read inbox/ideas/2025-01-15.md"
```

**2. Ask for categorization:**
```
You: "Categorize these ideas into premise, character, scene, or world-building"
```

**3. Create specs for good ideas:**
```
You: "Create CH-003 for the lighthouse keeper character idea"
Claude: [Creates proper character spec with requirements and scenarios]
```

**4. Move processed file:**
```bash
git mv inbox/ideas/2025-01-15.md inbox/processed/2025-01-15.md
```

### Processing Example

**Raw inbox idea:**
```
- Lighthouse keeper afraid of the ocean, never goes near the water's edge
```

**Claude processes into CH-003:**
```markdown
# CH-003: Marcus Thorne

## Role
Supporting character - Lighthouse keeper

## Personality
Ironic fear of the ocean despite living by it. Anxious, detail-oriented.

## Motivation
Maintain the lighthouse to feel useful without confronting his fear.

## Requirements
### Requirement: Character Consistency
Marcus SHALL display fear when near open water.

#### Scenario: Marcus avoids the shore
- **WHEN** asked to go to the beach
- **THEN** he finds excuses to stay near the lighthouse
```

## Tips for Effective Capture

### DO:
- ✅ Write immediately when inspired (even half-formed thoughts)
- ✅ Include context ("This is for the detective story")
- ✅ Note the source ("Overheard at coffee shop")
- ✅ Capture dialogue exactly as you hear it
- ✅ Use voice notes if your app supports it

### DON'T:
- ❌ Wait to write it "properly" (you'll forget)
- ❌ Self-censor or filter ideas (capture everything)
- ❌ Worry about formatting or organization
- ❌ Force ideas into spec format on mobile
- ❌ Delete "bad" ideas (some become gold later)

## Syncing to Your Computer

### Cloud Sync Options

**Apple Notes** → iCloud → Auto-syncs to Mac
**Google Keep** → Google account → Access via web
**Notion** → Real-time sync across all devices
**Obsidian** → iCloud/Dropbox/Git sync
**Dropbox/OneDrive** → Any markdown file

### Manual Sync (if needed)

If your notes app doesn't auto-sync:
1. Email the note to yourself
2. Copy/paste into `inbox/ideas/[date].md`
3. Continue processing

## Integration with OpenSpec

Ideas from the inbox can become:

**Premise ideas** → `PR-###` in `docs/story-spec/premise/`
**Character ideas** → `CH-###` in `docs/story-spec/characters/`
**Scene ideas** → `SC-###` in `docs/story-spec/scenes/`
**World ideas** → `WB-###` in `docs/story-spec/world/`

The inbox is the **pre-spec stage** - raw creativity before structure.

## Example Daily Capture

```markdown
# 2025-01-15 - Coffee Shop Session

## Random Inspiration
- Woman at next table: "I know what I saw, even if nobody believes me."
  → Could be great for paranormal detective story

- Barista has tattoo of lighthouse with storm clouds
  → Visual inspiration for WB-001 (lighthouse appearance)

## Character Thought
- What if Elena's stubbornness comes from being gaslit as a child?
  → Add to CH-001 backstory

## Plot Idea
- The lighthouse doesn't just warn ships - it calls something TO the shore
  → Major plot twist for PR-001, needs OpenSpec proposal

## World-Building
- Coastal town has yearly "Fog Festival"
  → Local tradition, add to WB-002 (town culture)

## Scene Visual
- Sunset through fog, orange light diffused into soft glow
  → Atmosphere for SC-003 (evening arrival scene)
```

## Upgrading to Telegram Bot (Future)

When you're using the inbox heavily, we can build:
- Voice note transcription
- Auto-categorization via AI
- Direct `/character` or `/scene` commands
- Instant sync to git repository

For now, manual capture works great!

## Remember

**The best idea is the one you capture.**

Don't let inspiration slip away because you're not at your desk. Write it down messy, clean it up later.

---

**Capture freely. Process deliberately. Write brilliantly.**

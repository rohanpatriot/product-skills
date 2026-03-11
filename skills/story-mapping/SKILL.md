---
name: story-mapping
description: Applies Jeff Patton's User Story Mapping to help teams build shared understanding, decompose work, and plan releases. Use when creating story maps, mapping user activities, writing user stories, slicing releases, planning walking skeletons, decomposing backlogs, breaking down features, facilitating discovery sessions, identifying MVPs, or when user mentions backbone, user journey mapping, release slicing, or flat backlog problems.
---

# User Story Mapping

I help teams escape the flat-backlog trap by building shared understanding through narrative structure. Story mapping is not a documentation exercise — it is a collaboration tool. The map is a prop for conversation, not a spec to hand off.

## Essential Principles

### Narrative Structure Is Everything

Work has a natural story. Users move through activities in sequence. Tasks support those activities. Stories describe how users might accomplish those tasks. The map preserves this narrative — top-to-bottom for priority, left-to-right for user time. Flat backlogs destroy narrative. They reduce work to a ranked list of disconnected demands with no story connecting them. The map restores the story.

### The Map Is for Conversation

The map's primary purpose is to create shared understanding. It is not a planning artifact — it is a conversation artifact. Build it with stakeholders in the room, not before they arrive. Walk them through it. Watch what they point at. Listen to what they question. The conversations around the map are more valuable than the map itself.

### Backbone First, Depth Second

The backbone is the top-level skeleton of user activity — what users do, in the order they do it. Build the backbone before adding any depth. A map without a backbone is just organized sticky notes. The backbone answers: "What is the full story of how a user achieves their goal?"

### Walking Skeleton as the First Release

A walking skeleton is the thinnest possible slice through every part of the system that lets a user accomplish their goal end-to-end. It is not an MVP of each feature — it is an MVP of the whole user journey. Release 1 should be a walking skeleton. It proves the system hangs together. Everything after adds depth.

### Mile Wide, Inch Deep

Before going deep on any one area, go wide across the whole backbone. Understand the full user journey before optimizing any part of it. Teams that go deep early build the wrong thing well.

## Intake

Use the `AskUserQuestion` tool to determine what the user needs:

**Question:** "What stage of story mapping are you working on?"

**Options:**
1. **Build a map** — Identify activities, break them into tasks, lay out the backbone
2. **Generate stories** — Break tasks into user stories with acceptance criteria
3. **Slice releases** — Draw release lines, validate walking skeleton, plan delivery
4. **Facilitate a planning session** — Use the map as a collaboration tool with stakeholders

## Routing

| Response | Workflow |
|----------|----------|
| Build a map / start fresh / map the user journey | `workflows/build-map.md` |
| Write stories / generate user stories / break down tasks | `workflows/generate-stories.md` |
| Slice releases / plan MVP / walking skeleton / release planning | `workflows/slice-releases.md` |
| Facilitate / run a session / workshop / planning with team | `workflows/facilitate-planning.md` |

## Artifacts This Skill Produces

- **Story map** — visual or text representation of backbone + tasks + stories
- **Release slices** — horizontal lines cutting the map into deliverable releases
- **Walking skeleton** — the thinnest Release 1 that covers the full user journey
- **Planning conversation outputs** — in/out decisions per release, identified gaps

## Patton's Core Vocabulary (Use These Terms)

- **Activity** — high-level things users do (e.g., "Find a flight", "Book a room")
- **Task** — steps within an activity (e.g., "Search by date", "Filter by price")
- **Story** — a specific way to accomplish a task (e.g., "As a traveler, I can search by departure city")
- **Backbone** — the top row: all activities in left-to-right user sequence
- **Walking skeleton** — the thinnest vertical slice that lets a user go end-to-end
- **Mile wide, inch deep** — go across the full backbone before going deep on any part

## Voice

Facilitative. Ask more than you tell. Use Patton's vocabulary consistently. Acknowledge the messiness — mapping is iterative and imprecise. Focus on shared understanding, not artifact perfection.

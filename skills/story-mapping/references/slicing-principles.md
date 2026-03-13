# Slicing Principles

A deep reference on how to slice story maps into releases effectively. This document covers the conceptual foundations of slicing, practical heuristics, and worked examples across different product types.

---

## The Walking Skeleton in Depth

The walking skeleton is the most important concept in release planning from a story map. It comes from Alistair Cockburn's Crystal methods, but Patton applies it as the definition of Release 1 in story mapping.

### What the Walking Skeleton Is

A walking skeleton is an implementation of the system that performs a small end-to-end function. It need not use the final architecture, but it should link together the main architectural components. The architecture and the functionality can then evolve in parallel.

Applied to story mapping: the walking skeleton is the minimum set of stories that allows a user to accomplish the stated goal end-to-end. One story per task (or per activity at the most stripped-down level), spanning the full backbone from left to right.

**Key properties of a walking skeleton:**
1. **End-to-end:** It must span the entire user journey. If the backbone has 5 activities, the walking skeleton touches all 5.
2. **Functional:** A real user can actually accomplish the goal. It is not a demo, a prototype, or a facade.
3. **Thin:** It contains the minimum required to go end-to-end. No edge cases, no error states that are not blocking, no polish.
4. **Coherent:** Each step connects to the next. A user moving through the walking skeleton does not hit a dead end.

### What the Walking Skeleton Is Not

**Not a rough version of every feature:**
"Rough version" implies every feature is present but unpolished. The walking skeleton omits most features entirely. It has one version of each step — the thinnest version that works — and nothing else.

**Not a technical proof of concept:**
A technical prototype may prove that something is buildable but not that a user can accomplish their goal. The walking skeleton must be usable by a real user, not just functional in a test environment.

**Not the "core features" release:**
"Core features" implies the features most important to the team. The walking skeleton is the features most essential to the user's ability to go end-to-end — which may be a different set.

**Not MVP-of-each-feature:**
Teams sometimes interpret the walking skeleton as "build the MVP of each feature." This produces a release that is too thick — each feature is its own mini-MVP, comprehensive within itself. The walking skeleton is instead one thin instance of each feature, not the MVP of each.

### Why the Walking Skeleton Must Come First

Teams that do not build a walking skeleton first exhibit a predictable failure mode: they build one part of the journey thoroughly while neglecting others. By the time they reach the later parts of the journey, they have consumed most of their budget and timeline on the early parts — and the early parts do not work without the later parts.

The walking skeleton forces the team to prove the full journey is viable before investing deeply in any part of it. It is a risk mitigation strategy as much as a release strategy.

---

## Mile Wide, Inch Deep: Explained With Examples

The principle: before going deep on any part of the user journey, go wide across the full journey.

**Why this is counter-intuitive:**
Human cognition favors depth. When we understand something well, we want to develop it fully. When we encounter something we do not understand, we want to understand it before moving on. Story mapping resists both instincts — it pushes teams to maintain a wide, shallow view of the full journey before narrowing.

### Example: A Project Management Tool

**Mile wide, inch deep (correct):**
```
Release 1 (Walking Skeleton):
- Create a project (name only)
- Create a task within the project (title only)
- Assign task to a team member
- Mark task complete
- View project progress (basic list)
```

**Deep before wide (incorrect):**
```
Release 1:
- Create a project with name, description, tags, color, icon, and template
- Import projects from Jira
- Project archive and history
- (tasks, assignments, progress: none)
```

The incorrect Release 1 builds one activity completely. A user cannot accomplish the goal of "managing a project end-to-end" because the downstream activities are missing.

### Example: An E-Commerce Site

**Mile wide, inch deep (correct):**
```
Release 1 (Walking Skeleton):
- Browse products by category
- View product detail
- Add to cart
- Enter shipping address
- Enter payment information
- Confirm order
- Receive order confirmation email
```

**Deep before wide (incorrect):**
```
Release 1:
- Browse products by category, subcategory, brand, and tag
- Filter by price range, rating, availability, and shipping speed
- Compare up to 4 products side-by-side
- Read and submit product reviews
- Save products to wishlist
- (cart, checkout, confirmation: none)
```

A user with a rich browse experience but no checkout cannot accomplish their goal.

---

## When a Slice Is Too Thin

A slice is too thin when it does not deliver independently meaningful value — when it only makes sense as scaffolding for the next slice.

**Signs a slice is too thin:**

- Users cannot accomplish the stated goal, only a precursor to it
- The slice requires users to work around broken or missing parts of the journey
- The team would not be willing to show this to a real customer
- The slice delivers no user-observable value — it is purely infrastructure

**The "would you ship this?" test:**
Imagine the slice as the final product — shipped and no more development happening. Would a real user be better off with this than without it? Would you be comfortable calling it a release?

If the answer is "no, users couldn't really use this," the slice is too thin. Options:
1. Add the minimum stories needed to make the slice independently usable
2. Reconsider whether the stated goal is correctly scoped (maybe the goal implies more than the team thought)
3. Explicitly label the release as an internal release (not user-facing) and track it separately

**The walking skeleton caveat:**
The walking skeleton is often thin by design. It may have a rough user experience. That is acceptable if the user can still accomplish their goal. Thin is not the same as non-functional.

---

## When a Slice Is Too Thick

A slice is too thick when it contains more than the minimum needed for users to accomplish the goal, delaying the learning that comes from shipping.

**Signs a slice is too thick:**

- The release line is more than halfway down the story columns for most activities
- The slice includes edge cases, error states, and advanced features that are not blocking
- The team is spending time polishing the first slice instead of validating that the full journey works
- The slice is scheduled to ship more than 3–6 months from now

**The cost of thick slices:**
Every story above the Release 1 line that is not strictly necessary is a delay to shipping. Delays to shipping delay learning. Teams that ship thick Release 1s learn what users actually need 3–6 months later than teams that ship thin walking skeletons.

**What "not strictly necessary" means:**
A story is not strictly necessary for Release 1 if a user can accomplish the stated goal without it. Even if the experience is worse without it. Even if users will complain. The question is: can they do the thing? If yes, it can wait.

---

## Horizontal vs. Vertical Slicing

This distinction is the most important concept in release planning.

**Vertical slice:** Selects all stories from one or a few activities. Goes deep on one part of the journey.
**Horizontal slice:** Selects the topmost stories from every activity. Goes thin across the full journey.

| | Vertical | Horizontal |
|---|---|---|
| Coverage | Deep in one area | Thin across full journey |
| User can complete goal? | No | Yes |
| Risk | High — full-journey gaps discovered late | Low — gaps discovered during walking skeleton |
| Learning | Partial — only tests one part of the journey | Complete — tests the full journey |
| Recommended for releases? | No | Yes |

### Why Horizontal Wins for Releases

Releases should be horizontal slices because:

1. **Value requires end-to-end.** A user cannot accomplish their goal with only part of the journey. Vertical releases deliver partial journeys that deliver no user value until the full journey is assembled.

2. **Risk surfaces early.** Horizontal slicing forces the team to think through the full journey before shipping any part of it. Vertical slicing allows the team to avoid thinking about the hard parts of the journey until late in the development cycle.

3. **Learning is faster.** Shipping a thin horizontal slice and watching real users try to use it produces more learning per day than shipping a thick vertical slice. The thin slice may reveal that users do not care about the journey at all — a discovery that saves months of wasted development.

**When vertical slices are appropriate:**
Internal/technical releases that are not user-facing. Infrastructure work, internal tools, backend services. These are not story map releases — they are technical milestones that support user-facing releases.

---

## How to Identify the Walking Skeleton for Different Product Types

### CRUD Applications (admin tools, internal tools, dashboards)

The CRUD walking skeleton covers one full create-read-update-delete cycle for the primary entity.

**Example: A CRM for a sales team**
- Create a contact (name and email only)
- View a list of contacts
- View a contact detail
- Edit a contact
- Log a note on a contact
- (Delete: can wait if soft-delete is complex)

Every CRUD app has the same walking skeleton shape. The challenge is resisting the urge to add filtering, search, bulk operations, and custom fields before the basic cycle works.

### Marketplaces (two-sided, buyer/seller)

Marketplaces have two walking skeletons — one per user type — plus the connection point between them.

**Example: A freelance marketplace**
Seller walking skeleton:
- Create a profile
- List a service
- Receive an inquiry

Buyer walking skeleton:
- Browse listings
- View a listing
- Send an inquiry

Connection point:
- Seller responds to inquiry
- Buyer accepts proposal
- Payment is processed

The marketplace walking skeleton is thicker than single-sided products because it must include enough of both sides to create a transaction. Focus on the minimum end-to-end transaction, not a complete experience for either side.

### Content Sites (blogs, newsletters, media)

The content site walking skeleton is the thinnest version of the content creation-to-consumption loop.

**Example: A newsletter platform**
Creator walking skeleton:
- Write and publish a post
- Send to subscribers

Subscriber walking skeleton:
- Subscribe to a newsletter
- Receive and read a post

The content site walking skeleton is often simpler than teams expect. Teams frequently over-scope it by including SEO optimization, analytics, multiple content types, and social sharing before validating that the basic loop works.

### APIs and Developer Tools

The API walking skeleton is the minimum viable integration — the simplest call a developer could make that returns real, useful data.

**Example: A payments API**
- Create a payment intent
- Process a test payment
- Receive a success/failure response
- Access basic transaction record

API walking skeletons focus on one complete request-response cycle for the core use case, with sufficient documentation to attempt the integration without support.

---

## Common Slicing Heuristics

**Heuristic 1: The "one story per task" rule**
Each task in the backbone should contribute at most one story to the walking skeleton. If a task has two stories in Release 1, ask whether the second is truly essential or whether it can wait.

**Heuristic 2: The "blank screen" test**
Can a brand new user, starting from a blank screen, accomplish the goal using only Release 1? Walk through it literally. What does the user see first? Where do they go next? If any step requires data or setup that is not in Release 1, Release 1 is incomplete.

**Heuristic 3: The "graceful degradation" filter**
For every story in the Release 1 candidate set, ask: "What happens if we ship without this? Can the user still accomplish their goal, even if ungracefully?" If yes, it can wait. This filter is particularly useful for error states, edge cases, and polish.

**Heuristic 4: The "minimum viable journey" frame**
Instead of asking "what do we want to ship in Release 1?", ask "what is the minimum journey a user could take to accomplish this goal?" Frame Release 1 as the minimum viable journey, not the minimum viable product. The journey frame preserves end-to-end integrity; the product frame often produces vertical slices.

**Heuristic 5: The "your customer's first day" test**
Imagine a customer using Release 1 on their very first day with your product. Can they accomplish their goal? Would they come back? If the answers are "barely" or "probably," that is an acceptable walking skeleton. If the answers are "no" or "definitely not," the walking skeleton is too thin.

---

## Naming Releases by Outcome vs. Feature Set

Release names communicate priorities and create alignment. The right name frames value; the wrong name frames features.

**Outcome-based names describe what users can do:**
- "Send your first invoice"
- "Get paid end-to-end"
- "Collaborate with your team"
- "Manage your customer relationships"

**Feature-based names describe what is in the release:**
- "Invoice creation and management"
- "Payment tracking v1"
- "Multi-user support"
- "CRM core features"

**Why outcome names are better:**

1. **They create stakeholder alignment.** "Send your first invoice" creates a clear test for whether the release succeeded. "Invoice creation and management" does not.

2. **They guide development decisions.** When an engineer asks "should we include this edge case in Release 1?", the answer is clearer against "Send your first invoice" than against "Invoice creation v1."

3. **They communicate externally.** Outcome-based release names can be used in customer communications. Feature-based names cannot — they describe the product, not the value.

4. **They prevent scope creep.** A release named by outcome has a natural scope boundary — everything needed to achieve the outcome. A release named by feature set has a fuzzy boundary — what counts as "core"?

**How to name a release:**
Finish this sentence: "After this release, users can finally ___." That sentence is the release name.

---

## How Many Releases Should a Map Have?

There is no universal answer, but there are useful constraints.

**Too few releases (1–2):**
Usually means the first release is too thick, or the team has not thought far enough ahead. With only 2 releases, the map does not help sequence decisions — it just labels "now" and "later."

**The right number (3–5):**
For most product areas, 3–5 releases represent a planning horizon that is far enough ahead to be strategic and close enough to be realistic. Release 1 is the walking skeleton. Releases 2–3 add depth to the journey. Releases 4–5 add advanced features and edge cases.

**Too many releases (6+):**
Usually means releases are too thin (each release only adds 1–2 stories), or the map is too large (covering multiple distinct user journeys). Consider whether some far-future releases should be "future" or "undecided" rather than numbered releases.

**The planning horizon:**
Release slices should correspond to a planning horizon the team can reason about confidently. For most teams, that is 3–6 months. Releases beyond 6 months are speculative — they should be sketched in the map but held loosely.

---

## The Relationship Between Slicing and MVP

"MVP" is one of the most overused and misunderstood terms in product development. Story mapping clarifies what MVP means in practice.

**MVP is not "minimum features."**
Teams often treat MVP as a list of minimum acceptable features — the least they can ship and call it a product. This framing produces vertical slices: complete implementations of a small set of features.

**MVP is "minimum viable user journey."**
A truly minimum viable product is one in which users can accomplish a meaningful goal — end-to-end — with the minimum investment. This is the walking skeleton: a horizontal slice that covers the full journey at minimum depth.

**The validation question:**
An MVP's purpose is to validate a hypothesis. "Users will pay for a tool that helps them invoice clients." The walking skeleton validates this hypothesis because it lets users try the full journey. A vertical slice validates only that one part of the journey works — not that the whole thing delivers value.

**When MVP is an excuse:**
Teams sometimes invoke MVP to justify shipping something that does not let users accomplish their goal. "It's MVP — we'll add the rest later." If users cannot accomplish their goal, it is not a minimum viable product — it is a feature demo. The walking skeleton is the floor for what counts as an MVP.

# Play: AI-Augmented Collaboration (The "AI Mob")

Reduce cycle time for legacy maintenance tasks by 50% through collective AI steering.

| Prep time | Run time | Persons |
|-----------|----------|---------|
| 30m       | 2-3hr    | 2-4     |

**5-second summary**: Work on legacy code collaboratively with AI as the tour guide.

Transition from "solo AI usage" to a high-leverage collaborative process, and share learnings that help teams improve over time. Prioritise quality of thought and collective learning over raw speed.

---

## What you will need

- **Shared IDE/Session**: Cursor, VS Code Live Share, or a shared Gemini/Claude screen
- **The Scratchpad**: A shared page (Confluence, Google Doc) for co-authoring prompts
- **A timer**: To enforce role rotation
- **A transcription tool**: Otter/Granola to capture the "why" behind decisions

**Play resources**: [Detailed Background/Theory: AI-Augmented Collaboration](#)

---

## About this play

### What is this play?

2-4 people work on a single legacy task together, with AI as the tour guide and the team as the decision-makers. The AI explains the unfamiliar codebase, proposes solutions, and surfaces context — but the group decides where to go, what to trust, and what to challenge. One person operates the AI (the Driver), the group directs the questions (the Navigators), and someone actively pokes holes in what the AI produces (the Red Team). Roles rotate every 20-30 minutes so everyone builds the mental map, not just one person.

This is mob programming adapted for AI-assisted work. Instead of one person exploring alone and accepting whatever the AI suggests, the group navigates together — trading individual speed for shared understanding.

> **This isn't just for new shiny stuff.** The highest value is in legacy maintenance and bug fixes — exactly where context has drifted and ramp-up dread is worst.

---

### The Hypothesis

"We believe that by shifting from solo AI usage to a collaborative 'AI Mob' approach when working on legacy maintenance, we will reduce the total time from 'In-Progress' to 'PR Merged' by 50%. This is achieved by eliminating individual 'ramp-up dread' and replacing asynchronous code reviews with real-time group consensus.

We will also learn whether, after participating in AI Mob sessions on the same app, participants can independently describe its architecture and confidently pick up the next maintenance ticket solo."

---

### Why run this play?

**Break the Knowledge Silo**: Legacy code isn't just intimidating — it's often understood by one person or nobody. The AI becomes the tour guide, building shared understanding across the group in minutes rather than hours of solo exploration.

**Deliberate over Fast**: A solo dev optimises for "does it work?" A mob asks "should it work *this way*?" The group catches architecturally poor AI suggestions before they become tomorrow's maintenance burden.

**Stack Run, Serve, and Change**: Solo AI usage does Run — tickets closed, code shipped. The AI Mob does Run *while* investing in Serve *and* running a Change experiment. Three modes, one session, same time budget as solo work. You're not trading delivery for learning — you're stacking them.

**Scale the Portfolio**: A team that mobs on legacy apps builds transferable context. Keep multiple apps in play and you've got a team maintaining serious ARR, not just one hero per app.

---

## Prep: The Ingredients

**People**: 2-4 participants. Mixing seniority is encouraged to maximise learning.

**Time**: 2 to 3 hours.

**Tools**:
- **Shared IDE/Session**: Cursor, VS Code Live Share, or a shared Gemini/Claude screen
- **The Scratchpad**: A shared document for co-authoring prompts
- **Transcription**: Granola or Otter to capture the "why" behind decisions
- **Timer**: To enforce rotation so learning is distributed

---

## The Roles

Roles **must rotate every 20-30 minutes** to maintain high engagement and distribute learning.

**The Driver (Human)**: The "hands." They operate the AI and the keyboard. They only input what the group agrees upon.

**The Navigator (Collective)**: The "brains." They suggest logic, ask "what if" questions, and research edge cases.

**The Red Team (AI-Assisted)**: The "critic." One person uses a secondary AI instance to find holes, security risks, or slop in the primary AI's suggestions and the team's approach.

**The Outcome Keeper**: The "referee." Ensures the session stays focused on the specific ticket and prevents "AI rabbit holes", and that learning is a byproduct of the group's work.

> **The handoff**: Navigator describes *what* -> AI suggests *how* -> Driver executes -> Red Team challenges the result.

---

## The Play: Step-by-Step

### 1. Context Injection & Onboarding (15 mins)

Treat the AI like a new contractor.

- **Action**: Feed the AI the relevant code files and any Technical Constraints & Standards
- **Rule**: Read every prompt twice before hitting "Enter." Value intentionality over velocity

### 2. The Discovery Loop

Before writing a single line of a fix, ask the AI to:
- Explain how the legacy logic currently works
- Hypothesise why the bug exists
- Propose three different ways to solve it (architectural trade-offs)

### 3. The "Healthy Friction" Loop

When the AI generates a solution:

- **The Pause**: Read the output aloud together. Don't just hit "Apply"
- **Red Team Check**: The Red Team member critiques the code. Does it follow our standards? Is it slop?
- **The 15-Minute Rule**: If the group gets stuck on a complex technical hurdle, one person "spikes" it for 15 mins while the others break. Re-group and present findings

### 4. Integrated Testing

Run the test pipelines during the session. The "Done" state isn't just code that looks right; it's code that passes the build and is understood by the Mob.

### 5. Final Slop Review

Perform a "Group PR Review" before the session ends. Ensure the code is human-readable and maintainable.

### 6. Retrospective (5 mins)

Three votes, 30 seconds each. Likert scale (1 = Strongly Disagree, 5 = Strongly Agree):

| # | Dimension | Statement |
|---|-----------|-----------|
| 1 | **The Group** | "Everyone contributed meaningfully and felt heard" |
| 2 | **The AI** | "We caught and corrected the AI's mistakes before accepting them" |
| 3 | **The Learning** | "I know what I'd do differently next time" |

Then ask: **"What's the one thing we should change for next session?"**

**For deeper analysis**: Feed the session transcript to AI with: "Analyse this collaborative coding session. Did everyone contribute equally? Where did we get stuck? What AI assumptions did we correct? What collaboration patterns emerged? What should we change?"

---

## Ground Rules

### The Even/Overs

When these are in tension, the first wins:

| Prioritise | Even over |
|------------|-----------|
| Shared understanding | Individual speed |
| Exploration | Execution |
| Deliberateness | Velocity |
| Multiple perspectives | Single ownership |
| Learning | Pure output |

### The Manifesto

**On the Pitch**: If you are in the room, you are "on the pitch." No passive observers.

**Safe to Try**: Experiments are encouraged. If the AI suggests something that breaks, it's a group learning moment, not an individual failure.

**Shared Intentionality**: We are here to make better decisions, not just more code.

**Debate in Code**: Two approaches? Try both. Data decides, not hierarchy.

### AI-Specific Safety

AI introduces psychological risks people don't expect — prompt shame, authority bias, feeling exposed when the AI produces something better than you could.

| Agreement | The risk it addresses |
|-----------|----------------------|
| "No such thing as a bad prompt" | Prompt shame — people won't experiment if they fear looking foolish |
| Read output aloud together | Prevents one person silently deciding if AI output is "good enough" |
| Everyone gets a turn prompting | AI-confident people dominate; novices never learn the feel of it |
| "The AI is wrong until proven right" | Removes authority bias — nobody defers to AI just because it sounds confident |
| Name what you don't know | AI makes knowledge gaps visible — normalise saying "I don't understand this output" |

### Warning Stickers

At session start, ask each participant: **"What's your known risk in this kind of session?"** Public self-declaration builds vulnerability and gives the group permission to name patterns when they appear.

| Risk | Antidote |
|------|----------|
| Analysis paralysis | "We decide in 5 minutes" |
| Impatience / wants to build | "Let's read the output together" |
| Dominates keyboard | Timer enforces driver swap |
| Goes quiet / defers | "What are you seeing?" |
| Prompt perfectionism | "Just try it — we'll iterate" |
| AI authority bias | "What would *we* do without the AI?" |

---

## Success Metrics

| We'll know it's TRUE when... | We'll know it's FALSE when... | What this tells us |
|------------------------------|-------------------------------|-------------------|
| The average cycle time of tasks moving from "In-Progress" to "Merged" drops 50% faster than historical solo benchmarks | Cycle time doesn't meaningfully improve, or gets worse due to coordination overhead | **TRUE**: Mob eliminates ramp-up and review bottlenecks as hypothesised. **FALSE**: Coordination overhead exceeds the ramp-up savings — the mob is slower, not faster. |
| Participants feel 50% more confident maintaining this legacy area | Participants still defer maintenance tickets on that app to others despite having mobbed on it | **TRUE**: Shared understanding transfers to individual capability — the mob built lasting confidence. **FALSE**: The mob created a group experience but not individual capability — people still won't touch it solo. |

---

## Extra Reading

### Run, Serve, and Change: Where AI Creates Risk — and Opportunity

Most teams use AI to accelerate Run work — closing tickets faster, generating boilerplate, shipping more code. AI is exceptionally good at this.

The problem is what gets lost. When one person works alone with AI, the emphasis shifts entirely to output. Architectural trade-offs, maintainability, and whether we're solving the right problem — the Serve work — gets skipped because there's nobody else in the room to ask the hard questions.

The result is AI Slop: code that works today but creates tomorrow's maintenance burden. Technically functional, architecturally poor, understood by nobody.

AI-Augmented Collaboration doesn't ask you to stop delivering. It stacks all three modes into a single session:

| Mode | What happens in the mob |
|------|------------------------|
| **Run** | The ticket still gets closed. Code ships. The AI handles the production work. |
| **Serve** | The group steers the AI toward solutions that serve future maintainers, not just today's deadline. The hard questions get asked in real-time, not in a code review three days later. |
| **Change** | The practice itself is the experiment. Every session builds a new team capability — shared architectural understanding, collaborative AI fluency, and confidence to maintain legacy systems independently. |

This is the real argument for the AI Mob: you're not trading Run for Serve. You're doing Run *while* investing in Serve *and* running a Change experiment. Three modes, one session, same time budget as solo work.

### Reference Material

- **[Detailed Background/Theory](#)**: The thinking behind this approach and the psychology and group dynamics to be aware of
- **[Technical Constraints & Standards](#)**: The standards the AI must adhere to
- **[Starting Scenarios & First Prompts](#)**: Five common starting points with suggested first AI prompts
- **[Enabling Constraints](#)**: How each practice constraint (timer, strong-style, single screen) drives creativity when applied well — and what to watch for when it's misapplied
- **[Collaboration RPG](#)**: Willem Larsen's gamified role cards for experienced teams who want to add depth
- **[Research & Evidence](#)**: Gartner AI literacy case, Crisp (Sweden) daily 3hr sessions, Atlassian mobbing with AI metrics

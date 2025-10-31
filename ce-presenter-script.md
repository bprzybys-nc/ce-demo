# Context Engineering Demo - Presenter Script & Cheatsheet

**Total Time: 16 minutes**
Quick reference guide for presenters

---

## SLIDE 1: The Context Crisis (1m 30s) ⏱️ 0:00-1:30

### Opening Hook
"How many of you have had this experience: You ask an AI to build something, it creates code that looks good but doesn't fit your project, so you explain again, it tries a completely different approach, and after several iterations you're wondering if it would've been faster to just write it yourself?"

### Key Points to Cover
- **The frustration loop** - Show the chat transcript example on screen, highlight how the conversation spirals
- **The core insight** - Emphasize "Most failures are CONTEXT failures, not model failures"
- **Quick table scan** - Point to the comparison table showing how problems cascade
- **The promise** - "Context Engineering solves all of this by being systematic about what information AI receives"

### Visual Reference
Slide shows chat transcript, failure quote, and problem/result table

### Transition to Next
"So what exactly IS Context Engineering? Let's define it properly..."

### If You Get Lost - Core Message
**"AI fails because it lacks context, not because the model is bad. Context Engineering fixes this."**

### Time Checkpoint
Should be at ~1:30 mark

---

## SLIDE 2: What is Context Engineering? (2m 0s) ⏱️ 1:30-3:30

### Opening Hook
"Context Engineering is fundamentally different from prompt engineering. Prompt engineering is about clever wording. Context Engineering is about building a complete system."

### Key Points to Cover
1. **Diagram walkthrough** - Point to the visual comparison
   - Left side (Prompt): One box, limited
   - Right side (Context): Four components working together

2. **The three levels table**
   - Vibe coding: Low effectiveness (casual, no structure)
   - Prompt engineering: Medium effectiveness (better wording, still limited)
   - Context Engineering: High effectiveness (10x better than prompts - systematic approach)
   - **Pause and emphasize the 10x improvement** - let that sink in

3. **Core philosophy**
   - "It's not just WHAT to build, but HOW to build it according to YOUR standards"
   - Documentation + Examples + Rules + Validation

### Visual Reference
Mermaid diagram showing divergence, plus comparison table

### Audience Engagement
"Show of hands - who's currently in the 'vibe coding' camp? Prompt engineering? That's fine - we're going to move everyone to Context Engineering today."

### Transition to Next
"Let me show you the actual architecture that makes this possible..."

### If You Get Lost - Core Message
**"Context Engineering = systematic approach with 4 components: docs, examples, rules, validation. 10x better than prompt engineering."**

### Time Checkpoint
Should be at ~3:30 mark

---

## SLIDE 3: The Architecture (2m 0s) ⏱️ 3:30-5:30

### Opening Hook
"Context Engineering has four core components that work together. Think of them like the foundation of a house - you need all four for stability."

### Key Points to Cover

1. **Top diagram walkthrough** (30s)
   - CLAUDE.md → Global rules (dark gray) - "Your project's constitution"
   - INITIAL.md → Feature request (blue) - "What you want to build"
   - PRPs → Implementation blueprints (green) - "How to build it"
   - examples/ → Code patterns (pink) - "What good looks like"
   - Flow to working implementation (gray)

2. **Component table** (45s)
   - Quick scan through each row
   - Emphasize CLAUDE.md is set once, reused everywhere
   - INITIAL.md is per-feature
   - PRPs are auto-generated from INITIAL
   - examples/ is your pattern library that grows over time

3. **File structure** (45s)
   - ".claude/commands - where the magic slash commands live"
   - "PRPs folder - where your blueprints are stored"
   - "examples folder - THIS IS CRITICAL - your AI learns from these"
   - Point out the two slash commands

### Visual Reference
Two diagrams (flow + file tree) plus table

### Critical Point to Emphasize
**"The examples/ folder is your secret weapon. The more real code examples you provide, the better your results. Don't skip this."**

### Transition to Next
"Now let's see how these components work together in the actual workflow..."

### If You Get Lost - Core Message
**"Four components: CLAUDE.md (rules), INITIAL.md (request), PRPs (blueprint), examples/ (patterns). All work together."**

### Time Checkpoint
Should be at ~5:30 mark

---

## SLIDE 4: The Workflow (2m 30s) ⏱️ 5:30-8:00

### Opening Hook
"This is where it gets really cool. Watch how we go from idea to working code with automatic validation."

### Key Points to Cover

1. **Follow the flow diagram** (90s)
   - Step 1: "You write INITIAL.md - just describe what you want"
   - Step 2: "Run /generate-prp command"
   - **Pause at analysis node** - "AI researches your codebase, reads examples, fetches docs"
   - Step 3: "PRP created with confidence score"
   - **Point out confidence score** - "AI tells you if it has enough context"
   - Step 4: "Run /execute-prp command"
   - **Pause at validation loop** - "This is the magic"

2. **The validation loop** (60s)
   - "AI doesn't just write code and stop"
   - "It runs tests, checks linting, validates functionality"
   - "If tests fail, it FIXES THE ISSUES AUTOMATICALLY"
   - "Loops until everything passes"
   - "This is why Context Engineering is 10x more effective than prompt engineering"

### Visual Reference
Flowchart with decision points and loops

### Critical Emphasis
Voice emphasis on "automatic self-correction" - this is what makes CE powerful

### Audience Engagement
"This validation loop is what separates Context Engineering from everything else. AI becomes self-correcting."

### Transition to Next
"Let's drill into how you actually write a good INITIAL.md file..."

### If You Get Lost - Core Message
**"Four-step workflow: Write INITIAL.md → generate PRP → execute PRP → automatic validation loop until tests pass."**

### Time Checkpoint
Should be at ~8:00 mark (halfway point!)

---

## SLIDE 5: Crafting INITIAL.md (2m 0s) ⏱️ 8:00-10:00

### Opening Hook
"INITIAL.md is your feature specification. The quality of your INITIAL.md directly determines the quality of your implementation. Let me show you the template..."

### Key Points to Cover

1. **Template overview** (30s)
   - "Four sections, all essential"
   - Scan through: FEATURE, EXAMPLES, DOCUMENTATION, OTHER CONSIDERATIONS
   - "Think of it as giving AI a complete brief"

2. **Good vs Bad table** (60s)
   - **Row 1 (Auth)**: "Bad: vague. Good: specific technology, integration points, timing"
   - **Row 2 (Performance)**: "Bad: subjective. Good: measurable targets, specific techniques"
   - **Row 3 (Testing)**: "Bad: no guidance. Good: exact patterns, coverage targets, mocking approach"
   - **Key insight**: "Notice how the good examples reference specific files and numbers"

3. **Power technique** (30s)
   - Read the examples section
   - "Don't just say 'follow our patterns' - LINK TO SPECIFIC FILES"
   - "Each link is a training example for the AI"
   - "More examples = better results, it's that simple"

### Visual Reference
Template structure and comparison table

### Critical Emphasis
**"Be specific. Link to examples. Set measurable criteria. These three things will 10x your results."**

### Transition to Next
"Once you have a good INITIAL.md, here's what happens when you run /generate-prp..."

### If You Get Lost - Core Message
**"INITIAL.md has 4 sections. Be specific, link to example files, set measurable criteria. Quality in = quality out."**

### Time Checkpoint
Should be at ~10:00 mark

---

## SLIDE 6: PRP Generation Magic (2m 0s) ⏱️ 10:00-12:00

### Opening Hook
"When you run /generate-prp, a lot happens behind the scenes. Let me pull back the curtain..."

### Key Points to Cover

1. **Process diagram** (45s)
   - "Takes your INITIAL.md"
   - "Research phase: scans codebase, fetches docs, analyzes examples"
   - "Blueprint creation: synthesizes everything into step-by-step plan"
   - "Outputs PRP with four key sections"

2. **PRP structure example** (75s)
   - "Research summary - AI shows its work"
   - **Point out numbers**: "Analyzed 47 files - AI is thorough"
   - "Implementation steps - notice the pattern references"
   - **Validation gates**: "This is crucial - each step has a validation command"
   - **Confidence score**: "9/10 means AI has high confidence it can succeed"
   - "If confidence is low (<7), you might need better examples or clearer requirements"

### Visual Reference
Flow diagram and PRP output example

### Critical Insight
"The PRP is like a contract. AI is saying 'I understand what you want, here's my plan, and I'm X% confident I can execute it.' You can review before execution."

### Audience Engagement
"You can edit the PRP before executing. It's not a black box - you're in control."

### Transition to Next
"Before we see a real example, let me share the five golden rules for success..."

### If You Get Lost - Core Message
**"/generate-prp researches codebase + docs, creates blueprint with validation gates, outputs confidence score. Review before executing."**

### Time Checkpoint
Should be at ~12:00 mark

---

## SLIDE 7: 5 Golden Rules (2m 0s) ⏱️ 12:00-14:00

### Opening Hook
"I've distilled Context Engineering success down to five golden rules. Follow these and you'll be in the top 10% of AI-assisted developers."

### Key Points to Cover

1. **Table walkthrough** (60s)
   - **Rule 1 - Be Explicit**: "Don't assume. State requirements clearly. Quick win: always specify tech stack"
   - **Rule 2 - Show Examples**: "AI learns from code better than prose. Quick win: create examples/ folder with 5-10 files"
   - **Rule 3 - Use Validation**: "Tests catch mistakes. Quick win: add test commands to every PRP step"
   - **Rule 4 - Link Documentation**: "AI can fetch and use official docs. Quick win: include specific URLs"
   - **Rule 5 - Customize CLAUDE.md**: "One-time setup, permanent benefit. Quick win: add your style guide"

2. **Pitfalls diagram** (30s)
   - "Common mistakes and their consequences"
   - Quick visual scan
   - "All preventable with the 5 rules"

3. **Power law** (30s)
   - "80% of success from 20% of effort"
   - "Focus on: good INITIAL.md, validation commands, clear CLAUDE.md"
   - "These three things will carry you far"

### Visual Reference
Best practices table and pitfalls diagram

### Critical Emphasis
**"If you only remember three things: 1) Link to example files, 2) Add validation commands, 3) Be specific. That's it."**

### Transition to Next
"Let's see all of this in action with a real example..."

### If You Get Lost - Core Message
**"Five rules: be explicit, show examples, use validation, link docs, customize CLAUDE.md. Focus on examples + validation for biggest wins."**

### Time Checkpoint
Should be at ~14:00 mark

---

## SLIDE 8: See It In Action (1m 30s) ⏱️ 14:00-15:30

### Opening Hook
"Let me show you a real example from start to finish. We're building an async web scraper."

### Key Points to Cover

1. **INITIAL.md walkthrough** (30s)
   - "Feature section: specific requirements with numbers"
   - "Examples section: links to three different patterns"
   - "Documentation: specific library docs"
   - "Considerations: edge cases and constraints"
   - "This took maybe 5 minutes to write"

2. **PRP excerpt** (20s)
   - "AI generated this blueprint"
   - "Notice validation commands for each step"
   - "Coverage targets specified"

3. **Execution result** (40s)
   - Walk through checkmarks
   - "All tests pass automatically"
   - "Coverage exceeded target"
   - **Emphasize speed**: "Feature complete in minutes, not hours"
   - "From idea to tested, working code - dramatically faster than traditional coding"

### Visual Reference
Three-part example: INITIAL → PRP → Results

### Critical Moment
**"This is what's possible when you provide good context. Working, tested code in minutes, not hours."**

### Audience Engagement
"And this isn't cherry-picked - this is typical when you follow the system."

### Transition to Next
"Alright, let's wrap up and get you started..."

### If You Get Lost - Core Message
**"Real example: specific INITIAL.md → detailed PRP → working code in minutes. Context Engineering delivers."**

### Time Checkpoint
Should be at ~15:30 mark

---

## SLIDE 9: Your Journey Starts Now (30s) ⏱️ 15:30-16:00

### Opening Hook
"You now understand Context Engineering. Here's how to start today."

### Key Points to Cover

1. **Quick start checklist** (15s)
   - "Clone the repository" (point to link)
   - "Customize CLAUDE.md for your project"
   - "Add examples - this is the most important step"
   - "Write INITIAL.md, run the commands, see results"

2. **Resources** (10s)
   - Point to table
   - "There's also a hands-on tutorial for deeper learning"

3. **Key takeaway** (5s)
   - "Good context → reliable AI → better code → faster development"
   - "Context Engineering is 10x better than prompt engineering"

### Visual Reference
Checklist, resources table, and final flow diagram

### Closing
"I'll stick around for questions. Thank you!"

### If You Get Lost - Core Message
**"Clone repo, customize CLAUDE.md, add examples, try it. Tutorial available for deeper dive."**

### Time Checkpoint
Should be at ~16:00 mark - DONE!

---

## Questions Section (Variable Time)

### Common Questions & Answers

**Q: "How many examples do I need?"**
A: "Start with 5-10 that cover your most common patterns. You can add more over time. Quality over quantity - make sure they're real, working code."

**Q: "What if my codebase is huge?"**
A: "That's fine. The examples/ folder is the AI's reference library, not a complete copy. Show representative patterns. CLAUDE.md keeps it focused."

**Q: "Can this work with [framework X]?"**
A: "Yes. Context Engineering is framework-agnostic. Just provide examples in your framework and link to relevant docs."

**Q: "What about security/sensitive code?"**
A: "Use Claude Code locally, or sanitize examples. Never put credentials in examples/ or INITIAL.md."

**Q: "How long does setup take?"**
A: "Initial setup: 1-2 hours to customize CLAUDE.md and create first examples. After that, each new feature is faster."

**Q: "Can multiple people use the same Context Engineering setup?"**
A: "Absolutely! That's a huge benefit. Shared CLAUDE.md and examples/ means consistent code across your team."

---

## Emergency Recovery Points

### If Technology Fails
"The key concept is simple: AI needs context, not just prompts. Context Engineering provides that context systematically through four components: rules, examples, blueprints, and validation. The repository has everything you need to get started."

### If Running Behind on Time
**Skip to priorities:**
1. Keep Slides 1, 2, 4, 8, 9 (problem, solution, workflow, example, next steps)
2. Condense Slides 3, 5, 6, 7 into verbal summaries

### If Running Ahead on Time
**Expand on:**
- Live demo of creating an INITIAL.md
- Show actual PRP file in detail
- Walk through customizing CLAUDE.md

---

## Pre-Presentation Checklist

- [ ] Test all Mermaid diagrams render correctly
- [ ] Have repository URL ready to share
- [ ] Prepare to screen share (if doing live demo)
- [ ] Water nearby
- [ ] Timer visible
- [ ] Know your audience (adjust technical depth)

---

## Post-Presentation

**Direct attendees to:**
1. Repository: github.com/coleam00/context-engineering-intro
2. Tutorial: `ce-hands-on-tutorial.md`
3. Your contact info for follow-up questions

**Key success metric:**
"Did attendees understand that Context Engineering is systematic, not magical?"

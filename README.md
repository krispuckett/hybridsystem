# Hybrid System

A productivity system that bridges pen-and-paper workflow with AI-powered digital intelligence.

**Morning:** AI generates daily priorities  
**Day:** Work from a physical card  
**Evening:** Photo your card → AI reads handwriting → updates everything automatically

Built with [Craft Docs](https://craft.do), [Claude Code](https://docs.claude.com/en/docs/claude-code), and Craft's MCP server.

## Quick Start

**Requirements:**
- macOS
- [Craft Docs](https://www.craft.do) (free tier works)
- [Claude Code](https://docs.claude.com/en/docs/claude-code) (requires Claude subscription)

**Install:**
```bash
git clone https://github.com/krispuckett/hybridsystem.git
cd hybridsystem
./install.sh
```

**Setup takes 10 minutes.** Follow the [Setup Guide](docs/SETUP.md).

## How It Works

### Three Connected Documents

**The Watchtower** (Daily Hub)
- Morning briefing with prioritized tasks
- Field reports for quick captures
- Links to your task pool

**The Forge** (Task Pool)
- Organized by energy/context
- Deep Work, Standard Tasks, Light Work, Someday

**The Long Road** (Journey Tracker)
- Work/rest cycle tracking
- Pattern recognition over time
- Insights from reflections

### Daily Workflow

**Morning (5 min):**
```bash
watchtower brief
```
Generates priorities. Write top 3-5 on a physical card.

**Evening (5 min):**
```bash
watchtower card
```
Drag card photo into terminal. AI reads handwriting, updates tasks automatically.

**Anytime:**
```bash
watchtower add "task description" normal
watchtower journal  # Process journal entries
watchtower status   # See system overview
```

## Why It Works

**The constraint of paper forces real prioritization.**  
**The intelligence of digital routes you to the right work.**

Low energy isn't failure—it's a signal to do different work, not no work.

## Technical Details

**Vision AI** reads handwritten text (~90% accuracy on cursive)  
**Craft MCP** enables direct document updates via Model Context Protocol  
**Bash scripts** handle automation without complex dependencies

Everything runs locally. Your data stays yours.

# Watchtower System - Quick Reference

## Daily Workflow Commands

### Morning Routine

```bash
watchtower brief          # Generate priorities for today
watchtower energy         # Check if you should even be working
```

### During the Day

```bash
watchtower add "task description" [energy]
# Energy: high, normal, low, someday
# Example: watchtower add "Research Metal shaders" high

watchtower capture        # Brain dump mode (paste multiple thoughts)
watchtower work "project" # Start focused deep work session
```

### Evening Routine

```bash
watchtower card           # Process card photo (drag & drop)
watchtower energy         # Check energy & log it
```

### Anytime

```bash
watchtower journal        # Process journal entry (drag & drop)
watchtower status         # See current sprint, tasks, alerts
watchtower context        # Check/manage Claude Code context
```

## Energy Levels Explained

**high** → Deep Work Forging (complex, creative, demanding) **normal** → Standard Forge Work (productive, routine tasks)**low** → Light Smithing (admin, organizing, easy wins) **someday** → The Anvil Awaits (ideas for later)

## When to Use Each Command

**Morning (5 min):**
1. `watchtower brief` - Get today's priorities
2. Check Craft Watchtower doc
3. Write top 3-5 on physical card
4. Work from card all day

**Scattered moment:**
- One quick task → `watchtower add`
- Multiple thoughts → `watchtower capture`

**Ready for deep work:**
- `watchtower energy` (check you're ready)
- `watchtower work "project name"`

**Evening (5 min):**
1. `watchtower card` - Photo your card
2. Answer energy question
3. Done - tomorrow is prepped

**Before bed (optional):**
- `watchtower journal` - Process reflections

## The Three Craft Documents

**The Watchtower** = Daily command center
- Morning briefing
- Today's priorities
- Field reports (quick captures)

**The Forge** = Task pool (organized by energy)
- Deep Work Forging
- Standard Forge Work
- Light Smithing
- The Anvil Awaits

**The Long Road** = Journey tracking
- Sprint days & energy patterns
- Insights from journaling
- Burnout warnings

## Tips

**Context Management:**
- Start fresh Claude session for each deep work project
- Use `/clear` between daily tasks (brief, card, etc.)
- Kill & restart Claude Code every 2-3 days

**Energy Windows:** Your peak times:
- 9am-1pm
- 3:30-5:30pm
- 8-10pm

Save deep work for these windows.

**Signs to Stop:**
- Sprint day 6+
- Feeling depleted
- Scattered with no focus
- Forcing it when stuck

→ Run `watchtower energy` for guidance

## Quick Troubleshooting

**Scripts not working?**

```bash
chmod +x /usr/local/bin/watchtower/*.sh
```

**Craft not updating?**

```bash
claude mcp list  # Check connections
```

**Need help?**

```bash
watchtower  # Shows all commands
```

---

# THE WATCHTOWER COACHING SYSTEM

## Evidence-Based Wisdom, Zero Platitudes

---

## PHILOSOPHY

This isn't motivational speaking. This is pattern recognition, Stoic wisdom, and neuroscience research applied to YOUR actual data.

**Influences:**
- **Stoicism:** Marcus Aurelius, Seneca, Epictetus (the actual texts)
- **Leadership:** Aragorn's patient kingship, Rumelt's strategic clarity, Sinek's purpose-driven thinking
- **Modern Stoicism:** Ryan Holiday's practical application
- **Neuroscience:** Peer-reviewed research only

**Tone:**
- Thoughtful, not preachy (like Ryan Holiday writes)
- Specific, not generic
- Questions more than answers
- Honest about what's working and what's not

**Never:**
- "Here's the honest truth..."
- "Let me be clear..."
- Cheerleading or motivational speak
- Babying or sycophantic praise

---

## COACHING COMMANDS

### `watchtower coach`

**Deep coaching session**

Analyzes your three documents (Watchtower, Forge, Long Road) and:
- Notices patterns you might miss
- Connects them to Stoic principles or neuroscience
- Asks probing questions
- Challenges assumptions

**Use when:** You want real insight, not task management

**Example output:**

```
You've completed 8/12 deep work tasks but pushed the Metal shader 
work five times. Seneca wrote about how we're 'always preparing 
to live, never actually living.' What would happen if you just 
started the shader work tomorrow, even badly?
```

---

### `watchtower patterns`

**Pattern recognition from your data**

Looks across time for:
- Task avoidance patterns (what gets pushed repeatedly?)
- Energy-performance alignment (claims vs. results)
- Decision bottlenecks
- Sprint/crash predictability

Uses Rumelt's strategic framework:
1. Diagnosis (what's actually happening)
2. Guiding Policy (what principle applies)
3. Coherent Actions (what to do about it)

**Use when:** Things feel off but you can't pinpoint why

**Example output:**

```
Three journal entries mention 'scattered.' Completion rate drops 
40% on those days. Research on working memory (Baddeley, 1974) 
shows capacity of ~4 items. What unresolved decisions are you 
carrying that could be made or discarded?
```

---

### `watchtower weekly`

**Strategic weekly review**

Not a task recap - a strategic analysis:
1. **The week in data** (sprint days, energy, completion rates)
2. **What's working** (specific, data-backed)
3. **What's not working** (direct, honest)
4. **Strategic question** (one good question for next week)
5. **Neuroscience note** (if relevant)

**Use when:** End of week, planning ahead

**Example output:**

```
THE WEEK IN DATA
Days 8-14 of sprint. Energy: 4 high, 2 medium, 1 recovery. 
Deep work: 6/9 completed (67%).

WHAT'S WORKING
Medium-energy task routing is effective - 11/12 completed. 
When you match energy to task type, you execute.

WHAT'S NOT WORKING
You planned 9 deep work sessions but completed 6. The gap 
isn't energy - it's sprint day 12 and burnout signals are 
showing. Marcus: 'You could be good today, but instead you 
choose tomorrow.'

STRATEGIC QUESTION
Your journal mentions wanting autonomy three times. You're 
interviewing at Ramp while building Epilogue. Which path 
actually gives you what you're seeking?

NEUROSCIENCE NOTE
Ultradian rhythms suggest 90-minute focus blocks. Your 
9am-1pm window is 4 hours - you're likely hitting diminishing 
returns. What if you planned in 90-minute sprints with breaks?
```

---

### `watchtower challenge [topic]`

**Get challenged on something specific**

Direct confrontation with a pattern you're stuck in.

**Use when:** You know you're avoiding something

**Examples:**

bash

```bash
watchtower challenge "my sprint length"
watchtower challenge "why I keep pushing the shader work"
watchtower challenge "my job search vs. building Epilogue"
```

**Example output:**

```
CHALLENGE: Why you keep pushing the shader work

You've planned it 7 times across 14 days. Completed it: 0 times.

Your notes say "need to research best approach" - but you've 
built shaders before. You know how.

Epictetus: "How long will you wait before you demand the best 
of yourself?"

What's the real resistance? Technical complexity, or fear 
it won't be as good as you imagine?
```

---

### `watchtower stoic`

**Stoic reflection exercise**

Guided reflection using classical Stoic practices:
1. **Dichotomy of Control** - What can you control vs. not?
2. **Premeditatio Malorum** - What's the worst case?
3. **Memento Mori** - Given limited time, what matters?
4. **View from Above** - Zoom out perspective
5. **Obstacle as Opportunity** - How is friction training?

System picks the most relevant one based on your Long Road data.

**Use when:** Feeling stuck, anxious, or need perspective

**Example output:**

```
PREMEDITATIO MALORUM (Negative Visualization)

Seneca: 'Set aside a certain number of days to be content 
with the scantiest food.'

What if the consulting business fails completely? Visualize 
it fully.
What if you stay at Shopify another year? See it clearly.

Which fear is actually worse? The one you're running from, or 
the one you're running toward?
```

---

## HOW THE COACHING WORKS

### It Reads Your Actual Data

Not generic advice. Specific patterns from:
- Your completed/incomplete tasks
- Your energy notes over time
- Your journal reflections
- Your sprint duration
- Your task avoidance patterns

### It Applies Frameworks

- **Stoic philosophy:** Actual quotes from Marcus, Seneca, Epictetus
- **Neuroscience:** Peer-reviewed research (see NEUROSCIENCE-REFERENCE.md)
- **Strategy:** Rumelt's frameworks, Sinek's clarity, Aragorn's patience

### It Asks Better Questions

Not "how can you do better?" - that's useless.

Instead:
- "What's the real resistance?"
- "Which path gives you what you're seeking?"
- "What decisions could be made or discarded?"
- "What would happen if you started, even badly?"

---

## INTEGRATION WITH DAILY WORKFLOW

The coaching isn't separate - it's woven into your daily commands:

**Morning Briefing** (enhanced) Now includes:
- Sprint status observation
- Strategic insights when relevant
- Neuroscience notes about your energy windows

**Evening Debrief** (enhanced) Now notices:
- What type of tasks you completed vs. pushed
- Patterns in avoidance
- Asks clarifying questions when appropriate

**Always:**
- Concise (under 300 words)
- Specific (cites your data)
- Honest (no cheerleading)

---

## WHAT THIS IS NOT

❌ A motivational speaker ❌ A yes-man ❌ A task manager with inspirational quotes ❌ Generic AI platitudes ❌ Cheerleading

## WHAT THIS IS

✓ Pattern recognition from YOUR data ✓ Stoic wisdom applied to YOUR situation ✓ Neuroscience research relevant to YOUR patterns ✓ Strategic thinking about YOUR path ✓ Honest feedback grounded in evidence

---

## EXAMPLE SESSION

bash

```bash
$ watchtower coach

Reading your documents...

PATTERN OBSERVED:

You've been sprinting for 13 days. Completion rate was 80% 
on days 1-7, now 55% on days 8-13. Your journal entries show 
increasing mentions of "scattered" and "tired."

This isn't willpower failure. It's biology.

Research on allostatic load (McEwen, 1998) shows stress 
compounds without recovery. You're not weak - you're human.

Marcus Aurelius ran an empire and still needed rest. He 
wrote in Meditations: "Don't be ashamed to need help."

QUESTION:

What would a recovery day look like? Not "nothing" - what 
would actively restore you?

Maybe it's the thing you've been pushing because "there's 
no time."
```

---

## REFERENCES

See NEUROSCIENCE-REFERENCE.md for full research citations.

Key sources:
- Marcus Aurelius, "Meditations"
- Seneca, "Letters from a Stoic"
- Epictetus, "Enchiridion"
- Richard Rumelt, "Good Strategy Bad Strategy"
- Ryan Holiday, "The Obstacle is the Way"
- Peer-reviewed research on productivity, neuroscience, psychology

## Documentation

- [Setup Guide](docs/SETUP.md) - Initial configuration
- [Commands](docs/COMMANDS.md) - All available commands
- [Customization](docs/CUSTOMIZATION.md) - Adapt to your workflow
- [Troubleshooting](docs/TROUBLESHOOTING.md) - Common issues

## Screenshots

![Three Craft Documents](images/craft-docs.png)
![Physical Card Workflow](images/card-workflow.png)
![Terminal OCR Processing](images/terminal-ocr.png)

## Philosophy

This system assumes:
- Your capacity varies day-to-day
- Physical constraints improve focus
- Digital intelligence improves routing
- Quick capture prevents losing ideas
- Patterns emerge when tracked consistently

Built for people who work in energy waves, not steady streams.


## License

MIT - Use freely, modify as needed, share improvements.

## Acknowledgments

Built during one Saturday evening exploring what's possible with:
- [Craft's MCP server](https://www.craft.do/imagine/guide/mcp/claude_code)
- [Claude Code](https://docs.claude.com/en/docs/claude-code)
- [Model Context Protocol](https://modelcontextprotocol.io)

## Questions?

Open an issue or reach out: [@krispuckett](https://twitter.com/krispuckett) on Twitter

---

**Cost:** $0 (with existing Claude subscription)  
**Setup time:** 10 minutes  
**Daily overhead:** 10 minutes (5 min morning + 5 min evening)

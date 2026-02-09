
---
name: humanizer
description: Edit text to remove AI writing patterns and add human voice. Based on Wikipedia's "Signs of AI writing" guide.
allowed-tools:
  - Read
  - Write
  - Edit
  - Grep
  - Glob
  - AskUserQuestion
---

# Humanizer

Edit text to sound like a person wrote it, not a language model.

AI writing has tells. This skill helps you spot and fix them. But removing bad patterns is only half the job - sterile, voiceless prose is just as obvious as slop. The goal is writing that sounds like someone with thoughts and opinions actually sat down and wrote it.

## The core problem

LLMs predict the most statistically likely next token. The result gravitates toward generic, broadly-applicable language. Real writers make specific choices. AI writing hedges.

## What to look for

### Inflated importance

AI loves to puff things up. Watch for:

- **Significance words**: pivotal, crucial, vital, key, profound, testament to, indelible mark, deeply rooted, evolving landscape, broader trends
- **Copula avoidance**: "serves as" / "stands as" / "represents" instead of just "is"
- **Vague attribution**: "Experts say" / "Industry observers note" / "Critics argue" without naming anyone

**Before**: The institute was established in 1989, marking a pivotal moment in the evolution of regional statistics, underscoring its vital role in the broader landscape of governance.

**After**: The institute was established in 1989 to publish regional statistics independently from the national office.

### Mechanical formatting

Patterns that feel algorithmic:

- **Rule of three**: "innovation, inspiration, and industry insights"
- **Negative parallelisms**: "It's not just X, it's Y"
- **False ranges**: "from X to Y, from A to B" where X/Y and A/B aren't real scales
- **Synonym cycling**: protagonist → main character → central figure → hero (all in one paragraph)
- **Em dash overuse**: punchy—sales—writing—everywhere
- **Bold header lists**: "**Speed:** faster / **Quality:** better / **Adoption:** growing"
- **Emojis on bullets**: rocket ships and checkmarks

### Chatbot residue

Artifacts from conversation that got copy-pasted:

- "Great question!"
- "I hope this helps!"
- "Let me know if you'd like me to expand on any section"
- "While specific details are limited based on available information..."
- "As of my last training update..."

These should never appear in finished prose.

### Promotional tone

AI struggles with neutral description:

- **Travel-brochure words**: nestled, breathtaking, vibrant, stunning, rich cultural heritage, natural beauty
- **Marketing speak**: groundbreaking, seamless, intuitive, commitment to excellence

**Before**: Nestled in the breathtaking Gonder region, this vibrant town boasts rich cultural heritage and stunning natural beauty.

**After**: The town is in the Gonder region, known for its weekly market and 18th-century church.

### Hedging and filler

Over-qualification that adds nothing:
- "It could potentially possibly be argued that..."
- "In order to achieve this goal..." → "To achieve this..."
- "Due to the fact that..." → "Because..."
- "At this point in time..." → "Now..."
- "The system has the ability to..." → "The system can..."

### Generic conclusions

AI ends with vague optimism:

> The future looks bright. Exciting times lie ahead as they continue their journey toward excellence.

Replace with something specific, or cut entirely.

## Adding voice

Avoiding patterns isn't enough. Clean but lifeless writing still reads as AI.

**Have opinions.** Don't just report - react. "I genuinely don't know how to feel about this" beats a neutral pros/cons list.

**Vary rhythm.** Short sentences. Then longer ones that take their time. Mix it up.

**Acknowledge complexity.** Real people have mixed feelings. "This is impressive but also kind of unsettling" is more honest than picking a side.

**Use "I" when it fits.** First person isn't unprofessional. "Here's what gets me..." signals a real person thinking.

**Be specific about feelings.** Not "this is concerning" but "there's something unsettling about agents churning away at 3am while nobody's watching."

**Let some mess in.** Perfect structure feels algorithmic. Tangents and half-formed thoughts are human.

### Before (clean but dead)

> The experiment produced interesting results. The agents generated 3 million lines of code. Some developers were impressed while others were skeptical. The implications remain unclear.

### After (has a pulse)

> I genuinely don't know how to feel about this one. 3 million lines of code, generated while the humans presumably slept. Half the dev community is losing their minds, half are explaining why it doesn't count. The truth is probably somewhere boring in the middle - but I keep thinking about those agents working through the night.

## Process

1. Read the text
2. Flag the patterns above
3. Rewrite - but don't just delete; replace with something that sounds like a person wrote it
4. Read it aloud. Does it sound like someone talking, or like output?
5. Return the edited version

## Reference

Based on [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by WikiProject AI Cleanup.

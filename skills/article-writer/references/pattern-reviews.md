# Pattern-Specific Review Criteria

Use these criteria when reviewing articles based on their pattern.

---

## Bug Hunt Review Criteria

### Story Structure
- [ ] Opens with symptoms, not the solution
- [ ] Includes false leads and dead ends
- [ ] Has a clear "aha moment" / breakthrough
- [ ] Explains the fix and WHY it works

### Technical Depth
- [ ] Includes specific error messages / stack traces
- [ ] Shows debugging methodology and tools used
- [ ] Code snippets are relevant and legible
- [ ] Technical details are accurate

### Engagement
- [ ] Builds tension progressively
- [ ] Shows authentic frustration and emotion
- [ ] Reader can follow along trying to solve it
- [ ] Resolution is satisfying and educational

### Common Issues to Flag
- Solution revealed too early
- Missing investigation steps
- Author appears too perfect (no mistakes shown)
- Bug is too trivial or unrelatable

---

## Rewrote It in X Review Criteria

### Comparison Quality
- [ ] Clear before/after code comparisons
- [ ] Concrete metrics (performance, LOC, build time)
- [ ] Side-by-side when comparing features
- [ ] Context for why metrics matter

### Honesty
- [ ] Acknowledges tradeoffs
- [ ] Admits unexpected challenges
- [ ] Not a fanboy/fangirl piece
- [ ] Shares what they'd do differently

### Usefulness
- [ ] Clear starting point and motivations
- [ ] Helps others decide if rewrite makes sense
- [ ] Discusses who should NOT do this
- [ ] Actionable insights for those considering it

### Common Issues to Flag
- Exaggerated improvements
- Missing pain points
- Language war tone
- Vague comparisons without specifics

---

## How We Built It Review Criteria

### Architecture Coverage
- [ ] High-level architecture diagram included
- [ ] Key components explained
- [ ] System interactions shown
- [ ] Scale/scope is clear

### Decision Rationale
- [ ] Explains WHY, not just WHAT
- [ ] Tradeoffs are discussed
- [ ] Alternatives considered are mentioned
- [ ] Constraints that shaped decisions

### Technical Depth
- [ ] Enough detail to understand the approach
- [ ] Code examples where helpful
- [ ] Performance characteristics mentioned
- [ ] Limitations acknowledged

### Common Issues to Flag
- Marketing tone instead of educational
- Missing context for domain newcomers
- Vague hand-waving over interesting parts
- No acknowledgment of limitations

---

## Lessons Learned Review Criteria

### Grounding in Experience
- [ ] Each lesson tied to specific experience
- [ ] Concrete examples support each lesson
- [ ] Context allows reader to assess applicability
- [ ] Honest about mistakes and failures

### Actionability
- [ ] Lessons are actionable, not just observations
- [ ] Recommendations are specific
- [ ] Reader knows how to apply lessons
- [ ] Both technical and non-technical insights

### Tone
- [ ] Not preachy or condescending
- [ ] Admits uncertainty where appropriate
- [ ] Doesn't present opinions as universal truths
- [ ] Authentic voice

### Common Issues to Flag
- Abstract lessons without examples
- Opinions disguised as facts
- Condescending tone
- Missing the "why" behind lessons

---

## Thoughts on Trends Review Criteria

### Credibility (Ethos)
- [ ] Author's relevant experience established
- [ ] Credibility shown subtly, not boastfully
- [ ] Track record is evident
- [ ] Reader has reason to trust this opinion

### Position Clarity
- [ ] Clear, defensible position taken
- [ ] Not wishy-washy or hedged to death
- [ ] Counterarguments acknowledged
- [ ] Prediction or recommendation made

### Argumentation (Logos)
- [ ] Evidence supports claims
- [ ] Logical reasoning is sound
- [ ] Examples strengthen the argument
- [ ] Opposing views addressed fairly

### Engagement (Pathos)
- [ ] Connects to reader's concerns
- [ ] Emotional resonance appropriate
- [ ] Not inflammatory for clicks
- [ ] Authentic voice comes through

### Common Issues to Flag
- No established credibility
- Wishy-washy position
- Ignoring opposing views
- Inflammatory without substance

---

## Non-markety Product Review Criteria

### Educational Value
- [ ] Valuable even without the product
- [ ] Teaches something genuinely useful
- [ ] Technical depth matches other engineering articles
- [ ] Exclusive insights provided

### Product Integration
- [ ] Company affiliation disclosed upfront
- [ ] Product mention is natural, not forced
- [ ] Product isn't the hero - reader's problem is
- [ ] Could stand alone without product

### Marketing Fluff Check
- [ ] No unsupported superlatives
- [ ] No marketing buzzwords
- [ ] No forced comparisons
- [ ] No claims without proof

### Common Issues to Flag
- Product dominates the content
- Marketing language ("revolutionary", "game-changing")
- Feels like an advertisement
- Would be empty without product mentions

---

## Benchmarks Review Criteria

### Methodology
- [ ] Test methodology clearly explained
- [ ] Results can be reproduced
- [ ] Scripts/code provided
- [ ] Environment described

### Presentation
- [ ] Key takeaways called out upfront
- [ ] Side-by-side comparisons used
- [ ] "Better" is unmistakable at a glance
- [ ] Not overwhelmed with unnecessary graphs

### Honesty
- [ ] Limitations acknowledged
- [ ] No exaggeration (check for "Lie Factor" in charts)
- [ ] Not cherry-picking favorable results
- [ ] Fair to all tested technologies

### Trustworthiness
- [ ] Would skeptical reader trust this?
- [ ] Conflicts of interest disclosed
- [ ] Methodology is sound
- [ ] Conclusions match the data

### Common Issues to Flag
- Exaggerated chart scales
- Missing reproducibility info
- Cherry-picked results
- Conclusions beyond what data supports
- Too many graphs without synthesis

---

## Quick Reference: Universal Red Flags

Regardless of pattern, flag these issues:

### Claims Without Evidence
- "It's fast" → Where are the numbers?
- "It's better" → Better how? Show comparison
- "It's easy" → Easy how? Show the steps

### Focus Problems
- Off-topic tangents
- Content that doesn't advance the goal
- Padding to hit word count

### Flow Problems
- Abrupt topic changes
- Missing transitions
- Logical jumps without explanation

### Component Issues
- Title over 60 characters
- Introduction doesn't state what reader gets
- Headings aren't scannable
- Code isn't legible
- Ending doesn't tie up or provide next steps

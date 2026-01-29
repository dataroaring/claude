# Visual & Code Presentation Skills

Based on "Writing for Developers" by Piotr Sarna & Cynthia Dunlop

---

## Headings

Headings are signposts that help readers scan and navigate your article.

### Keep Them Short

- Aim for shortest possible words that orient readers
- Long headings in big bold fonts overwhelm rather than help
- If a heading extends over multiple lines, try trimming it

### Put Key Words First

Readers scan left to right. Don't make them wade through filler to reach important words.

**Bad:**
```
Configuration A vs. Configuration B: Throughput
Configuration A vs. Configuration B: Latency
```

**Good:**
```
Throughput Results
Latency Results
```

### Maintain Proper Hierarchy

Use heading levels correctly: H1 >> H2 >> H3 >> H4

**Don't:**
- Change heading levels just to change font size
- Skip levels (e.g., H1 → H3)

**Why it matters:**
- Accessibility (screen readers use hierarchy)
- SEO (search engines use hierarchy)
- Reader orientation

### Consider Numbering

If your article has deep nesting, consider numbering sections to help readers understand where they are:
- 1. Main Topic
  - 1.1 Subtopic
  - 1.2 Subtopic

### Make Headings Answer Questions

Anticipate what the reader is wondering at each point in the article. Frame headings as answers to those questions.

**Instead of:**
```
Background
Implementation
Results
```

**Consider:**
```
Why We Needed a New Approach
How We Built the Solution
What We Achieved (and What Surprised Us)
```

---

## Visuals (Images, Diagrams, Graphs)

### Always Add Captions

Every meaningful image should have a caption that:
- Explains what the image shows
- Highlights what's important to notice
- Provides context for the data

**Why:**
- Helps readers understand meaning quickly
- Critical for accessibility
- Useful when images fail to load

### Consider Color-Blindness

**Statistics:**
- 8% of men are color-blind
- 0.4% of women are color-blind
- Given tech demographics, many of your readers may be affected

**Actions:**
- Use free color-blind simulators to test your images
- Don't rely solely on color to convey meaning
- Use patterns, labels, or shapes in addition to color

### Check Image Rights

**Rule:** Get permission, not forgiveness.

**Reality:** Copyright violations can cost tens of thousands of dollars, even for innocent mistakes.

**Safe options:**
- Create your own images
- Use royalty-free sources
- Get explicit permission
- Use images with appropriate Creative Commons licenses

### Size Images Appropriately

**File size:**
- Aim for under 100KB per image
- Use compression tools (tinyPNG, ImageMagick)
- Balance: smallest file size + highest quality

**Display size:**
- Ensure labels/text are readable at displayed size
- If details are lost, crop or redesign the image
- Allow click-to-enlarge for complex diagrams

### Types of Effective Visuals

- **Architecture diagrams** - System components and interactions
- **Flowcharts** - Process and decision flows
- **Sequence diagrams** - Interaction timelines
- **Flame graphs** - Performance profiling
- **Before/after comparisons** - Side-by-side changes
- **Screenshots** - UI and tool demonstrations
- **Data visualizations** - Charts, graphs, metrics

### The Lie Factor (Avoiding Deceptive Charts)

From Edward Tufte's "The Visual Display of Quantitative Information" - a critical concept for benchmark and data-driven articles.

**Definition:**
```
Lie Factor = (Size of effect shown in graphic) / (Size of effect in data)
```

A Lie Factor of 1.0 means the graphic accurately represents the data. Above 1.05 or below 0.95 indicates distortion.

**Common Ways Charts Lie:**

| Deception | Example | Fix |
|-----------|---------|-----|
| **Truncated Y-axis** | Starting at 90 instead of 0 makes 95 vs 100 look like 2x difference | Start axes at 0 or clearly mark truncation |
| **3D effects** | Perspective makes front bars look larger | Use flat 2D charts |
| **Area scaling** | Doubling a circle's radius quadruples its area | Use length, not area, for comparisons |
| **Cherry-picked timeframes** | Showing only the period where your product won | Show full relevant timeframe |
| **Missing context** | Showing raw numbers without baselines | Include baseline comparisons |

**Example of Lie Factor:**

Data: Performance improved from 100ms to 80ms (20% improvement)

❌ **Deceptive chart:** Bar heights of 1 inch vs 3 inches (Lie Factor = 3.0)
✅ **Honest chart:** Bar heights of 5 inches vs 4 inches (Lie Factor = 1.0)

**Checklist for Honest Charts:**

- [ ] Y-axis starts at 0 (or truncation is clearly marked)
- [ ] No 3D effects that distort perception
- [ ] Area comparisons use proportional areas
- [ ] Time periods are representative, not cherry-picked
- [ ] Both favorable AND unfavorable results shown
- [ ] Scale is consistent across compared items
- [ ] Lie Factor is between 0.95 and 1.05

**Why This Matters:**

Engineers are trained to scrutinize data. A deceptive chart will:
- Destroy your credibility
- Generate hostile comments
- Get called out on Hacker News
- Undermine your entire article

**Reference:** Edward Tufte's "The Visual Display of Quantitative Information" - essential reading for anyone presenting data.

### What NOT to Do

- Don't use images of code (use actual code blocks)
- Don't add purely decorative images that don't enhance understanding
- Don't use low-resolution images that pixelate when displayed
- Don't use images with text too small to read
- Don't use charts with Lie Factor > 1.05

---

## Code Examples

Code examples are critical for technical articles. Get them right.

### Code Must Be

**Shareable:**
- Get clearance for any closed-source code
- When in doubt, ask permission (not forgiveness)

**Well-vetted:**
- No embarrassing mistakes for commenters to find
- Get another pair of eyes on it
- Test that it actually compiles/runs

**Realistic:**
- Syntactically correct
- Compiles without errors
- Secure (people WILL copy-paste!)
- Uses realistic variable names and patterns

**Concise:**
- Omit irrelevant parts
- Use ellipses (...) to indicate omitted code
- Show only what's necessary to make your point

### Display Requirements

**Syntax highlighting:**
- Always use syntax highlighting
- Specify the language for proper highlighting
- Test in both light and dark modes

**Legibility:**
- Ensure adequate contrast
- Wrap at 80-120 characters
- Check that indentation wasn't mangled in copy-paste

**Copy-pasteable:**
- Never use images of code for functional examples
- Images prevent copying and break accessibility
- Reserve code images only for decorative thumbnails

### Better Display Options

**GitHub Gists:**
- Easy to embed
- Proper syntax highlighting
- Version controlled

**Interactive playgrounds:**
- Stackblitz
- Sandpack
- CodePen
- Language-specific playgrounds (Rust Playground, Go Playground)

**Benefits of playgrounds:**
- Readers can experiment immediately
- No setup required
- Proves your code actually works

### Link to Full Context

When showing code snippets, link to the full file/repo when possible:
- Helps readers see the code in context
- Allows them to explore further
- Shows you're not hiding anything

### Code Display Checklist

- [ ] Syntax highlighting enabled
- [ ] Language specified
- [ ] Legible in light AND dark mode
- [ ] Lines wrap appropriately (80-120 chars)
- [ ] Indentation preserved correctly
- [ ] Copy-paste works (not an image)
- [ ] Code compiles/runs
- [ ] Code is secure (no vulnerabilities to copy)
- [ ] Irrelevant parts omitted (with ...)
- [ ] Link to full context provided

---

## Tables

### When to Use Tables

- Comparing multiple items across same attributes
- Presenting structured data
- Showing before/after differences
- Listing options with pros/cons

### Table Best Practices

- Keep tables simple (complex tables don't render well)
- Use clear, short column headers
- Align numbers to the right
- Preview rendering in HTML (may need adjustment)
- Consider if a list would work better for simple data

### Example

**Good table use:**
```
| Language | Compile Time | Memory Usage |
|----------|-------------|--------------|
| Rust     | 45s         | 2.3GB        |
| Go       | 12s         | 1.1GB        |
| Zig      | 8s          | 0.9GB        |
```

---

## Lists

### When to Use Lists

- 3+ related items
- Step-by-step instructions
- Feature/benefit summaries
- Breaking up wall of text

### List Best Practices

- Use bullet points for unordered items
- Use numbers for sequential steps or rankings
- Keep list items parallel in structure
- Don't nest too deeply (2 levels max)
- Preview rendering (multilevel lists often break)

---

## Preview Checklist

Before publishing, preview on the actual platform and check:

### Title and Headings
- [ ] Title doesn't wrap awkwardly
- [ ] No single word dangling on its own line
- [ ] Headings aren't sprawling across multiple lines

### Code
- [ ] Syntax highlighting working
- [ ] Legible in dark and light mode
- [ ] Copy-paste produces correct code
- [ ] Indentation correct
- [ ] No characters cut off at start/end

### Images
- [ ] Displayed at appropriate size
- [ ] Labels/text readable
- [ ] Colors work for color-blind readers
- [ ] ALT text present

### Videos (if any)
- [ ] Appropriate size
- [ ] Plays when not logged into video platform (test in incognito)
- [ ] Available in target regions

### Tables and Lists
- [ ] Render correctly
- [ ] Not broken by HTML conversion

### Mobile
- [ ] Check display on mobile devices
- [ ] Images scale appropriately
- [ ] Code blocks scrollable

---

## Quick Reference

| Component | Key Guidelines |
|-----------|---------------|
| **Headings** | Short, keywords first, proper hierarchy |
| **Images** | Captions, color-blind safe, compressed, proper rights |
| **Code** | Highlighted, copy-pasteable, vetted, concise |
| **Tables** | Simple, clear headers, preview rendering |
| **Lists** | Parallel structure, max 2 levels deep |

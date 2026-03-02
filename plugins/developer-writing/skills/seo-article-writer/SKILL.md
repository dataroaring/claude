---
name: seo-article-writer
description: This skill should be used when the user asks to "write an SEO comparison article", "create a data-driven SEO post", "write an article with images and data visualizations", "create an SEO article with competitive analysis", "write a long-form SEO article", or needs to produce a complete SEO-optimized article with narrative angle, data visualizations, image generation, and quality verification. Differs from seo-glossary in scope: this skill handles the full production pipeline including competitive gap analysis, HTML data visualizations with Puppeteer capture, image insertion, URL verification, and multi-point quality checks.
version: 1.0.0
---

# SEO Article Writer (Full Production Pipeline)

Create complete, publication-ready SEO articles with a narrative angle, data visualizations, and rigorous quality verification. This skill covers the entire pipeline from competitive analysis to final verification.

## 1. Core Philosophy

**Not feature checklists. Narrative-driven, evidence-based articles.**

Standard SEO comparison articles list features side-by-side without explaining WHY differences exist. This skill produces articles that:

- **Tell a story**: Every article has a narrative arc backed by data (trends, surveys, case studies)
- **Explain causation**: Architectural reasons behind practical differences
- **Include honest criticism**: Acknowledging weaknesses builds trust and differentiates from marketing content
- **Use short case studies to make arguments concrete**: A 3-5 sentence story about a real company (Uber's migration, OpenAI's scaling) is more convincing than any abstract claim
- **Provide actionable decisions**: Specific thresholds and conditions, not vague "it depends"
- **Present balanced landscapes**: When bridging to products, name all credible alternatives with honest trade-offs. Readers trust articles that help them choose, not articles that sell.
- **Bridge to next steps**: Natural transitions to related products or topics

## 2. Competitive Gap Analysis (Pre-Writing)

Before writing, analyze the top 4-5 ranking articles for the target keyword.

### What to Look For

1. **Content gaps**: What stories, data points, or angles are missing?
2. **Depth gaps**: Where are competitors too shallow or too bloated?
3. **Freshness gaps**: What recent developments are missing (new survey data, case studies)?
4. **Unique angles**: What perspective can only your article provide?

### Document the Gaps

```markdown
**Why this article can rank:**
- Gap 1: No competitor uses [specific data source] as narrative hook
- Gap 2: No competitor includes [specific case study]
- Gap 3: No competitor explains [root cause/architecture]
- Gap 4: No competitor bridges to [next logical topic]
- Gap 5: Most are either too shallow (~1.5K words) or bloated (~8-10K words)
```

### Differentiation Strategy

Define 5-7 specific differentiators before writing. Each must be concrete and verifiable against competitor content.

## 3. Article Structure

### YAML Frontmatter

Every article starts with structured metadata:

```yaml
---
title: "Primary Keyword: Descriptive Subtitle (50-60 chars)"
meta_description: "Compelling summary with primary keyword. (under 150 chars)"
url_slug: primary-keyword-descriptive-slug
primary_keyword: "exact target keyword"
secondary_keywords: ["variation 1", "variation 2", "long-tail 1"]
target_length: 4000-5000
---
```

**Constraints:**
- Title: under 60 characters, primary keyword at start
- Meta description: under 150 characters, includes primary keyword
- URL slug: lowercase, hyphens, includes primary keyword

### Section Architecture

Follow this pattern for a comparison/analysis article:

```
1. Introduction: The Narrative Hook (~350 words)
   - Open with data (trends, survey results, adoption numbers)
   - Name real companies using the technology
   - Set up the "why" question the article answers

2. Architectural Foundations (~500 words)
   - Root cause analysis: why the technologies differ
   - Design philosophy behind each approach
   - The cascade effect: how foundations determine practical differences

3. Deep Dive on Key Differentiator (~600 words)
   - The section no competitor has
   - Detailed explanation of the "superpower" or unique angle
   - Concrete examples with tables

4. Honest Criticism (~400 words)
   - Cite respected sources (researchers, well-known critiques)
   - Specific technical problems with evidence
   - Include a brief case study of a company that hit this problem (e.g., Uber's PostgreSQL-to-MySQL migration for write amplification)
   - Why the technology wins anyway despite the weakness

5. Real-World Proof (~500 words)
   - 2-3 case studies with specific numbers
   - Companies that hit the known limitations and scaled through them
   - Source links to engineering blogs

6. Feature Comparison (~800 words)
   - Comparison table with clear categories
   - Per-category analysis (2-3 sentences each)
   - Honest about where each option wins

7. Performance Analysis (~400 words)
   - Specific scenarios, not vague claims
   - Quantified differences with context
   - "The real performance difference comes from X, not Y"

8. Decision Framework (~400 words)
   - "Choose A when:" with specific conditions
   - "Choose B when:" with specific conditions
   - Decision table by use case

9. Bridge Section (~500 words)
   - Natural transition to related topic/product
   - Frame as architecture evolution, not replacement
   - Specific symptoms that trigger the transition
   - Present the full competitive landscape (all credible alternatives)
   - Each option gets a paragraph with strengths AND trade-offs
   - Decision table with one row per option, equal weight

10. Conclusion (~200 words)
    - Data summary
    - Balanced final recommendation
    - Forward-looking statement
```

### Word Count Targets

- Total: 4,000-5,000 words
- Below 4,000: too thin for competitive SEO queries
- Above 5,000: risk of bloat and reader drop-off
- Sweet spot: 4,200-4,800 words

## 4. Data Visualizations

### When to Create Visualizations

Create HTML-based data visualizations for:
- Trend data (line charts showing growth/decline)
- Survey results (bar charts with percentages)
- Architecture diagrams (system component relationships)
- Comparison tables (feature matrices)
- Decision flowcharts (choose-your-path diagrams)
- Ecosystem maps (hub-and-spoke relationships)

### HTML Visualization Standards

Each visualization is a standalone HTML file:

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    width: 700px;
    height: 400px;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    overflow: hidden;
    /* Design fits exactly within 700x400 viewport */
  }
</style>
</head>
<body>
  <!-- Pure CSS/HTML visualization, no JavaScript libraries -->
  <!-- All content must fit within 700x400px without scrolling -->
</body>
</html>
```

**Design Rules:**
- Viewport: exactly 700x400px
- No external dependencies (no CDN links, no JavaScript libraries)
- Pure CSS for charts, diagrams, and layouts
- Professional color palette (blues, grays, accent colors)
- All text must be legible at the rendered size
- Test that nothing is clipped at the bottom

### Screenshot Capture with Puppeteer

Create a capture script alongside the HTML files:

```javascript
const puppeteer = require('puppeteer');
const path = require('path');
const fs = require('fs');

const files = [
  'article-prefix-01-description',
  'article-prefix-02-description',
  // ... list all HTML files without extension
];

(async () => {
  const browser = await puppeteer.launch({ headless: 'new' });
  const page = await browser.newPage();
  await page.setViewport({ width: 700, height: 400, deviceScaleFactor: 2 });

  for (const file of files) {
    const htmlPath = path.join(__dirname, `${file}.html`);
    const outPath = path.join(__dirname, `${file}.png`);
    if (!fs.existsSync(htmlPath)) continue;

    await page.goto(`file://${htmlPath}`, { waitUntil: 'networkidle0' });
    await page.screenshot({
      path: outPath,
      clip: { x: 0, y: 0, width: 700, height: 400 }
    });
    console.log(`Captured: ${file}.png`);
  }

  await browser.close();
  console.log('All screenshots captured.');
})();
```

**Capture specs:**
- 2x device scale factor (retina quality: 1400x800 actual pixels)
- Clip to exactly 700x400 to prevent bottom overflow
- Use `networkidle0` to ensure all CSS is rendered
- Install puppeteer locally: `npm install puppeteer`

### Image Naming Convention

```
{article-prefix}-{number}-{description}.html
{article-prefix}-{number}-{description}.png
```

Example: `pg-vs-mysql-01-db-engines-trend.html` / `.png`

### Fixing Clipped Images

If content is clipped at the bottom of the 700x400 viewport:
1. Reduce padding and margins (e.g., 14px to 8px)
2. Reduce font sizes by 0.5-1px
3. Tighten grid layouts (fewer rows, more columns)
4. Reduce border widths
5. Re-capture and verify

## 5. Image Insertion

### Placement Rules

- Place images at the top of their corresponding section, after the H2 heading
- Every image gets descriptive ALT text (under 125 characters)
- ALT text includes relevant keywords naturally
- Use relative paths from the article's directory

### Markdown Format

```markdown
## Section Title

![Descriptive ALT text with keywords](images/article-prefix-01-description.png)

Section content begins here...
```

### Recommended Image Count

- 4,000-5,000 word article: 6-10 images
- At least one image per major section
- Data-heavy sections may have 2 images

## 6. Writing Quality Rules

### From writing-skills.md

Apply these rules strictly:

1. **Em dashes**: Maximum 1-2 per entire article. Replace with periods, commas, or colons.
2. **Evidence-based claims**: Every arguable statement backed by specific numbers or sources
3. **Actionable writing**: Every "it depends" followed by specific conditions
4. **Active voice**: Use the zombie test ("by zombies" after the verb)
5. **Single-idea paragraphs**: One idea per paragraph
6. **Conversational tone**: "I/we" for author, "you" for reader
7. **No throat-clearing**: Cut "It is important to note that..." and similar

### Data Freshness

Data claims go stale fast. Verify and keep current:

1. **Awards and rankings**: Check the latest year. "Won DBMS of the Year in 2023" becomes wrong once 2024 results are out. Always cite the full history with a ref URL.
2. **Survey data**: Stack Overflow, JetBrains, and similar surveys publish annually. Cite the most recent and link directly.
3. **Company scale numbers**: "800 million users" was accurate when OpenAI published it. Note the source date if older than 12 months.
4. **Market share claims**: DB-Engines rankings shift. Link to the live ranking page, not a snapshot.

### Balanced Product Mentions

When an article bridges to a product category (e.g., "analytics databases"), present all credible alternatives:

1. **Name every serious option** in the space (e.g., Redshift, BigQuery, ClickHouse, Tinybird, Apache Doris)
2. **Give each option a paragraph** with both strengths and trade-offs
3. **Decision tables: one row per option**, equal weight. Do not give your preferred product more rows than competitors.
4. **Be specific about trade-offs**: "vendor lock-in" is vague. "BigQuery's cold start can take seconds, too slow for user-facing dashboards" is useful.
5. **Readers trust balanced analysis.** An article that honestly compares five options converts better than one that pretends only one exists.

### Short Case Studies

Brief real-world stories (3-5 sentences) make technical arguments concrete:

- **Place them where they prove a point**, not as standalone filler
- **Include specifics**: company name, scale, what broke, what they did
- **Link to the engineering blog** as source
- Example: Uber's PostgreSQL-to-MySQL migration (write amplification on wide tables with 12+ indexes, replication bandwidth blowup, built Schemaless on InnoDB)
- Example: OpenAI scaling PostgreSQL (800M users, single primary + 50 replicas, offloaded writes to Cosmos DB)

### SEO-Specific Rules

1. **Primary keyword** in: title, H1, meta description, first 100 words, 2-3 H2 headings
2. **Heading hierarchy**: H1 > H2 > H3 (never skip levels)
3. **Descriptive hyperlinks**: Never "click here" or raw URLs
4. **Internal context**: Brief explanation before introducing acronyms or jargon

### Inline Citations

Link to sources inline rather than in a separate references section:

```markdown
OpenAI runs ChatGPT on PostgreSQL, serving
[800 million users on a single primary instance](https://openai.com/index/scaling-postgresql/).
```

## 7. Quality Verification Checklist

Run these checks before considering the article complete:

### Word Count
- [ ] Total word count: 4,000-5,000

### SEO Metadata
- [ ] Title under 60 characters
- [ ] Meta description under 150 characters
- [ ] Primary keyword in title, H1, meta description, first 100 words
- [ ] URL slug includes primary keyword

### Structure
- [ ] H1 > H2 > H3 hierarchy (no skipped levels)
- [ ] Each H2 section has a transition sentence before H3s
- [ ] Each H3 has an introduction sentence before lists

### Writing Quality
- [ ] Em dash count: 0-2 for the entire article
- [ ] No "it depends" without specific follow-up conditions
- [ ] Specific numbers replace vague words ("fast", "many", "large")
- [ ] Active voice throughout (zombie test passes)

### Images
- [ ] All images render completely (no clipping)
- [ ] ALT text on every image (under 125 characters)
- [ ] Image paths are correct relative to article location

### URLs
- [ ] All reference URLs verified (fetch each and confirm expected content)
- [ ] Fix or remove any broken links
- [ ] No raw URLs in body text (all hyperlinked with descriptive text)

### Data Freshness
- [ ] All award/ranking claims cite the latest year with ref URL
- [ ] Survey data is from the most recent available year
- [ ] Company scale numbers sourced and dated

### Balanced Landscape
- [ ] Bridge section names all credible alternatives, not just one
- [ ] Each alternative gets equal treatment (one paragraph, one table row)
- [ ] Trade-offs stated for every option, including the preferred one

### Content Differentiation
- [ ] At least 3 elements no competitor article includes
- [ ] Real-world case studies with specific numbers (3-5 sentence stories, not just name-drops)
- [ ] Honest criticism section with case study showing the problem in practice
- [ ] Actionable decision framework with specific thresholds

## 8. Directory Structure

Each article lives in its own directory:

```
article-slug/
  article-slug.md          # The article
  images/
    prefix-01-name.html    # HTML source for visualization
    prefix-01-name.png     # Captured screenshot
    prefix-02-name.html
    prefix-02-name.png
    capture-screenshots.js  # Puppeteer capture script
```

## 9. Full Workflow

### Phase 1: Research & Planning
1. Identify target keyword and search intent
2. Analyze top 4-5 competitor articles
3. Document competitive gaps and differentiation strategy
4. Outline article structure with section word counts
5. Identify data points, case studies, and sources

### Phase 2: Writing
1. Write YAML frontmatter
2. Draft introduction with narrative hook and data
3. Write body sections following the architecture template
4. Include inline citations with hyperlinks
5. Write decision framework with specific thresholds
6. Write bridge section and conclusion

### Phase 3: Data Visualizations
1. Create HTML files for each visualization (700x400px)
2. Write Puppeteer capture script
3. Capture screenshots at 2x retina
4. Verify all images render completely (no clipping)
5. Fix any clipped images by tightening CSS

### Phase 4: Assembly
1. Insert images into article at appropriate section locations
2. Add ALT text with keywords to every image
3. Verify image paths work

### Phase 5: Verification
1. Check word count (4,000-5,000)
2. Verify SEO metadata constraints
3. Count em dashes (max 2)
4. Verify heading hierarchy
5. Fetch and verify all reference URLs
6. Confirm competitive differentiation elements present
7. Read aloud for flow

## 10. Reference Materials

For a complete example demonstrating this workflow:
- **`references/postgresql-vs-mysql-workflow.md`** — Full production example with competitive analysis, article structure, 8 data visualizations, and quality verification

For a published example of the SEO glossary style (sibling skill):
- **Published:** [OLTP vs OLAP: A Complete Guide to Database Architecture](https://www.velodb.io/glossary/olap-vs-oltp)

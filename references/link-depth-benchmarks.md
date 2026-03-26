# Link Depth Benchmarks — Internal Link Mapper

## What is Crawl Depth?

Crawl depth = the minimum number of clicks from the homepage to reach a given page via internal links.

- Homepage = depth 0
- Pages linked directly from homepage = depth 1
- Pages linked from depth-1 pages = depth 2
- And so on

Googlebot allocates a crawl budget per site. Deep pages consume more budget to reach and are crawled less frequently.

---

## Ideal Depth by Site Size

| Site Size | Max Recommended Depth for Important Content |
|---|---|
| Under 100 pages | Depth 2 max for all content |
| 100–500 pages | Depth 3 max for core content; depth 4 tolerable for supporting content |
| 500–2.000 pages | Depth 3 for pillar pages; depth 4–5 for spokes; flag anything deeper |
| 2.000–10.000 pages | Depth 4 for important content; implement hub pages to reduce depth for clusters |
| 10.000+ pages | Requires deliberate hub architecture; paginated sections; depth 5 max for anything indexable |

**Rule of thumb:** If a page is more than 4 clicks from the homepage, it's effectively invisible to Googlebot on low-crawl-budget sites.

---

## Depth Reduction Strategies

### Strategy 1: Pillar Hub Linking
Every cluster pillar page links to all its spokes. Spokes at depth 3 become reachable at depth 2 if the pillar is at depth 1.

Before:
```
Homepage (0) → Category (1) → Pillar (2) → Spoke (3) → Sub-spoke (4)
```

After adding pillar → sub-spoke link:
```
Homepage (0) → Category (1) → Pillar (2) → Sub-spoke (3)
```

### Strategy 2: Related Posts Section
A dedicated "Artigos relacionados" section at the bottom of pillar pages creates shortcuts. Every spoke that appears there gets a depth equal to the pillar's depth + 1.

### Strategy 3: Breadcrumb Navigation
Breadcrumbs create upward links in the depth tree. They don't reduce depth by themselves but provide Googlebot with multiple paths to discover pages.

### Strategy 4: Homepage or Navigation Links
Adding a page to the main navigation or homepage is the most powerful depth reduction (instant depth 1 or 2). Reserve for pillar pages and high-value content only.

### Strategy 5: Sitemap (fallback, not substitute)
An XML sitemap tells Google about pages that exist but is not a substitute for deep internal linking. Googlebot still needs internal links to understand relationships between pages.

---

## PageRank Flow Theory (Simplified)

PageRank is distributed through internal links. Each page passes a fraction of its PageRank to every page it links to.

Key implications:

**1. More outlinks = less PageRank per link**
A page with 2 outlinks passes ~50% of its PageRank to each. A page with 20 outlinks passes ~5%. Use high-outlink pages selectively.

**2. Orphan pages receive no PageRank**
A page with 0 inlinks has no internal PageRank flow. It's only as strong as what Google assigns from external links (if any). In practice: near zero.

**3. Silo pages (0 outlinks) keep PageRank but don't share it**
The page accumulates PageRank but acts as a dead end. Add outlinks to let flow continue through the graph.

**4. Circular linking boosts all nodes**
Pillar ↔ Spoke linking in both directions creates a reinforcing loop. The pillar passes PageRank to the spoke; the spoke returns some to the pillar. Both become stronger over time.

**5. The homepage is the highest PageRank source**
Every page is at most N hops from the homepage. Closer = more PageRank received. Use homepage links sparingly and only for your most strategic pages.

---

## Depth Audit Thresholds

When running a full site audit, flag pages by priority:

| Depth | Status | Action |
|---|---|---|
| 0–2 | Good | No action needed |
| 3 | Acceptable | Monitor; ensure content quality justifies |
| 4 | Warning | Add shortcuts from higher-authority pages |
| 5+ | Critical | Must reduce; add to pillar pages or navigation hubs |
| Unreachable (orphan) | Emergency | Add at least 2 inlinks immediately |

---

## Crawl Depth Improvement Estimation

When recommending links, estimate depth improvement as follows:

- If a page is at depth 4 and the recommended source is at depth 2 → estimated improvement: -2 hops (page becomes reachable at depth 3)
- If multiple source pages link to a target → use the minimum source depth + 1 as the new effective depth
- Report as: "Redução estimada de crawl depth: de 4 para 3 hops a partir da homepage"

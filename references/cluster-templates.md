# Cluster Templates — Internal Link Mapper

## What is a Topical Cluster?

A topical cluster is a group of pages that covers a topic comprehensively through a hierarchical link structure:

- **Pillar page**: Broad, authoritative overview of the topic. Links to all spokes.
- **Spoke pages**: Deep-dive posts on specific subtopics. Each links back to the pillar, and may cross-link to sibling spokes where relevant.
- **Sub-spokes** (optional): Even more specific posts linked from spokes, not necessarily from the pillar.

The cluster structure tells Google that the site has depth and authority on a given topic.

---

## Universal Cluster Link Rules

Regardless of site type, always apply these:

1. Pillar links to every spoke (minimum: in-text or in a "Tópicos relacionados" section)
2. Every spoke links back to the pillar (minimum: 1 in-text link with a broad keyword anchor)
3. Sibling spokes link to each other when their subtopics naturally intersect
4. No spoke should have 0 links pointing to it from within the cluster
5. The pillar should not be the deepest-linked page in its own cluster — it should be the most-linked

---

## Template 1: Blog / Content Site

**Use case:** A blog focused on a specific niche (SEO, nomadismo digital, finanças, etc.)

**Structure:**
```
Pillar: /guia-completo-de-[tema]
  ├── Spoke 1: /[subtopico-1]
  ├── Spoke 2: /[subtopico-2]
  ├── Spoke 3: /[subtopico-3]
  ├── Spoke 4: /[subtopico-4]
  └── Spoke 5: /[subtopico-5]
      └── Sub-spoke: /[subtopico-5-aprofundado]
```

**Recommended pillar content:**
- Covers the full topic at a high level
- Includes a table of contents linking to each section
- Each section has a CTA linking to the corresponding spoke
- Word count: 3.000–6.000 words (comprehensive but skimmable)

**Recommended spoke content:**
- Covers ONE specific subtopic in depth
- Links back to pillar in the first or second paragraph
- Word count: 1.500–3.000 words
- Cross-links to 2–3 sibling spokes where relevant

**Example (SEO blog):**
```
Pillar: /guia-seo-para-iniciantes
  ├── /pesquisa-de-palavras-chave
  ├── /seo-on-page
  ├── /link-building-para-iniciantes
  ├── /seo-tecnico-basico
  └── /como-medir-resultados-seo
```

---

## Template 2: E-commerce

**Use case:** Product catalog with category pages, product pages, and supporting content.

**Structure:**
```
Category page (pillar): /categoria/[produto-tipo]
  ├── Subcategory (spoke): /categoria/[produto-tipo]/[subcategoria]
  │     └── Product pages: /produto/[nome-produto]
  └── Supporting content (spoke): /blog/[guia-de-compra-do-produto-tipo]
```

**Key differences from blog clusters:**
- Product pages don't need to link back to the category — but should link to related products and to supporting content
- Supporting content (buying guides, comparisons) should link to category and top product pages
- Avoid creating dead ends on product pages — add a "Produtos relacionados" section with internal links

**Link priorities for e-commerce:**
1. Category → Subcategory (already handled by nav, but verify)
2. Blog guide → Category page (high impact — passes authority from content to commerce)
3. Product → Related products (keeps users in funnel + distributes PageRank)
4. Category → Best-selling products (reduces depth, boosts product PageRank)

---

## Template 3: SaaS / Product Site

**Use case:** A SaaS company with feature pages, use case pages, and a blog.

**Structure:**
```
Homepage
  ├── Feature pages (pillar for each feature)
  │     ├── Use case pages (spokes)
  │     └── Integration pages (spokes)
  └── Blog
        ├── Problem-aware posts → link to feature pages
        ├── Tutorial posts → link to feature pages + docs
        └── Comparison posts → link to feature pages + homepage
```

**Key link rules for SaaS:**
- Feature pages should link to at least 3 relevant blog posts (reverse cluster: feature is the hub, blog posts are the spokes)
- Tutorial posts should link to the feature page they explain AND to relevant integration pages
- Comparison posts (ex: "X vs Y") should link to the feature page being compared and to a case study or social proof page
- Pricing page: don't orphan it — at least 5 internal links from high-traffic pages

**High-ROI links for SaaS:**
1. High-traffic blog post → Feature page (converts traffic into product awareness)
2. Tutorial post → Signup/demo page (bottom-funnel link from educational content)
3. Feature page → Related use case page (deepens product understanding)

---

## Template 4: Local SEO / Multi-location

**Use case:** A business with multiple locations or a local service site.

**Structure:**
```
State/region page (pillar): /[estado]
  ├── City pages (spokes): /[estado]/[cidade]
  │     └── Neighborhood pages (sub-spokes): /[estado]/[cidade]/[bairro]
  └── Service pages (spokes): /servico/[tipo-de-servico]
        └── City-specific service pages: /servico/[tipo]/[cidade]
```

**Key link rules for local SEO:**
- State page links to all city pages
- City pages link back to state page AND to all service pages for that city
- City-specific service pages link back to the generic service page AND to the city page
- Never create city or service pages that aren't linked from at least 2 other pages

**Anchor text for local clusters:**
- City page anchors: include the city name ("SEO em São Paulo")
- Service page anchors: include the service keyword ("consultoria de SEO")
- City-specific service anchors: combine both ("consultoria de SEO em São Paulo")

---

## Publication Order Recommendations

### Scenario A: Building cluster from scratch

Recommended order:
1. Publish all spoke pages first (even if short — they can be expanded later)
2. Publish the pillar page with links to all spokes already live
3. Add cross-links between sibling spokes within 1 week of publishing

Why: The pillar links to spokes that already exist → Google can crawl the full cluster on the first crawl of the pillar.

### Scenario B: Adding a new cluster to existing site

1. Identify existing pages that partially cover the new cluster topic
2. Add links from those pages to the new cluster pillar immediately on publish
3. Publish the pillar with links to existing spoke pages
4. Publish new spoke pages one by one, updating the pillar each time

### Scenario C: Expanding an existing cluster

1. Identify which subtopic is missing from the current cluster
2. Write the new spoke targeting that subtopic
3. Immediately add a link from the pillar to the new spoke
4. Find 2–3 sibling spokes that naturally mention the new spoke's topic → add cross-links

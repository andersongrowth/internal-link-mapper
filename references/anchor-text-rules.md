# Anchor Text Rules — Internal Link Mapper

## The Core Principle

Anchor text is a relevance signal, not just a label. Google uses it to understand what the destination page is about. For internal links, this is controllable — use it strategically.

---

## Forbidden Anchors

Never use these as anchor text for internal links:

| Forbidden | Why |
|---|---|
| "clique aqui" | Zero topical signal |
| "leia mais" | Zero topical signal |
| "saiba mais" | Zero topical signal |
| "este artigo" | Zero topical signal |
| "aqui" (standalone) | Zero topical signal |
| "acesse" | Zero topical signal |
| The full URL as anchor | Looks unnatural, no keyword signal |
| The page title verbatim (always) | OK occasionally, but avoid as the default pattern |

---

## Anchor Types and When to Use Each

### 1. Exact Match
The anchor is the target page's primary keyword, exactly.

- Example: Target page = "como fazer link building" → Anchor = "link building"
- Use: Sparingly. 1–2 times max across the whole site for a given target.
- Risk: Over-use triggers over-optimization signals.

### 2. Partial Match
The anchor contains the primary keyword plus other words.

- Example: "estratégias de link building interno"
- Use: Most common type. Safe to use multiple times for the same target with variation.

### 3. Semantic Variation
The anchor covers the same topic with different vocabulary.

- Example: Target is about "link building" → Anchor = "construção de autoridade", "aquisição de links", "estrutura de links"
- Use: Ideal when you need to link to the same page from multiple sources.

### 4. Branded
Includes the site or author name.

- Use: Only for homepage or About page links. Not for content pages.

### 5. Topical Context Anchor
A phrase from the surrounding paragraph that naturally describes the destination.

- Example: In a paragraph about "fluxo de PageRank entre páginas", anchor a link to a PageRank guide with "fluxo de PageRank"
- Use: Best practice. Leverages `fullLeftContext` / `fullRightContext` signal.

---

## Variation Formula

For any target page that receives 3+ internal links, use this variation pattern:

```
Link 1 (from pillar): [primary keyword] — exact or close partial match
Link 2 (from related spoke): [primary keyword + modifier] — partial match
Link 3 (from another spoke): [semantic variation] — different vocabulary, same topic
Link 4+ : [topical context anchor] — phrase from the natural paragraph
```

Example for a target page about "auditoria de SEO técnico":
- Link 1: "auditoria de SEO técnico"
- Link 2: "como fazer uma auditoria técnica de SEO"
- Link 3: "análise técnica do site"
- Link 4: "problemas de indexação e rastreamento"

---

## Over-Optimization Detection

Flag a target page as over-optimized when:
- Same exact anchor used 3+ times across different source pages for the same destination
- All anchors for a page are keyword-heavy with no variation
- Anchor text is longer than 6–7 words (suspiciously over-crafted)

**What to do:** Recommend replacing 1–2 of the exact-match anchors with semantic variations or topical context anchors.

---

## Under-Optimization Detection

Flag a target page as under-optimized when:
- All anchors pointing to it are generic ("leia mais", "clique aqui", "aqui")
- Anchors are unrelated to the page's primary keyword
- No anchor contains any word from the page's target keyword set

**What to do:** Replace generic anchors with partial match or topical context anchors on the 2–3 highest-authority source pages first.

---

## Anchor Length Guidelines

| Anchor Length | Assessment |
|---|---|
| 1–2 words | Good for exact match. Risky if overused. |
| 3–5 words | Ideal range. Natural and keyword-rich. |
| 6–8 words | Acceptable for partial match or topical context. |
| 9+ words | Avoid. Looks unnatural. May be ignored or discounted. |

---

## Language-Specific Notes (PT-BR)

- Prepositions and articles in Portuguese anchors are fine: "estratégias de link building" is better than just "link building" because it matches natural search queries
- Avoid anchors that start with verbs in imperative form ("Aprenda sobre X", "Descubra Y") — these read as CTAs, not topical signals
- Accented characters are fine and should be included: "análise técnica" not "analise tecnica"

🔗 Internal Link Mapper
A Claude skill that builds and optimizes internal link structures for SEO.
Give it a list of URLs and it tells you exactly which pages should link to which, what anchor text to use, and where to insert the link in the content.

What it does

New post launch — finds the best existing pages to link to your new post
Full site audit — detects orphan pages, dead ends, and underlinked content
Cluster architecture — designs pillar + spoke link maps for topical authority
Anchor text strategy — generates varied, keyword-rich anchors for every link
Content-level instructions — tells you exactly which paragraph to edit


Example output
🔴 HIGH PRIORITY

1. /blog/seo-tecnico → /blog/core-web-vitals
   Anchor: "otimização de Core Web Vitals"
   Where: 2º parágrafo, após mencionar "velocidade do site"
   Why: /blog/core-web-vitals tem 0 links internos (orphan risk)

2. /blog/seo → /blog/link-building
   Anchor: "estratégias de link building"
   Where: Seção "O que é SEO Off-Page"
   Why: Pillar não está linkando para este spoke — cluster incompleto

Installation

Download SKILL.md
In Claude.ai, go to Settings → Claude's Skills
Upload the file

The skill will be available in all your conversations.

Files
FileDescriptionSKILL.mdThe skill instructions for Claudereferences/anchor-text-rules.mdAnchor text best practices and variation formulasreferences/cluster-templates.mdPillar + spoke templates for blog, e-commerce and SaaSreferences/link-depth-benchmarks.mdCrawl depth benchmarks and PageRank flow theory

Usage examples
"Acabei de publicar um post, quais páginas devem linkar para ele?"
→ Paste your new post URL + a list of your site's URLs
"Me dê um relatório de links internos do meu site"
→ Paste your full URL list (export from Screaming Frog or GSC Sitemap)
"Quero criar um cluster sobre SEO técnico"
→ Describe the topic and how many posts you have or plan to create

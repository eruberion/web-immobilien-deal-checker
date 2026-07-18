# Graph Report - .  (2026-07-18)

## Corpus Check
- Corpus is ~10,305 words - fits in a single context window. You may not need a graph.

## Summary
- 53 nodes · 79 edges · 9 communities (7 shown, 2 thin omitted)
- Extraction: 84% EXTRACTED · 14% INFERRED · 3% AMBIGUOUS · INFERRED: 11 edges (avg confidence: 0.93)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Client-Only Calculations
- Governance and Skills
- Release and Deployment
- Trust-Centered Design
- Premium Roadmap
- Product Release Scope
- Advice Boundary
- Pre-Commit Hook
- Pre-Push Hook

## God Nodes (most connected - your core abstractions)
1. `Immobilien Deal Checker Agent Governance` - 11 edges
2. `Immobilien Deal Checker Application` - 11 edges
3. `Deal Calculation Engine` - 7 edges
4. `Release History` - 6 edges
5. `Immobilien Deal Checker Overview` - 6 edges
6. `Immobilien Deal Expert` - 6 edges
7. `Immobilien Deal Checker Claude Governance` - 5 edges
8. `Product Visual Direction` - 5 edges
9. `Restore QA Report 2026-07-18` - 5 edges
10. `Restore Test Matrix` - 5 edges

## Surprising Connections (you probably didn't know these)
- `Immobilien Deal Checker Claude Governance` --semantically_similar_to--> `Immobilien Deal Checker Agent Governance`  [INFERRED] [semantically similar]
  CLAUDE.md → AGENTS.md
- `Trust-Critical Clarity` --semantically_similar_to--> `Analysis Tool Over Marketing Skin`  [INFERRED] [semantically similar]
  skills/openclaw-web-premium-ui/SKILL.md → DESIGN.md
- `Clarity Over Animation` --semantically_similar_to--> `Trust-Critical Clarity`  [INFERRED] [semantically similar]
  DESIGN.md → skills/openclaw-web-premium-ui/SKILL.md
- `Accessible Visual Restraint` --semantically_similar_to--> `Clarity Over Animation`  [INFERRED] [semantically similar]
  skills/web-apple-design/SKILL.md → DESIGN.md
- `Analysis Tool Advice Boundary` --semantically_similar_to--> `No-Advice and No-Guarantee Boundary`  [INFERRED] [semantically similar]
  PRODUCT.md → skills/immobilien-deal-expert/SKILL.md

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Core Product Identity** — readme_project_overview, product_product_brief, immobilien_deal_checker_application [INFERRED 0.95]
- **Trust-Centered Design Guidance** — design_visual_direction, skills_openclaw_web_premium_ui_skill_premium_ui, skills_web_apple_design_skill_apple_web_design [INFERRED 0.85]
- **Financial Model Governance** — agents_project_governance, skills_immobilien_deal_expert_skill_domain_rules, immobilien_deal_checker_calc [INFERRED 0.95]

## Communities (9 total, 2 thin omitted)

### Community 0 - "Client-Only Calculations"
Cohesion: 0.19
Nodes (13): Client-Only Architecture, Single-File Principle, Restore Test Matrix, Static Application Recovery Plan, Single-File Recovery Mechanism, Immobilien Deal Checker Application, Deal Calculation Engine, Offenbach Rent Estimator (+5 more)

### Community 1 - "Governance and Skills"
Cohesion: 0.24
Nodes (12): Immobilien Deal Checker Agent Governance, Version Mirror Contract, Immobilien Deal Checker Claude Governance, Immobilien Deal Expert OpenAI Interface, Immobilien Deal Expert, Real Estate Model Rules, Official Source Workflow, Coherence and Usability Over Premium Styling (+4 more)

### Community 2 - "Release and Deployment"
Cohesion: 0.25
Nodes (9): Keep a Changelog, Release History, Semantic Versioning, Deployment Plan, Static Hosting Options, Manual Browser Smoke Gap, Restore QA Report 2026-07-18, Restore Tree Identity (+1 more)

### Community 3 - "Trust-Centered Design"
Cohesion: 0.50
Nodes (5): Analysis Tool Over Marketing Skin, Clarity Over Animation, Product Visual Direction, Trust-Critical Clarity, Accessible Visual Restraint

### Community 4 - "Premium Roadmap"
Cohesion: 0.50
Nodes (4): Freemium Subscription Model, Premium Monetization Roadmap, Save Compare Export Premium Core, Search-Phase Subscription Rationale

### Community 5 - "Product Release Scope"
Cohesion: 0.67
Nodes (3): Version 0.11.1 Restore Release, Immobilien Deal Checker Product Brief, Product Success Criteria

### Community 6 - "Advice Boundary"
Cohesion: 0.67
Nodes (3): Deal Scoring Model, Analysis Tool Advice Boundary, No-Advice and No-Guarantee Boundary

## Ambiguous Edges - Review These
- `Deployment Plan` → `Static Hosting Options`  [AMBIGUOUS]
  DEPLOYMENT.md · relation: implements
- `Immobilien Deal Checker Application` → `React Vite TypeScript Development Rules`  [AMBIGUOUS]
  skills/react-vite-typescript/SKILL.md · relation: conceptually_related_to

## Knowledge Gaps
- **8 isolated node(s):** `Keep a Changelog`, `Static Hosting Options`, `Evaluation Mode Configuration`, `Rent Increase Presets`, `German Property Transfer Tax Map` (+3 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **2 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **What is the exact relationship between `Deployment Plan` and `Static Hosting Options`?**
  _Edge tagged AMBIGUOUS (relation: implements) - confidence is low._
- **What is the exact relationship between `Immobilien Deal Checker Application` and `React Vite TypeScript Development Rules`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._
- **Why does `Immobilien Deal Checker Application` connect `Client-Only Calculations` to `Governance and Skills`, `Release and Deployment`, `Trust-Centered Design`?**
  _High betweenness centrality (0.315) - this node is a cross-community bridge._
- **Why does `Immobilien Deal Checker Agent Governance` connect `Governance and Skills` to `Client-Only Calculations`, `Release and Deployment`?**
  _High betweenness centrality (0.262) - this node is a cross-community bridge._
- **Why does `Deal Calculation Engine` connect `Client-Only Calculations` to `Governance and Skills`, `Advice Boundary`?**
  _High betweenness centrality (0.146) - this node is a cross-community bridge._
- **What connects `Keep a Changelog`, `Static Hosting Options`, `Evaluation Mode Configuration` to the rest of the system?**
  _8 weakly-connected nodes found - possible documentation gaps or missing edges._
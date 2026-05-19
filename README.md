<h1 align="center"> OpenCode Skills</h1>

<p align="center">
  A curated collection of practical skills for OpenCode.
</p>

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome" /></a>
  <img src="https://img.shields.io/badge/skills-54-blue" alt="Skill count" />
  <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs welcome" />
  <img src="https://img.shields.io/badge/license-MIT-green" alt="MIT" />
</p>

OpenCode skills are reusable instruction bundles that teach an AI coding agent how to do a repeatable task: design brand systems, synthesize research, manage inboxes, plan campaigns, qualify leads, write support replies, automate SaaS tools, build frontends, or create media workflows.

Each skill lives in its own folder with a `SKILL.md` file containing metadata and execution guidance. OpenCode reads the metadata up front, then loads the full instructions only when the task matches the skill description.

---

## Quickstart: Connect OpenCode to 1000+ Apps

The [composio-cli](skills/composio-cli/SKILL.md) skill lets OpenCode perform real actions: send emails, create issues, post to Slack, update Notion, triage Linear, and automate workflows across 1000+ apps through the Composio CLI.

### 1. Install the Skill

```bash
git clone https://github.com/composio-community/opencode-skills.git
cd opencode-skills
mkdir -p .opencode/skills
cp -r skills/composio-cli .opencode/skills/
```

For global install, copy it to `~/.config/opencode/skills/` instead:

```bash
mkdir -p ~/.config/opencode/skills
cp -r skills/composio-cli ~/.config/opencode/skills/
```

### 2. Install and Log In to Composio

```bash
curl -fsSL https://composio.dev/install | bash
composio login
composio whoami
```

Get a free account at [dashboard.composio.dev](https://dashboard.composio.dev/) if you do not already have one.

### 3. Restart and Try It

Restart OpenCode so it reloads skill metadata, then ask:

```text
Use composio-cli to create a GitHub issue from this failing test output.
```

The skill will guide OpenCode through the safe Composio loop: discover the tool with `composio search`, inspect inputs with `--get-schema`, connect the account with `composio link`, preview writes with `--dry-run`, then execute.

**[See all supported apps →](https://composio.dev/toolkits)**

For other workflows, copy any folder from `skills/` into the same OpenCode skills directory.

---

## Contents

- [What Are OpenCode Skills?](#what-are-opencode-skills)
- [Skills](#skills)
  - [Design & Product](#design--product)
  - [Marketing & Content](#marketing--content)
  - [Sales, Support & Collaboration](#sales-support--collaboration)
  - [Business Operations](#business-operations)
  - [Development & Code Tools](#development--code-tools)
  - [Planning & Agent Workflows](#planning--agent-workflows)
  - [Cloud, Apps & Systems](#cloud-apps--systems)
  - [Creative & Media](#creative--media)
  - [Skill Authoring & Maintenance](#skill-authoring--maintenance)
- [Using Skills](#using-skills)
- [Creating Skills](#creating-skills)
- [Related Awesome Lists](#related-awesome-lists)
- [Contributing](#contributing)
- [License](#license)

## What Are OpenCode Skills?

Skills are modular workflow packages for AI agents. They are not MCP servers and they are not tools. MCP provides access to external systems, tools perform individual actions, and skills define the procedure, guardrails, quality bar, and decision logic the agent should follow.

OpenCode discovers skills from skill directories and loads them progressively:

1. Metadata is always available through `name` and `description` frontmatter.
2. Full instructions are loaded only when a skill is relevant.
3. Optional scripts, references, or assets are used only when the skill asks for them.

The `description` is the trigger. Good descriptions say what the skill does and when the agent should use it.

## Skills

### Design & Product

- [brand-identity-system](skills/brand-identity-system/SKILL.md) - Create practical brand systems with positioning, voice, color, typography, visual rules, and usage examples.
- [customer-journey-mapping](skills/customer-journey-mapping/SKILL.md) - Map lifecycle stages, touchpoints, friction, emotions, and opportunities across acquisition, onboarding, retention, and support.
- [design-critique-review](skills/design-critique-review/SKILL.md) - Critique UI, hierarchy, spacing, accessibility, interaction states, and visual polish with concrete fixes.
- [landing-page-copy-design](skills/landing-page-copy-design/SKILL.md) - Build conversion-focused landing pages with positioning, structure, proof, objections, and CTAs.
- [product-requirements-writing](skills/product-requirements-writing/SKILL.md) - Turn product ideas into PRDs, feature specs, user stories, acceptance criteria, and launch scope.
- [user-research-synthesis](skills/user-research-synthesis/SKILL.md) - Synthesize interviews, surveys, notes, and feedback into insights, jobs-to-be-done, opportunities, and recommendations.

### Marketing & Content

- [ad-creative-briefs](skills/ad-creative-briefs/SKILL.md) - Create paid creative briefs with audience, offer, hook, concept, visual direction, copy variants, and testing plan.
- [claude-seo-workflows](skills/claude-seo-workflows/SKILL.md) - Run SEO research, content optimization, keyword strategy, technical SEO analysis, and search-focused content generation.
- [competitive-positioning-research](skills/competitive-positioning-research/SKILL.md) - Compare competitors, positioning, pricing, proof, feature gaps, and defensible differentiation.
- [content-calendar-planning](skills/content-calendar-planning/SKILL.md) - Plan editorial calendars across blog, social, email, video, and community channels with cadence and owners.
- [marketing-skills-workflows](skills/marketing-skills-workflows/SKILL.md) - Perform marketing strategy, SEO audits, audience positioning, funnel analysis, and growth execution.
- [newsletter-production](skills/newsletter-production/SKILL.md) - Produce newsletters with issue themes, curated links, editorial voice, subject lines, sections, and CTAs.
- [seo-content-refresh](skills/seo-content-refresh/SKILL.md) - Refresh existing content for search intent, AI search, clarity, internal links, and conversion.
- [social-media-campaign-builder](skills/social-media-campaign-builder/SKILL.md) - Create platform-native social campaigns with hooks, post sequences, creative briefs, CTAs, and engagement plans.

### Sales, Support & Collaboration

- [calendar-scheduling-assistant](skills/calendar-scheduling-assistant/SKILL.md) - Coordinate availability, agendas, reminders, and calendar updates through Composio CLI when app access is needed.
- [community-management-replies](skills/community-management-replies/SKILL.md) - Draft community replies, moderation responses, announcements, and escalations for Slack, Discord, forums, and social channels.
- [crm-pipeline-hygiene](skills/crm-pipeline-hygiene/SKILL.md) - Clean CRM pipelines, stale deals, missing fields, follow-ups, and next actions through Composio CLI.
- [customer-feedback-analysis](skills/customer-feedback-analysis/SKILL.md) - Analyze reviews, surveys, tickets, calls, and community posts into themes, severity, opportunities, and roadmap inputs.
- [customer-support-response](skills/customer-support-response/SKILL.md) - Draft support replies, classify tickets, identify policy answers, and escalate issues through connected support tools.
- [email-inbox-triage](skills/email-inbox-triage/SKILL.md) - Triage inboxes, summarize threads, draft replies, label messages, and track follow-ups using Composio CLI.
- [lead-qualification-enrichment](skills/lead-qualification-enrichment/SKILL.md) - Qualify and enrich leads using ICP criteria, buying signals, company research, and CRM context.
- [meeting-notes-actions](skills/meeting-notes-actions/SKILL.md) - Turn meeting transcripts and rough notes into summaries, decisions, risks, and owner-tagged action items.
- [sales-call-prep](skills/sales-call-prep/SKILL.md) - Prepare sales call briefs with account research, pain hypotheses, discovery questions, objections, and follow-up plan.

### Business Operations

- [hiring-candidate-screening](skills/hiring-candidate-screening/SKILL.md) - Screen candidates against role requirements, summarize resumes, draft interview questions, and prepare scorecards.
- [invoice-expense-processing](skills/invoice-expense-processing/SKILL.md) - Extract, validate, categorize, and summarize invoices, receipts, expenses, and payment follow-ups.
- [knowledge-base-maintenance](skills/knowledge-base-maintenance/SKILL.md) - Maintain Notion, Confluence, help center, or wiki content through audits, updates, consolidation, and app publishing.
- [okr-planning-review](skills/okr-planning-review/SKILL.md) - Create and review OKRs, goals, metrics, initiatives, and operating reviews for teams or products.
- [policy-sop-generator](skills/policy-sop-generator/SKILL.md) - Create policies, SOPs, playbooks, checklists, and operating procedures from rough notes or repeated workflows.
- [powerpoint-generation](skills/powerpoint-generation/SKILL.md) - Generate professional PowerPoint presentations from rough notes, outlines, documents, or ideas.
- [vendor-comparison-analysis](skills/vendor-comparison-analysis/SKILL.md) - Compare vendors, tools, agencies, or software options using requirements, pricing, risks, and recommendation criteria.

### Development & Code Tools

- [frontend-design-systems](skills/frontend-design-systems/SKILL.md) - Build production-quality React, Tailwind CSS, and shadcn/ui interfaces with strong spacing, alignment, readability, and non-generic visual design.
- [playwright-mcp-workflows](skills/playwright-mcp-workflows/SKILL.md) - Automate browsers, test applications, validate UI behavior, and run reliable end-to-end workflows through Playwright MCP.
- [repo-context-packaging](skills/repo-context-packaging/SKILL.md) - Package a codebase into a compact, structured context bundle for another AI agent or long-context review.
- [tdd-workflow](skills/tdd-workflow/SKILL.md) - Drive implementation with the red-green-refactor loop when behavior can be specified as tests.
- [vercel-react-best-practices](skills/vercel-react-best-practices/SKILL.md) - Build production React apps with Vercel-style readability, performance, maintainability, and stable UI behavior.

### Planning & Agent Workflows

- [claude-subconscious-workflows](skills/claude-subconscious-workflows/SKILL.md) - Run background reasoning, reflective analysis, hidden planning layers, and self-improvement passes for complex tasks.
- [context-engineering](skills/context-engineering/SKILL.md) - Structure, compress, and orchestrate context for reliable Claude and AI agent workflows.
- [idea-to-plan](skills/idea-to-plan/SKILL.md) - Turn vague ideas or underspecified requests into written specs and implementation plans before coding.
- [memory-management](skills/memory-management/SKILL.md) - Build lightweight memory systems for continuity across sessions, projects, and long-running work.
- [multi-agent-orchestration](skills/multi-agent-orchestration/SKILL.md) - Split large tasks across parallel sub-agents with clear roles and a merge step.
- [structured-project-execution](skills/structured-project-execution/SKILL.md) - Execute multi-step projects with durable progress, decision, and plan tracking across handoffs.

### Cloud, Apps & Systems

- [azure-messaging-workflows](skills/azure-messaging-workflows/SKILL.md) - Build scalable Azure messaging systems with queues, service buses, pub/sub, and event-driven patterns.
- [azure-observability-workflows](skills/azure-observability-workflows/SKILL.md) - Implement Azure observability with logging, monitoring, tracing, metrics, dashboards, and diagnostics.
- [composio-cli](skills/composio-cli/SKILL.md) - Operate external SaaS apps from the terminal via Composio CLI, including discovery, auth, tool schemas, execution, triggers, and cross-app automation.

### Creative & Media

- [blender-geometry-nodes](skills/blender-geometry-nodes/SKILL.md) - Create procedural Blender systems with Geometry Nodes, procedural materials, and non-destructive generation.
- [blender-hard-surface-modeling](skills/blender-hard-surface-modeling/SKILL.md) - Model precise hard-surface assets in Blender with clean topology, subdivision workflows, and bevel systems.
- [blender-python-integration](skills/blender-python-integration/SKILL.md) - Generate Blender Python scripts for procedural scenes, animations, assets, and workflow automation.
- [blender-rigging-animation](skills/blender-rigging-animation/SKILL.md) - Set up Blender, rig a character, and create a simple rendered animation.
- [remotion-animation-rules](skills/remotion-animation-rules/SKILL.md) - Build technically correct Remotion animations with frame-based rendering, spring physics, and native animation patterns.
- [remotion-creative-storytelling](skills/remotion-creative-storytelling/SKILL.md) - Develop concepts, hooks, story structure, and audience-focused narratives for Remotion videos.
- [remotion-image-video-masking](skills/remotion-image-video-masking/SKILL.md) - Create layered Remotion masking effects with image/video masks, text occlusion, and frame-based animation.
- [remotion-layout-debugging](skills/remotion-layout-debugging/SKILL.md) - Diagnose and fix layout instability, text jumping, resizing issues, and render inconsistency in Remotion.

### Skill Authoring & Maintenance

- [skill-doc-authoring](skills/skill-doc-authoring/SKILL.md) - Write a well-formed `SKILL.md` from a workflow, SOP, or repeated process with reliable trigger metadata.
- [skill-improvement-opportunity-logger](skills/skill-improvement-opportunity-logger/SKILL.md) - Observe work sessions, identify repeated friction, log improvement opportunities, and refine workflows over time.

## Using Skills

OpenCode can load skills from project or global locations.

Project-scoped skills:

```text
.opencode/skills/<skill-name>/SKILL.md
.claude/skills/<skill-name>/SKILL.md
.agents/skills/<skill-name>/SKILL.md
```

Global skills:

```text
~/.config/opencode/skills/<skill-name>/SKILL.md
~/.claude/skills/<skill-name>/SKILL.md
~/.agents/skills/<skill-name>/SKILL.md
```

After installing, restart OpenCode so it reloads skill metadata. To verify a skill, inspect its frontmatter and make sure `name` and `description` are present.

## Creating Skills

Skill layout:

```text
skill-name/
|-- SKILL.md
|-- scripts/
|-- references/
`-- assets/
```

Basic `SKILL.md` template:

```md
---
name: skill-name
description: What this skill does. Use when the user asks for specific trigger cases.
---

# Skill Name

## When to use

## Procedure

## Quality bar

## Anti-patterns
```

Best practices:

- Keep the directory name and `name:` lowercase with hyphen separators.
- Make `description` specific enough for the agent to trigger the skill correctly.
- Keep the main body focused on execution steps and guardrails.
- Put long reference material in `references/` and deterministic helpers in `scripts/`.
- Use [skill-doc-authoring](skills/skill-doc-authoring/SKILL.md) when turning a workflow into a skill.

## Related Awesome Lists

- [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) - Curated Claude Skills, plugins, and resources.
- [ComposioHQ/awesome-codex-skills](https://github.com/ComposioHQ/awesome-codex-skills) - Practical Codex skills for CLI and API workflows.
- [anthropics/skills](https://github.com/anthropics/skills) - Official Anthropic skills and examples.
- [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) - Cross-agent skill collections for Claude Code, Codex, Gemini CLI, Cursor, and more.
- [obra/superpowers](https://github.com/obra/superpowers) - Agent skill methodology and composable software-development workflows.

## Contributing

PRs welcome. Add real, reusable skills with precise metadata, clear execution guidance, and no generic filler. If you add a skill, update the skill count badge and place it in the most specific category above.

## License

MIT

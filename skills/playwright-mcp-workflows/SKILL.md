---
name: playwright-mcp-workflows
description: Workflow for using Playwright with MCP-based agent systems to automate browsers, test applications, perform UI validation, and execute reliable end-to-end workflows through structured browser orchestration.
---

# Playwright MCP Workflows

## Overview

This skill enables Claude to use Playwright within MCP-based workflows to automate browsers, interact with web applications, validate UI behavior, and execute reliable end-to-end automation tasks.

The workflow focuses on:
- browser automation
- MCP tool orchestration
- UI testing
- workflow automation
- DOM interaction
- visual validation
- deterministic browser control
- scalable automation pipelines

The goal is to allow Claude to interact with websites and web applications in a structured, reliable, and repeatable way while maintaining stable automation behavior.

This workflow is especially useful for:
- testing applications
- validating frontend behavior
- automating repetitive workflows
- browser-based agent systems
- AI-powered QA pipelines

---

# Setup

Before starting:

1. Install Node.js:
   https://nodejs.org

2. Create a project:

```bash
npm init -y
```

3. Install Playwright:

```bash
npm install playwright
```

4. Install browser binaries:

```bash
npx playwright install
```

5. Configure MCP integration layer.

Recommended tools:
- Playwright
- MCP-compatible agent systems
- VS Code
- Chromium
- GitHub Actions (optional)

Recommended extensions:
- Playwright VS Code Extension
- Error Lens

Optional:
- Docker
- CI/CD pipelines
- Screenshot diff tools
- Headless browser infrastructure

---

# Inputs Required

- Target website or application
- Automation objective
- Browser workflow requirements
- UI validation goals

Optional:
- Authentication credentials
- Test accounts
- Existing Playwright scripts
- MCP orchestration systems

---

# When to Use This Skill

Use this skill when:
- automating browser workflows
- testing frontend applications
- validating UI behavior
- building AI browser agents
- performing regression testing
- automating repetitive web tasks
- creating deterministic browser pipelines
- orchestrating multi-step browser workflows

---

# When NOT to Use

Do NOT use this skill for:
- backend-only workflows
- non-browser automation
- highly unstable undocumented interfaces
- unsafe credential-sharing systems
- tasks requiring CAPTCHA bypassing or abuse automation

---

# Example Use Case

> Use Claude with Playwright MCP tools to validate a SaaS dashboard workflow.

Claude should:

1. Open the application
2. Authenticate into the dashboard
3. Navigate through UI flows
4. Validate layout and functionality
5. Detect broken interactions
6. Capture screenshots if needed
7. Report workflow issues clearly

Final result should:
- remain deterministic
- reproduce reliably
- validate critical workflows
- improve testing quality
- support scalable browser automation

---

# Core Playwright MCP Principles

## 1. Keep Browser Automation Deterministic

Automation systems should behave consistently across executions.

Claude should:
- avoid unstable selectors
- wait for deterministic states
- validate page readiness
- use structured navigation logic

Good deterministic workflows improve:
- reliability
- debugging
- reproducibility

Avoid:
- timing hacks
- arbitrary delays
- unstable DOM assumptions

---

## 2. Use Stable Selectors

Selectors are critical for reliable automation.

Preferred selectors:
- data attributes
- semantic labels
- accessible roles
- stable IDs

Avoid:
- deeply nested CSS selectors
- dynamically generated classes
- fragile DOM chains

Good selectors improve:
- test stability
- maintainability
- long-term reliability

---

## 3. Validate UI State Explicitly

Claude should actively validate:
- page rendering
- loading completion
- element visibility
- interaction success
- error states

Avoid assuming:
- pages loaded correctly
- requests completed successfully
- animations finished automatically

Explicit validation improves:
- reliability
- debugging quality
- workflow stability

---

## 4. Separate Workflow Logic From Assertions

Good automation systems separate:
- navigation logic
- interaction systems
- validation assertions
- reporting

This improves:
- readability
- debugging
- scalability
- maintenance

Example structure:

```plaintext
workflows/
assertions/
helpers/
screenshots/
```

---

## 5. MCP Systems Should Orchestrate Cleanly

MCP-based workflows should:
- coordinate browser tasks
- manage tool execution
- preserve shared context
- sequence automation reliably

Claude should:
- track workflow state
- maintain execution context
- synchronize automation stages

Good orchestration improves:
- scalability
- agent coordination
- execution clarity

---

# Workflow

## 1. Define the Browser Workflow

Start by identifying:
- target application
- automation objectives
- validation requirements
- interaction flow

Examples:
- login flows
- dashboard testing
- checkout validation
- admin workflows
- onboarding systems

Define:
- success conditions
- failure states
- expected UI behavior

---

## 2. Launch Browser Session

Initialize Playwright.

Example:

```ts
const browser = await chromium.launch();
```

Configure:
- browser type
- headless/headed mode
- viewport size
- session persistence

Ensure:
- sessions remain stable
- environment remains reproducible

---

## 3. Navigate & Interact

Claude should:
- open pages
- click elements
- fill forms
- navigate workflows
- wait for stable states

Use:
- role selectors
- labels
- stable identifiers

Validate:
- interactions succeed
- pages render correctly
- navigation remains stable

---

## 4. Validate UI Behavior

Check:
- visible content
- layout rendering
- loading states
- interaction feedback
- error messages

Claude should detect:
- broken flows
- missing elements
- unstable rendering
- interaction failures

Optional:
- screenshot comparisons
- visual regression checks

---

## 5. Handle Errors Gracefully

Automation systems should:
- detect failures early
- capture useful logs
- preserve screenshots
- report issues clearly

Avoid:
- silent failures
- ambiguous error handling
- incomplete reporting

Good debugging improves:
- reliability
- maintainability
- workflow scalability

---

## 6. Coordinate MCP Tasks

In multi-agent systems:
- browser agents
- review agents
- reporting agents
- orchestration agents

should coordinate through:
- shared context
- structured workflow state
- deterministic execution order

This improves:
- scalability
- automation reliability
- task coordination

---

## 7. Final Validation & Reporting

Before completion validate:
- workflow success
- UI consistency
- interaction stability
- error-free execution

Generate:
- reports
- screenshots
- summaries
- failure logs

Ensure:
- results remain reproducible
- workflows remain maintainable

---

# Output Expectations

The final output should include:
- reliable browser automation
- stable Playwright workflows
- deterministic UI validation
- structured MCP orchestration
- maintainable automation systems
- production-ready testing workflows

The workflow itself should remain:
- scalable
- modular
- reproducible
- easy to debug
- automation-friendly

---

# Execution Strategy (for AI agents)

The agent should:

1. Maintain deterministic browser behavior
2. Use stable selectors consistently
3. Validate UI states explicitly
4. Separate workflow logic from assertions
5. Coordinate MCP systems carefully
6. Generate useful debugging information proactively

The workflow should optimize for:
- reliability
- reproducibility
- automation quality
- UI stability
- debugging clarity

---

# Best Practices

- Prefer stable selectors
- Avoid arbitrary delays
- Validate every critical interaction
- Capture useful debugging information
- Keep automation workflows modular
- Separate assertions from navigation logic
- Preserve reproducible execution environments

---

# Notes

- Stable selectors dramatically improve automation reliability
- Deterministic workflows scale better long-term
- Explicit validation prevents hidden automation failures
- Good browser orchestration improves multi-agent execution quality
- Playwright is most powerful when combined with structured workflow systems

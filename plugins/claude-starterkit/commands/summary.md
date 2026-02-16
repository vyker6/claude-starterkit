---
description: Show a summary of all claude-starterkit skills, commands, and hooks
disable-model-invocation: true
---

Display the following summary to the user exactly as written:

---

# claude-starterkit

**24 skills, 12 commands, 7 automatic hooks** for productive team development.

## Commands

| Command | What it does |
|---------|-------------|
| `/teampush` | Full 7-gate governance pipeline — enforces CLAUDE.md rules, TDD, worktree isolation, design system, security, verification, and regression checks before allowing push |
| `/deploy` | Automated deploy pipeline — runs tests, debugs failures, audits frontend design, creates PR, triggers builds |
| `/handoff` | Documents current work state (progress, decisions, blockers, next steps) for seamless handoff between team members |
| `/conflicts` | Scans all open branches and PRs for file overlaps with your current work — catches merge conflicts before they happen |
| `/decide` | Records an architecture decision (ADR) to `docs/decisions/` and updates CLAUDE.md so future sessions respect it |
| `/pr-prep` | Generates a comprehensive PR description with review walkthrough, risk assessment, and test plan for human reviewers |
| `/onboard` | Analyzes the codebase and generates a personalized project orientation for new team members |
| `/brainstorm` | Explores requirements and design before implementation |
| `/write-plan` | Creates a detailed implementation plan |
| `/execute-plan` | Executes a saved implementation plan with review checkpoints |
| `/revise-claude-md` | Updates CLAUDE.md with learnings from the current session |
| `/summary` | Shows this summary of all skills, commands, and hooks |

## Automatic Hooks (no commands needed)

These run automatically in the background:

| Hook | When it fires | What it does |
|------|--------------|-------------|
| **Branch check** | Session start | Warns if you're on main/master — create a feature branch first |
| **Branch naming** | Session start | Warns if branch doesn't follow convention (feat/, fix/, docs/, etc.) |
| **Stale branch** | Session start | Warns if branch hasn't rebased on main in 3+ days |
| **TDD nudge** | After every file edit | Reminds you to write tests for implementation files |
| **Commit lint** | Before git commit | Blocks non-conventional commits — must use feat:, fix:, docs:, etc. |
| **Large diff** | Before git push | Warns if diff exceeds 500 lines — suggests splitting the PR |
| **Push gate** | Before git push / PR | Blocks push until `/teampush` passes all 7 governance gates |

## Skills (available via Skill tool)

### Team Collaboration
- **context-handoff** — Document work state for team handoff
- **conflict-radar** — Scan open branches for file overlaps
- **architecture-decision-records** — Record and reference team ADRs
- **pr-prep** — Generate review-ready PR descriptions
- **onboarding** — Project orientation for new team members

### Governance & Quality
- **team-governance** — 7-gate enforcement pipeline (CLAUDE.md, worktree, TDD, design, security, review, regression)
- **verification-before-completion** — Verify claims with evidence before marking done
- **requesting-code-review** — Automated code review against standards
- **receiving-code-review** — Handle code review feedback with rigor
- **vibe-security** — OWASP security scanning

### Development Workflow
- **test-driven-development** — Write tests before implementation
- **systematic-debugging** — Diagnose bugs methodically
- **frontend-design** — Production-grade UI/UX interfaces
- **deploy** — Automated test, build, PR, push pipeline
- **finishing-a-development-branch** — Guide branch completion and merge

### Planning & Execution
- **brainstorming** — Explore requirements and design
- **writing-plans** — Create implementation plans
- **executing-plans** — Execute plans with review checkpoints
- **dispatching-parallel-agents** — Handle 2+ independent tasks concurrently
- **subagent-driven-development** — Execute plans with subagents

### Tooling
- **using-git-worktrees** — Isolate feature work in worktrees
- **claude-md-improver** — Audit and improve CLAUDE.md quality
- **using-superpowers** — Skill discovery and bootstrapping
- **writing-skills** — Create and verify new skills

---

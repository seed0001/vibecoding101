# Vibe Coding 101 Agent Directive

## Purpose

This document gives any AI coding application the operating context and rules
for working on Vibe Coding 101. Read this document before planning, editing,
running commands, or publishing changes.

If an instruction here conflicts with a direct instruction from the project
owner, follow the owner's latest instruction. Always follow applicable safety,
security, platform, and permission requirements.

## Mission

Build Vibe Coding 101: a practical book and educational platform that teaches
people to create useful, valuable products efficiently with AI.

The complete ecosystem includes:

1. A practical book about efficient vibe coding.
2. A website with structured education, examples, and progress tracking.
3. A Discord community for students and builders.
4. A marketplace where students can sell what they create.
5. Transparent records showing what the human directed, what an agent
   completed, and when direct human intervention was required.

The project itself is also the primary case study. Its history must honestly
demonstrate how much can be built through voice direction from a relaxed state.

## Working relationship

The project owner normally communicates by voice through a cell phone. Assume
the owner is away from the computer unless explicitly stated otherwise.

The agent should perform as much safe, authorized work as its environment
allows, including:

- Inspecting the repository and understanding existing behavior.
- Researching technical options when current information is required.
- Writing and editing code and documentation.
- Installing necessary project dependencies when authorized.
- Running tests, builds, linters, and smoke checks.
- Diagnosing failures and implementing in-scope fixes.
- Committing and pushing completed work when publication is requested or is
  already part of the established workflow.
- Updating the project build log after meaningful milestones.

Do not hand routine implementation steps back to the owner. Ask the owner to
use the computer only when an action genuinely requires human presence,
credentials, private information, billing approval, an interactive login, or a
decision that would materially change product scope.

## Communication style

- Be direct, conversational, and concise.
- Lead with outcomes, blockers, and decisions.
- Use plain language without hiding important technical facts.
- Do not use artificial praise, cheerleading, or filler.
- State uncertainty honestly and verify assumptions when practical.
- Challenge weak technical assumptions respectfully and explain the reasoning.
- Ask questions only when the answer is necessary to proceed safely or would
  materially change the result.
- During longer tasks, give short progress updates so the owner knows what is
  happening.
- End with what changed, what was verified, what was published, and any action
  that still requires the owner.

## Execution standard

1. Understand the requested outcome and inspect relevant project context.
2. Preserve working behavior and unrelated user changes.
3. Make the smallest coherent change that fully achieves the outcome.
4. Validate the result in proportion to its risk.
5. Fix in-scope failures before reporting completion.
6. Commit intentional files with a clear message.
7. Push when the task or established workflow calls for publication.
8. Confirm the working tree and remote state are synchronized.
9. Update `BUILD_LOG.md` with an accurate account of the milestone.

Do not claim that something works merely because files were created or packages
were installed. Use the strongest practical verification available: automated
tests, a production build, a smoke test, direct output inspection, or remote
state confirmation.

## Autonomy and permission boundaries

Proceed without unnecessary confirmation for actions that are:

- Read-only or diagnostic.
- Reversible and confined to this repository.
- Normal implementation, testing, documentation, or publishing steps already
  authorized by the owner's request.

Stop and request direction before:

- Spending money or changing billing.
- Entering, requesting, or exposing secrets.
- Deleting production data or performing an irreversible destructive action.
- Sending public communications outside the project's normal Git publishing
  workflow.
- Making a major product decision not implied by the owner's direction.

Never work around authentication or security controls. Record the blocker and
the smallest manual action needed from the owner.

## Phone-first rule

Optimize the workflow so the owner can remain on the phone:

- Use existing authenticated tools and repository connections when available.
- Combine related safe operations instead of requesting repeated approvals.
- Make sensible implementation decisions from the documented vision.
- Keep manual instructions short, exact, and deferred until truly necessary.
- After the owner completes a manual step, verify its result and resume the
  automated workflow.

## Build log and measurement

`BUILD_LOG.md` is part of the product, not incidental project notes. Update it
after each meaningful completed milestone and after every manual computer
intervention.

Every entry must include:

- Date and milestone name.
- The owner's direction.
- Work performed by the agent.
- Verified result.
- Classification.
- Any manual computer intervention.
- Relevant commit, deployment, or artifact identifiers when available.

Use one of these classifications:

- **Voice-directed / agent-executed:** The owner directs the work remotely and
  the agent completes the milestone.
- **Manual computer intervention:** The owner directly performs the substantive
  milestone at the computer.
- **Collaborative:** Both the owner and agent perform substantial parts of the
  milestone.

The milestone autonomy rate is:

`voice-directed completed milestones / all completed milestones x 100`

Deferred work does not affect the rate until completed. Never inflate the rate,
hide a manual intervention, or imply that this metric measures time or lines of
code.

## Git and repository discipline

- Inspect status and diffs before staging.
- Never overwrite or silently include unrelated changes.
- Keep generated secrets, credentials, dependencies, and local environment
  files out of Git.
- Use focused commit messages that describe the completed result.
- Do not leave accidental nested repositories, temporary publishing folders, or
  unexplained untracked files.
- After pushing, verify that the local commit matches the remote branch.
- Keep `README.md`, this directive, and `BUILD_LOG.md` consistent with the
  current project.

## Product principles

- Teach through working examples and transparent evidence.
- Prefer a usable end-to-end path over disconnected feature fragments.
- Explain enough that students understand what the AI did and why.
- Treat security, accessibility, privacy, and maintainability as part of
  efficient development, not optional polish.
- Design the marketplace around student ownership, clear attribution, and
  trustworthy transactions.
- Distinguish prototypes from production-ready systems honestly.
- Record failures and course corrections when they provide useful lessons.

## Current manual dependency

Railway CLI is installed, but Railway authentication is deferred until the
owner creates the application and runs `railway login` at the computer. Do not
count this as a manual intervention until it occurs.

## Definition of done

A milestone is done only when:

- The requested behavior or artifact exists.
- Relevant validation has passed or any limitation is explicitly documented.
- Documentation and the build log are current.
- Intended changes are committed and pushed when publication is in scope.
- The working tree contains no unexplained changes.
- The owner receives a concise, factual completion report.

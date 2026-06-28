# SkillRouter Brief

## One-line Summary

A router-first agent system that chooses the right skill, tool, or agent for a task.

## Category

Skill / Tool / Agent Selection Engine

## Priority

Phase 3 / platform

## Product Context

This project belongs to the public Cerebra Forge Labs / ForgeOps Labs product idea set. The public repository should present SkillRouter as an independent product that people can understand and use, while the deeper Cerebra MCP layer can be used internally for orchestration, review, testing, security, DevOps, and context governance.

## Product Concept

Given a user request such as checking a repo and creating a deployment plan, SkillRouter selects repo-analyzer, security-reviewer, test-planner, devops-planner, and documentation-writer.

## Why It Should Exist

It directly demonstrates the core idea of CerebraSkill: route to the correct capability instead of using one generic agent for everything.

The market need is practical: teams want AI-assisted systems that move beyond prompts and demos into repeatable workflows, validated outputs, and handoff-ready artifacts. SkillRouter should make that workflow explicit and useful from the first release.

## Target Users

agent platform teams, AI workflow builders, support automation teams, tool orchestration developers

## Primary Job To Be Done

When a user needs skill / tool / agent selection engine work, they should be able to provide the minimum required context, run the workflow, inspect the result, and leave with a usable output package rather than vague advice.

## Inputs

user task, available skills, tool permissions, tenant policies, risk profile, context budget

## Outputs

routing plan, selected skills, rejected skills, tool permission plan, execution trace, review gates

## Core Capabilities

- intent classification
- skill registry
- routing policy
- permission gates
- context selection
- multi-skill plan
- fallback routing
- audit trace

## Cerebra MCP Fit

Recommended Cerebra MCP capabilities:

CerebraSkill-mcp, CerebraRole-mcp, CerebraOrchestrator-mcp, CerebraSecurity-mcp

Cerebra should be used as the behind-the-scenes quality layer for role selection, context composition, risk checks, review, testing, security, and delivery evidence. The public product should not require users to understand Cerebra internals before they can get value.

## MVP Experience

1. User creates a project or run.
2. User provides required inputs.
3. System validates missing or risky information.
4. System generates or audits the target artifact.
5. User reviews output, warnings, assumptions, and next steps.
6. User exports or saves the result.

## Differentiation

- Product-specific workflow, not a generic chatbot.
- Concrete outputs that can be committed, deployed, tested, or reviewed.
- Quality gates that make generated work safer to trust.
- Clear traceability from inputs to output.
- Practical public repo structure that invites adoption and contribution.

## Success Metrics

- First useful result is produced in under 10 minutes for a new user.
- At least 80 percent of MVP runs produce an exportable artifact.
- Generated outputs require fewer than three major manual corrections in normal use.
- Users can understand setup and usage from the README without private context.
- The project can be demonstrated publicly with safe sample data.

## Non-goals

- Do not expose private Cerebra internals as a requirement for public use.
- Do not automate destructive or external actions without explicit approval.
- Do not build broad marketplace features before the core workflow works.
- Do not ship AI output without assumptions, risks, and validation status.

## Recommended MVP Stack

TypeScript service, rules engine, vector/semantic matching, policy evaluator, trace store

## Key Risks

wrong tool routing, privilege escalation, opaque decisions, missing fallback, over-routing

## Launch Recommendation

Ship the first version as a focused public repo with clear docs, sample input, sample output, and a small runnable path. Treat broader integrations as phase two unless they are essential to proving the product.

# SkillRouter

A router-first agent system that chooses the right skill, tool, or agent for a task.

## Product Position

SkillRouter is a **Skill / Tool / Agent Selection Engine** in the Cerebra Forge Labs / ForgeOps Labs public product set. It is designed as a public, useful tool while Cerebra MCP remains the orchestration and governance factory behind the scenes.

## Why This Project Matters

It directly demonstrates the core idea of CerebraSkill: route to the correct capability instead of using one generic agent for everything.

The goal is not to publish a shallow demo. The repository should become a buildable product foundation with clear requirements, delivery gates, and enough implementation detail for a developer or AI coding agent to start from zero and ship a usable MVP.

## Target Users

agent platform teams, AI workflow builders, support automation teams, tool orchestration developers

## Core Workflow

1. Capture the user's intent and required inputs.
2. Validate the inputs against the product-specific quality bar.
3. Generate or inspect the target artifact.
4. Show findings, assumptions, risks, and next actions.
5. Export or hand off the result in a format that is useful outside the app.

## Documentation

- [Project brief](docs/brief.md)
- [Requirements](docs/requirements.md)
- [Architecture](docs/architecture.md)
- [Roadmap](docs/roadmap.md)
- [Delivery checklist](docs/delivery-checklist.md)

## Recommended First Build

Build one complete happy path first, then add integrations and automation. The MVP should prove that SkillRouter can deliver its core output reliably before broadening scope.

## License

MIT

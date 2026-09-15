# Portfolio Case Study

## AI-Powered Social Video Production Workflow

### Business problem

Producing short-form AI video across multiple services creates significant coordination overhead. Script approval, audio generation, avatar footage, AI B-roll, references, revisions and final composition can easily become a fragile manual process.

### Objective

Create a controlled orchestration layer that reduces manual coordination while keeping humans in control of editorial quality, generation costs and final visual approval.

### Solution

I designed an n8n-based multi-stage workflow that coordinates:

- content intake
- AI-assisted script development
- revision and approval
- audio production
- independent audio approval
- avatar / B-roll production planning
- AI-video provider calls
- reference management
- scene review
- final composition

The workflow uses persistent states and explicit stop conditions so that missing or invalid assets cannot silently propagate downstream.

### Key design decisions

- **Human-in-the-loop:** approval gates are placed before important or credit-consuming steps.
- **Modular stages:** editorial, audio and video modules are separated rather than implemented as one monolithic workflow.
- **Stateful execution:** each production job retains status and relevant metadata as it moves through the system.
- **Fail safely:** required assets must pass validation; invalid inputs stop production.
- **Provider flexibility:** workflow logic is separated from individual AI providers where practical.

### Outcome

The project converted a fragmented set of AI-media tasks into a structured production process with clearer control over status, approvals, errors and generation costs.

### Skills demonstrated

n8n · Workflow Automation · API Integration · Webhooks · AI Integration · Human-in-the-Loop Automation · Process Design · Workflow Troubleshooting · Structured State Management

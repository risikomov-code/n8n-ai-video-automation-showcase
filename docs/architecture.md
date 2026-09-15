# Architecture Notes

This document gives enough technical context to evaluate the project without exposing the production implementation.

## Production stages

### 1. Editorial intake and review
A structured business brief is converted into an AI-assisted draft. The system supports revision and requires explicit human approval before downstream media production.

### 2. Audio production
Approved text moves to an audio stage. Generated audio is reviewed independently before it can be used in video production.

### 3. Avatar / visual planning
The system can route a job toward presenter/avatar footage, AI-generated B-roll, or a mixed composition depending on the production plan.

### 4. Visual generation and final composition
Scenes are generated and reviewed before final composition. Invalid or missing inputs trigger stop conditions instead of silent substitutions.

## Technical patterns demonstrated

- Webhook-driven user actions
- API orchestration
- Persistent workflow state
- Idempotent job identifiers
- Human-in-the-loop decision states
- Explicit lifecycle statuses
- Validation before credit-consuming operations
- Modular production stages
- Provider abstraction
- Failure-first design

## Deliberately omitted

The following are part of the private production implementation and are not included in this showcase:

- exact node graphs
- request payload schemas
- prompts
- provider parameters
- internal identifiers
- webhook paths
- file-system layout
- authentication setup
- retry policies
- cost calculations
- production-state schema

These details are shared only within an appropriate client engagement when required.

---
name: demo.planning
description: Creating and updating software development implementation plans in markdown files (project)
---

# Development Planning Skill

Development planning is about creating structured implementation plans for software development work in markdown files. This skill is specifically for planning coding tasks - features, systems, refactoring, integrations, and other technical implementation work. It focuses on plan creation and maintenance, NOT execution.

## When to Use

Use this skill when:
- Creating new software implementation plans (features, systems, refactoring, integrations)
- Updating existing project plans based on new requirements
- Restructuring plans that have grown too large
- Adding verification and validation criteria to implementation plans

## What This Skill Is For

This skill is designed for **software development planning**, including:
- Feature implementation plans
- System architecture plans
- Code refactoring plans
- Integration plans
- Technical migration plans
- Development roadmap planning

## What This Skill Is NOT For

This skill is NOT for:
- Task planning or daily work organization
- Meeting planning or agendas
- Business strategy planning
- Marketing or sales planning
- Personal productivity planning
- Any non-technical, non-implementation planning

## Important Constraints

**Planning vs Execution**: This skill is ONLY for creating and updating development plans. Never execute or implement plans while using this skill.

**CRITICAL - ABSOLUTE PROHIBITIONS**:
- NEVER create folders, files, or execute any commands while using this skill
- NEVER write or modify implementation code
- NEVER ask for permission to implement
- NEVER ask "Would you like me to proceed with implementation?" or similar questions
- NEVER suggest proceeding to implementation
- When plan is complete, simply END - wait for user's next instruction
- ONLY update and refine the plan document itself

**Execution happens separately**:
- Implementation will be done via a different skill or explicit user request
- The user will explicitly request implementation when ready
- This skill ENDS when the plan is complete - just stop and wait

**Development planning is iterative**:
- Plans can and should evolve during the planning phase
- Focus may shift based on deeper understanding (e.g., from "action plan" to "analysis plan")
- User feedback should refine the plan, not trigger execution

## Plan Structure

### Location
All plans must be written to the `plans/` folder in the current project root.

### Naming Convention
- Main plan: `plans/PLAN_NAME.md`
- Stages: `plans/PLAN_NAME_1.md`, `plans/PLAN_NAME_2.md`, etc.
- Sub-stages: `plans/PLAN_NAME_1_1.md`, `plans/PLAN_NAME_1_2.md`, etc.

Choose PLAN_NAME according to the plan subject (e.g., `authentication-system.md`, `dashboard-redesign.md`).

### Plan Size Guidelines

**Main plan (`PLAN_NAME.md`)**:
- Should remain under 1,000 lines
- Contains overview, objectives, and links to stages

**When plan exceeds 1,000 lines**:
- Split into stages (PLAN_NAME_1.md, PLAN_NAME_2.md, etc.)
- Main PLAN_NAME.md references all stages
- Each stage focuses on a logical phase of work

**When stage exceeds 1,000 lines**:
- Further split into sub-stages (PLAN_NAME_1_1.md, PLAN_NAME_1_2.md, etc.)
- Parent stage references all sub-stages

### Assets and Resources

For code samples, data files, or binary assets:
1. Create folder: `plans/PLAN_NAME/`
2. Place assets as individual files in that folder
3. Reference from markdown plan files using relative paths

## Required Plan Sections

Each plan stage MUST include:

### 1. Overview
- Purpose and objectives
- Context and background
- Success criteria

### 2. Tasks/Steps
- Detailed breakdown of work
- Dependencies between tasks
- Implementation approach

### 3. Verification & Validation (V&V) - CRITICAL

Every stage MUST have a V&V section that clearly defines:

**Verification** (Are we building the product right?)
- How to verify each implementation step
- Code review checkpoints
- Unit test requirements
- Integration test scenarios

**Validation** (Are we building the right product?)
- Acceptance criteria
- User testing scenarios
- Performance benchmarks
- UI/UX validation points

**Why V&V is critical**:
- Required for automated plan execution
- Enables validation of plan completion
- Provides measurable success criteria
- Supports future automation

## Plan Lifecycle

1. **Creation**: Development plans are created in `plans/` folder
2. **Refinement**: Plans evolve based on user feedback during planning phase
3. **Execution**: Plans are executed separately (NOT via this skill)
4. **Documentation**: After execution, implementation docs go to `docs/` folder
5. **Reference**: Implementation docs reference the original plan

### Development Plan Evolution Patterns

During development planning phase, plans may evolve in structure:

**Focus shifts**:
- Example: "Sales Recovery Plan" → "Insights Plan" (action-focused → analysis-focused)
- Rename plan file if purpose changes significantly
- Update overview to reflect new focus

**Approach refinement**:
- Example: Adding "iterative refinement" methodology after user feedback
- Example: Changing from "build all dashboards" to "one dashboard at a time"
- Update execution workflow sections based on new requirements

## Plan Template

```markdown
# [Plan Title]

## Overview
[Purpose, objectives, context]

## Stage 1: [Stage Name]

### Objectives
[What this stage achieves]

### Tasks
1. [Task 1]
2. [Task 2]
   - Subtask 2.1
   - Subtask 2.2

### Verification & Validation

#### Verification
- [ ] Code review: [what to review]
- [ ] Unit tests: [test requirements]
- [ ] Integration: [test scenarios]

#### Validation
- [ ] Acceptance: [acceptance criteria]
- [ ] Performance: [benchmarks]
- [ ] User testing: [scenarios]

## Related Stages
- [Stage 2](PLAN_NAME_2.md)
```

## Examples

### Small Plan (< 1000 lines)
`plans/user-authentication.md` - Single file with all sections

### Large Plan (> 1000 lines)
```
plans/dashboard-redesign.md           # Overview with links
plans/dashboard-redesign_1.md         # Stage 1: Backend API
plans/dashboard-redesign_2.md         # Stage 2: Frontend components
plans/dashboard-redesign_2_1.md       # Stage 2.1: Chart components
plans/dashboard-redesign_2_2.md       # Stage 2.2: Layout system
```

### Plan with Assets
```
plans/api-integration.md              # References assets
plans/api-integration/                # Asset folder
  - schema.json                       # Sample data schema
  - mock-response.json                # Example API response
```

# Important!
- Whenever you split large plans into smaller stages, always start with writing stage files, only then rewrite initial large file!
- Whenever I ask you to make the plan more detailed, you must always split the plan into smaller files, one for each stage

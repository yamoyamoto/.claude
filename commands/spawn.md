**Purpose**: Parallel task execution with TODO-driven implementation

---

@include shared/universal-constants.yml#Universal_Legend

## Command Execution
Execute: immediate. --plan→show plan first
Legend: Generated based on symbols used in command
Purpose: "Execute tasks from TODO list with parallel sub-agents"

Spawn multiple sub-agents to execute tasks in parallel. Accepts TODO list as input, reads linked overall plan and detailed design documents to understand full context, then implements tasks efficiently with maximum parallelization.

**CRITICAL: Test Writing Rule**
- **NEVER write tests in projects without existing test infrastructure**
- **NO Test-Driven Development (TDD) in projects without tests**
- Automatically detect test infrastructure before ANY implementation
- Skip all test-related tasks if no tests exist in the project

**Agent Utilization**: This command MUST use agents defined in `.claude/agents/` directory:
- `senior-developer-xp` for implementation (respects no-test rule)
- `code-review-expert` for code quality validation
- `refactoring-engineer` for code improvements
- `software-architect` for architectural decisions during implementation
- Additional specialized agents as needed

@include shared/flag-inheritance.yml#Universal_Always

Examples:
- `/spawn "path/to/todo-list.md"` - Execute TODO list with parallel agents
- `/spawn --mode sequential "path/to/todo-list.md"` - Sequential execution when dependencies require
- `/spawn --ultrathink "complex-system-todo.md"` - Deep analysis before parallel execution

## Core Features

**TODO-Driven Execution:**
- Accept TODO list document as primary input
- Automatically read linked overall plan & detailed design docs
- Understand full project context before execution
- Track task dependencies and optimize execution order
- **Automatic test task filtering based on project test infrastructure**

**Parallel Sub-Agent Architecture:**
- Spawn multiple agents for independent tasks
- Maximum parallelization for efficiency
- Intelligent task distribution
- Result integration and coordination
- **Single message with multiple Task tool calls for true parallelism**

**Agent-Based Implementation Workflow:**
- **Developer + Reviewer pairs** for each task group
- **Architect consultation** for design decisions
- **Refactoring engineer** for code quality
- **Continuous validation** during implementation

## Execution Modes

**Parallel (Default):** Independent tasks → Maximum concurrency
**Sequential:** Dependency chain → Ordered execution
**Hybrid:** Smart batching → Parallel groups with dependencies

## Process Flow

**Phase 1: Context Understanding (PARALLEL EXECUTION)**
Execute simultaneously:
- **Read TODO list** → Parse tasks & dependencies
- **Read linked docs** → Overall plan & detailed design
- **Test infrastructure detection** → Check for existing tests
- **Codebase analysis** → Current state assessment

**Phase 2: Task Analysis & Planning**
- **Analyze dependencies** → Build execution graph
- **Group independent tasks** → Identify parallel batches
- **Filter test tasks** → Remove if no test infrastructure exists

**Phase 3: Parallel Implementation (MAXIMUM PARALLELIZATION)**
Execute multiple agent groups simultaneously:
- **Independent Task Groups**: Each with dedicated agents
  - `senior-developer-xp` for implementation
  - `code-review-expert` for immediate validation
- **Architecture Decisions**: `software-architect` when needed
- **Code Improvements**: `refactoring-engineer` for optimization

**Phase 4: Integration & Review (PARALLEL EXECUTION)**
Execute simultaneously:
- **Code Integration** → Merge parallel outputs
- **Final Review** → Multiple reviewers in parallel
- **Performance Validation** → Check implementation quality

**Phase 5: Results Consolidation**
- **Unified output** → Integrated implementation
- **Status tracking** → Update TODO completion

## Best Practices

- Ensure TODO lists include clear dependencies
- Link all related documents in TODO header
- Use parallel mode for maximum efficiency
- Monitor sub-agent progress via unified dashboard
- **Test tasks will be automatically skipped if no test infrastructure exists**
- **Always execute independent tasks in parallel batches**
- **Use developer-reviewer pairs for quality assurance**

## Examples

```bash
# Execute TODO list with auto-parallelization
/spawn "feature-x-todo-list.md"

# Force sequential for complex dependencies
/spawn --mode sequential "migration-todo-list.md"

# Deep analysis before execution
/spawn --ultrathink "system-redesign-todo.md"
```

## Agent Integration Strategy

**Parallel Execution Principles:**
- **ALWAYS execute independent agents in parallel**
- Use single message with multiple Task tool invocations
- Group tasks by dependencies for batch execution

**Core Implementation Agents (from `.claude/agents/`):**
- **senior-developer-xp**: Primary implementation (NO TDD if no tests)
- **code-review-expert**: Continuous quality validation
- **refactoring-engineer**: Code optimization and improvements
- **software-architect**: Design decisions and architecture guidance

**Execution Patterns:**
1. **Task Groups**: Developer + Reviewer work in parallel per group
2. **Cross-validation**: Multiple reviewers validate in parallel
3. **Architecture Consultation**: On-demand for design decisions

## Deliverables

- Parallel execution logs with agent activities
- Task completion status with validation results
- Integrated implementation (test-aware)
- Performance metrics and parallelization efficiency

@include shared/universal-constants.yml#Standard_Messages_Templates
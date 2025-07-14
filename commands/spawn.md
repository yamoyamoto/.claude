**Purpose**: Parallel task execution with TODO-driven implementation

---

@include shared/universal-constants.yml#Universal_Legend

## Command Execution
Execute: immediate. --plan→show plan first
Legend: Generated based on symbols used in command
Purpose: "Execute tasks from TODO list with parallel sub-agents"

Spawn multiple sub-agents to execute tasks in parallel. Accepts TODO list as input, reads linked overall plan and detailed design documents to understand full context, then implements tasks efficiently with maximum parallelization.

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

**Parallel Sub-Agent Architecture:**
- Spawn multiple agents for independent tasks
- Maximum parallelization for efficiency
- Intelligent task distribution
- Result integration and coordination

## Execution Modes

**Parallel (Default):** Independent tasks → Maximum concurrency
**Sequential:** Dependency chain → Ordered execution
**Hybrid:** Smart batching → Parallel groups with dependencies

## Process Flow

1. **Read TODO list** → Parse tasks & dependencies
2. **Read linked docs** → Overall plan & detailed design
3. **Analyze dependencies** → Build execution graph
4. **Spawn sub-agents** → Parallel execution
5. **Integrate results** → Unified output

## Best Practices

- Ensure TODO lists include clear dependencies
- Link all related documents in TODO header
- Use parallel mode for maximum efficiency
- Monitor sub-agent progress via unified dashboard

## Examples

```bash
# Execute TODO list with auto-parallelization
/spawn "feature-x-todo-list.md"

# Force sequential for complex dependencies
/spawn --mode sequential "migration-todo-list.md"

# Deep analysis before execution
/spawn --ultrathink "system-redesign-todo.md"
```

## Deliverables

- Parallel execution logs
- Task completion status
- Integrated implementation
- Performance metrics

@include shared/universal-constants.yml#Standard_Messages_Templates
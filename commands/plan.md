**Purpose**: Implementation planning and roadmap development (planning only, no implementation)

**CRITICAL: This command is for PLANNING ONLY. NEVER perform any implementation, code writing, or file creation beyond the planning documents. (計画のみ・実装は絶対に行わない)**

---

@include shared/universal-constants.yml#Universal_Legend

## Command Execution

Execute: immediate. --plan→show plan first
Legend: Generated based on symbols used in command
Purpose: "Create comprehensive plans & roadmaps for $ARGUMENTS" (PLANNING ONLY - NO IMPLEMENTATION)

Develop strategic plans, roadmaps, and documentation frameworks for projects, features, or initiatives specified in $ARGUMENTS. Creates implementation plans only - does not perform actual implementation. Performs thorough existing codebase research and analysis before planning. Actively utilizes web search and multiple subagents for comprehensive research and evaluation to ensure thorough planning coverage.

**Agent Utilization**: This command MUST use agents defined in `.claude/agents/` directory:
- `product-manager-pdm` for requirements and user value analysis
- `software-architect` for system design and architecture
- `senior-developer-xp` for implementation details (respects no-test rule)
- `code-review-expert` for plan validation

**CRITICAL: Parallel Execution Required**
- Execute multiple agents simultaneously wherever possible
- Use single message with multiple Task tool calls for parallel execution
- Only use sequential execution when dependencies require it
- Phases 1, 3, and 5 MUST run agents in parallel for efficiency

**IMPORTANT: All planning documents MUST be written in Japanese (日本語で記述すること)**

**NEVER IMPLEMENT: This command must ONLY create planning documents. Do NOT write any implementation code, create any feature files, or perform any actual development work. (実装は絶対に行わない・計画書の作成のみ)**

@include shared/flag-inheritance.yml#Universal_Always

Examples:

- `/plan "new feature implementation"` - Feature planning with design docs
- `/plan "mobile app launch"` - Project roadmap development
- `/plan --think-hard "system migration"` - Complex planning with deep analysis

## Planning Categories

**Strategic Planning:** Objective setting | Long-term roadmap

**Feature Planning:** Requirements analysis | Technical design | Implementation roadmap

**System Planning:** Architecture design | Migration strategy

## Planning Process

**CRITICAL: Test Writing Rule**
- **NEVER write tests in projects without existing test infrastructure**
- **NO Test-Driven Development (TDD) in projects without tests**
- Check for existing test files/frameworks before planning any test-related tasks
- If no tests exist in the project, exclude all test-related tasks from the plan

**Agent-Based Workflow for All Implementation Tasks:**

**Phase 1: Initial Discovery (PARALLEL EXECUTION)**
Execute these agents simultaneously for maximum efficiency:
- **Product Manager (PdM)**: Define user needs, business requirements, and success criteria
- **Software Architect**: Analyze technical feasibility and existing architecture
- **Code Review Expert**: Audit current codebase for patterns and potential issues
- **Additional Research Agents**: Technology evaluation, competitive analysis, best practices

**Phase 2: Requirements Synthesis**
- **PdM + Architect Collaboration**: Merge business and technical perspectives
- Finalize requirements based on all parallel inputs
- Test infrastructure detection (determines if tests will be included)

**Phase 3: Design Development (PARALLEL EXECUTION)**
Execute these agents simultaneously:
- **Software Architect**: High-level system design
  - System boundaries and component architecture
  - Integration points and data flow
  - Technology stack decisions
- **Senior Developer**: Implementation approach research
  - Code patterns and conventions analysis
  - Framework and library evaluation
  - Development effort estimation

**Phase 4: Detailed Planning (SEQUENTIAL)**
- **Senior Developer**: Create detailed specifications based on architect's design
  - Implementation approach
  - API contracts
  - Error handling strategies
  - **Test strategy ONLY if existing tests are detected**

**Phase 5: Final Review (PARALLEL EXECUTION)**
Execute these agents simultaneously for comprehensive validation:
- **Code Review Expert**: Technical review
  - Architecture alignment
  - Security considerations
  - Best practices compliance
- **Product Manager**: Business alignment review
  - Requirements coverage
  - Success criteria validation
- **Software Architect**: Design coherence review
  - System integration validation
  - Scalability verification

**Phase 6: Documentation Integration**
- Merge all parallel outputs into cohesive documentation
- Overall plan (basic design/requirements)
- Detailed design specifications
- Essential TODO list with task dependencies clearly mapped

## Auto-Generated Documentation

The `/plan` command automatically generates three complementary documents in the same directory as the prompt file (unless otherwise specified).

**IMPORTANT: Each document MUST include cross-reference paths to other related documents (各ドキュメントには他の関連ドキュメントへのパスを記載すること)**

**1. Overall Plan Document** (`[subject]-overall-plan.md`)

- Executive summary and strategic overview
- Objectives definition
- High-level approach and methodology
- Implementation strategy
- **Cross-references section with paths to detailed design and TODO list documents**

**2. Detailed Design Document** (`[subject]-detailed-design.md`)

- Technical specifications and architecture details
- Implementation approach and considerations
- Integration points and system design
- **Test Strategy Section**: ONLY included if existing tests are detected in the project
- **Cross-references section with paths to overall plan and TODO list documents**

**3. TODO List Document** (`[subject]-todo-list.md`)

- Essential tasks only (no optional items)
- Prioritized actionable tasks with clear ownership
- **Task dependencies MUST be explicitly specified for each task (各タスクの依存関係を必ず明記)**
- Task dependencies and sequencing requirements clearly mapped
- Format: Each task must include `Dependencies: [Task IDs or "None"]`

## Subagent Integration

**Parallel Execution Strategy:**
- **ALWAYS execute independent agents in parallel** to maximize efficiency
- Use single message with multiple Task tool invocations for parallel execution
- Only enforce sequential execution where dependencies exist

**Core Agents (from `.claude/agents/`):**
- **product-manager-pdm**: Requirements, user value, success criteria
- **software-architect**: System design, technology decisions, architecture
- **senior-developer-xp**: Implementation details, code patterns (NO TDD if no tests exist)
- **code-review-expert**: Validation, security, best practices
- **refactoring-engineer**: Code improvement strategies (when applicable)

**Parallel Execution Groups:**
1. **Discovery Phase**: PdM + Architect + Reviewer + Research agents (ALL PARALLEL)
2. **Design Phase**: Architect + Developer research (PARALLEL)
3. **Review Phase**: Reviewer + PdM + Architect validation (ALL PARALLEL)

**Additional Research Agents:** Technology evaluation | Best practices | Competitive analysis | Web search

**Efficiency Principle:** Maximize parallel agent execution. Sequential only when outputs depend on previous phase.

@include shared/task-management-patterns.yml#Planning_Integration

## Deliverables

**Three-Document Planning Suite:**

- **Overall Plan**: Strategic framework with objectives (日本語で記述)
- **Detailed Design**: Technical specifications, implementation approach, and integration details (日本語で記述)
- **TODO List**: Essential tasks only with clearly mapped dependencies (no optional items) (日本語で記述・依存関係明記)

**Integrated Planning System:** Cross-referenced documents | Task dependency mapping

@include shared/universal-constants.yml#Standard_Messages_Templates

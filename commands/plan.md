**Purpose**: Implementation planning and roadmap development (planning only, no implementation)

**CRITICAL: This command is for PLANNING ONLY. NEVER perform any implementation, code writing, or file creation beyond the planning documents. (計画のみ・実装は絶対に行わない)**

---

@include shared/universal-constants.yml#Universal_Legend

## Command Execution

Execute: immediate. --plan→show plan first
Legend: Generated based on symbols used in command
Purpose: "Create comprehensive plans & roadmaps for $ARGUMENTS" (PLANNING ONLY - NO IMPLEMENTATION)

Develop strategic plans, roadmaps, and documentation frameworks for projects, features, or initiatives specified in $ARGUMENTS. Creates implementation plans only - does not perform actual implementation. Performs thorough existing codebase research and analysis before planning. Actively utilizes web search and multiple subagents for comprehensive research and evaluation to ensure thorough planning coverage.

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

**1. Discovery & Research**

- Thorough existing codebase analysis and understanding
- Current state assessment
- Constraint identification
- Competitive landscape (when applicable)

**2. Strategic Design**

- Objective prioritization
- Approach selection and validation

**3. Tactical Planning**

- Task breakdown and sequencing

**4. Documentation Framework**

- Overall plan (basic design/requirements)
- Detailed design specifications
- Essential TODO list with task dependencies clearly mapped (no optional items)

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
- **Cross-references section with paths to overall plan and TODO list documents**

**3. TODO List Document** (`[subject]-todo-list.md`)

- Essential tasks only (no optional items)
- Prioritized actionable tasks with clear ownership
- **Task dependencies MUST be explicitly specified for each task (各タスクの依存関係を必ず明記)**
- Task dependencies and sequencing requirements clearly mapped
- Format: Each task must include `Dependencies: [Task IDs or "None"]`

## Subagent Integration

**Research Tasks:** Technology evaluation | Best practice research | Competitive analysis | Web search for latest information

**Evaluation Tasks:** Option comparison | Impact analysis | Feasibility studies

**Auto-Utilization:** Multiple subagents are actively used for comprehensive research and evaluation to ensure thorough planning coverage across all planning scenarios.

@include shared/task-management-patterns.yml#Planning_Integration

## Deliverables

**Three-Document Planning Suite:**

- **Overall Plan**: Strategic framework with objectives (日本語で記述)
- **Detailed Design**: Technical specifications, implementation approach, and integration details (日本語で記述)
- **TODO List**: Essential tasks only with clearly mapped dependencies (no optional items) (日本語で記述・依存関係明記)

**Integrated Planning System:** Cross-referenced documents | Task dependency mapping

@include shared/universal-constants.yml#Standard_Messages_Templates

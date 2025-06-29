**Purpose**: Strategic planning and roadmap development

---

@include shared/universal-constants.yml#Universal_Legend

## Command Execution
Execute: immediate. --plan→show plan first
Legend: Generated based on symbols used in command
Purpose: "Create comprehensive plans & roadmaps for $ARGUMENTS"

Develop strategic plans, roadmaps, and documentation frameworks for projects, features, or initiatives specified in $ARGUMENTS. Performs thorough existing codebase research and analysis before planning. Actively utilizes web search and multiple subagents for comprehensive research and evaluation to ensure thorough planning coverage.

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

The `/plan` command automatically generates three complementary documents in the same directory as the prompt file (unless otherwise specified):

**1. Overall Plan Document** (`[subject]-overall-plan.md`)
- Executive summary and strategic overview
- Objectives definition
- High-level approach and methodology
- Implementation strategy

**2. Detailed Design Document** (`[subject]-detailed-design.md`)
- Technical specifications and architecture details
- Implementation approach and considerations
- Integration points and system design

**3. TODO List Document** (`[subject]-todo-list.md`)
- Essential tasks only (no optional items)
- Prioritized actionable tasks with clear ownership
- Task dependencies and sequencing requirements clearly mapped

## Subagent Integration

**Research Tasks:** Technology evaluation | Best practice research | Competitive analysis | Web search for latest information

**Evaluation Tasks:** Option comparison | Impact analysis | Feasibility studies

**Design Tasks:** Architecture planning | UI/UX design | Process design | Integration planning

**Auto-Utilization:** Multiple subagents are actively used for comprehensive research and evaluation to ensure thorough planning coverage across all planning scenarios.

@include shared/task-management-patterns.yml#Planning_Integration

## Deliverables

**Three-Document Planning Suite:**
- **Overall Plan**: Strategic framework with objectives
- **Detailed Design**: Technical specifications, implementation approach, and integration details  
- **TODO List**: Essential tasks only with clearly mapped dependencies (no optional items)

**Integrated Planning System:** Cross-referenced documents | Task dependency mapping

@include shared/universal-constants.yml#Standard_Messages_Templates
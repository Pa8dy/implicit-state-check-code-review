# implicit-state-check-code-review
Implicit State Machine Architecture Review  An AI-powered architecture review prompt designed to identify hidden complexity before it becomes technical debt.

An AI-powered architecture review prompt / skill designed to identify hidden complexity before it becomes technical debt.

Rather than focusing on code style, file organisation, or superficial refactors, this review analyses a codebase through the lens of:

Implicit state machines
Business policy distribution
Validation boundaries
Authorisation rules
Query composition
Data-flow complexity
UX, DX, and AX optimisation
What it looks for

Most applications contain hidden state machines that emerge naturally as features are added.

Examples include:

Lifecycle workflows
Approval processes
User onboarding flows
Visibility and permission rules
Import/export pipelines
Multi-step forms
Background processing

These state machines often exist as scattered conditionals, flags, status checks, and duplicated business rules rather than explicit models.

This review identifies those hidden systems and highlights opportunities to make them simpler, more visible, and easier to reason about.

Core Principles

The review uses a small set of architectural heuristics:

Fewer, deeper modules
Smaller interfaces
Validate data once at system boundaries
Use trusted types internally
Consolidate duplicated policy
Keep business rules in one obvious location
Eliminate parallel representations of the same concept
Make state transitions explicit
Reduce invalid and impossible states
Optimises For
UX (User Experience)
Consistent behaviour across screens
Predictable workflows
Reduced state-related bugs
Clearer user journeys
DX (Developer Experience)
Easier maintenance
Reduced cognitive load
Fewer sources of truth
Simpler onboarding
AX (Agent Experience)
Easier for AI coding agents to understand
Fewer files required to trace behaviour
More discoverable business rules
Safer automated refactoring
Deliverables

The review produces:

Explicit identification of hidden state machines
Ranked high-leverage architectural recommendations
Risk assessments for each recommendation
UX/DX/AX impact analysis
Concrete refactoring directions
Suggested implementation order
Areas where future technical debt is likely to emerge
Philosophy

This is not a "rewrite my app" prompt.

The goal is to:

Make hidden decisions visible.

A maintainable codebase is not one with the fewest files or smallest line count.

A maintainable codebase is one where the answer to a business question has a single obvious home.

If you have to inspect multiple modules to answer:

Can this entity be edited?
Can this record be viewed?
Can this workflow transition state?

Then the complexity already exists.

This review helps you find it early, while it's still cheap to fix.

Best used during active development to identify architectural seams before they become expensive refactoring projects.

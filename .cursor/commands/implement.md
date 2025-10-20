# Incremental Implementation

Implement features incrementally using a bottom-up, test-driven approach.

## Process:

1. **Receive Implementation Plan**: User provides or you help create a clear implementation plan with discrete components
2. **Bottom-Up Order**: Work on components without dependencies first (e.g., migrations before models, models before services)
3. **Incremental Delivery**: Implement ONE logical component at a time:
   - Present the component implementation
   - Wait for user review
   - Run tests for that component
   - Fix any issues
   - Get approval before moving to next component
4. **Commit Between Components**: After each approved component, ask for confirmation to commit the changes before proceeding
5. **Logical Grouping**: A "component" can include multiple related files if they form a cohesive unit (e.g., model + enum updates, or service + tests)

## Component Definition:

A component is a logical unit that:
- Can be tested independently
- Has clear boundaries
- Doesn't break existing functionality when added
- Is reviewable in isolation

Examples of components:
- ✅ Migration file (single component)
- ✅ Model updates + enum changes (one component if tightly coupled)
- ✅ Service class + its unit tests (one component)
- ✅ Controller action + integration test (one component)
- ❌ Entire feature implementation at once (too large)

## Implementation Workflow:

For each component:
1. **Implement**: Create/update files for the component
2. **Present**: Show what was done and why
3. **Test**: Run relevant tests (unit tests for that component only)
4. **Review**: Wait for user approval
5. **Fix**: Address any feedback or failures
6. **Commit**: After approval, commit with clear message
7. **Next**: Move to next component in the plan

## Example Flow:

```
Plan: Add BuildingReports integration
Components:
1. Migration (sites + device enums)
2. Device model updates
3. BuildingReports::InventoryProcessor + tests
4. Background job (if needed)

Execution:
→ Implement Component 1 (migration)
→ Show migration, explain changes
→ Run migration in test/dev
→ Get approval
→ Commit: "Add building_reports_building_id to sites and new device types"
→ Implement Component 2 (model updates)
→ Show changes, run model tests
→ Get approval
→ Commit: "Update Device model for BuildingReports support"
... and so on
```

## Key Principles:

- **No big-bang implementations**: Break down into reviewable chunks
- **Tests are part of the component**: Don't implement without tests
- **Working tree stays clean**: Commit after each approved component
- **Dependencies first**: Always implement lower-level dependencies before higher-level consumers
- **Explicit approval**: Don't move to next component without user saying to proceed

## What NOT to do:

- ❌ Implement entire feature and present at the end
- ❌ Create multiple components then ask for review
- ❌ Skip tests "for later"
- ❌ Commit multiple components together
- ❌ Guess at unclear requirements instead of asking

This ensures quality, reviewability, and the ability to rollback or adjust at any point in the implementation.


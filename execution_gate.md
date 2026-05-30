# Execution Gate

## Decision Flow
```
User Request → Analyze Scope → Check Necessity → Confirm Safety → Execute Minimal Change
```

## Red Flags
- Multiple file changes for simple fix
- Framework modifications for small bug
- Dependencies updates for typo fix
- Documentation updates for code change

## Green Lights
- Single targeted edit
- Direct response to request
- No side effects
- High reversibility

## Gatekeeper Questions
1. Is this absolutely necessary?
2. Is this directly requested?
3. Could this break existing work?
4. Is there a smaller way to accomplish this?

## Execution Protocol
1. Analyze request thoroughly
2. Check against all restraint rules
3. Generate risk assessment if needed
4. Get user confirmation for high-risk operations
5. Execute minimal change
6. Document execution in audit log
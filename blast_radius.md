# Blast Radius Evaluation

## Impact Assessment
Estimate impact before action:

### Low Risk (Proceed)
- Single style fix
- Typo correction  
- One-line patch

### Medium Risk (Confirm)
- Shared component modification
- API parameter changes
- Configuration updates

### High Risk (Explicit Approval)
- Routing system changes
- Framework structure modifications
- Dependencies updates
- Build configuration changes

## Rule
The larger the blast radius, the higher the confirmation requirement.

## Radius Analysis Questions
- How many files will be affected?
- Will this break existing functionality?
- What systems depend on this change?
- How easy is it to roll back?

## Impact Threshold
- 1-3 files: Low risk
- 4-10 files: Medium risk
- 10+ files: High risk
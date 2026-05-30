# Assumption Control

## Never Assume Hidden Intent
Do not infer:
- Architecture migration
- Framework replacement
- Feature expansion
- Optimization goals

Unless explicitly requested.

## Information Gap Protocol
If information is missing:
- Prefer asking clarification
- Over autonomous interpretation

## Dangerous Assumptions (Forbidden)
- "User probably wants..."
- "This would be better if..."
- "Modern best practice suggests..."

These are not instructions.

## Clarification Checklist
Before proceeding:
- [ ] Request is specific and clear
- [ ] No hidden assumptions detected
- [ ] Scope is well-defined
- [ ] Success criteria is explicit

## Example
User: "Fix video page 404"
- ✅ Check routing configuration
- ✅ Verify file existence
- ❌ Assume user wants to migrate to new framework
- ❌ Assume user wants SEO optimization
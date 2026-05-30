# Context Lock

## Never Expand Scope
- Stay within requested boundaries
- Do not "improve" unrelated code
- Do not add "helpful" features
- Do not optimize beyond request

## Task Boundaries
- Requested file only
- Requested feature only  
- Requested bug only
- No adjacent improvements

## Example
User: "Fix the login button"
- ✅ Fix the button click handler
- ✅ Update button styling if broken
- ❌ Rewrite entire authentication system
- ❌ Add social login options

## Red Flag Detection
- User asks for small fix
- AI wants to rewrite everything
- User mentions one file
- AI wants to modify multiple files
- User wants to fix typo
- AI wants to restructure project
# Confirmation Feedback - Strict Protocol

## Acceptable Confirmation Formats
**ONLY** accept these exact formats:
- `yes`
- `approve` 
- `confirm`

## Rejection Protocol
If user responds with anything other than acceptable formats:
- **Treat as rejection**
- **Do not proceed**
- **Ask for clarification**
- **Log rejection attempt**

## Confirmation Template
```
RISK ASSESSMENT
==============
Files to be Modified:
- [ ] {file_path} - {change_summary}
- [ ] {file_path} - {change_summary}

Risk Level: {level}
Blast Radius: {radius}

Confirmation Required:
Type "yes", "approve", or "confirm" to proceed:
```

## Verification
- Case-insensitive matching
- Trim whitespace
- Exact string matching only
- No partial matches accepted
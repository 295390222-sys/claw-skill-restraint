# Dangerous Operations Protection

## Enhanced Risk Assessment Template
```
IMPACT ASSESSMENT
================
Files to be Modified:
- [ ] File 1: {path} - {change_summary}
- [ ] File 2: {path} - {change_summary}
- [ ] File 3: {path} - {change_summary}

DEPENDENCIES (Auto-Detected):
- [ ] {dependency_name}: {type} - {impact_level}
- [ ] {dependency_name}: {type} - {impact_level}
- [ ] {dependency_name}: {type} - {impact_level}

Risk Level: [Low/Medium/High]
Blast Radius: {number} files
Dependencies Affected: {list}

Potential Impact:
- Positive: {benefits}
- Negative: {risks}
- Reversibility: {easy/medium/hard}

Required Actions:
1. {action_1}
2. {action_2}
3. {action_3}

Confirmation Required:
Do you approve these changes? (yes/approve/confirm)
```

## Dependency Detection
AI must automatically identify:
- Import statements and their sources
- File references and cross-dependencies
- Configuration file dependencies
- Build system dependencies
- Test file dependencies
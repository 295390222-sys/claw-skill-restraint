# Quantified Minimal Action Metrics - Final

## Enhanced Scoring System
```
Score = max(0, 100 - (lines_changed * 0.1) - (files_changed * 5) - (modules_affected * 10))

Score Categories:
- Excellent: 90-100 (Micro change)
- Good: 70-89 (Small change)  
- Acceptable: 50-69 (Medium change)
- Poor: 0-49 (Large change - requires user approval)
```

## Module Impact Assessment
### Module Detection
- Frontend components
- Backend services
- Database schemas
- Configuration files
- Build scripts
- Test files

### Impact Calculation
```
Module Impact = Σ(module_importance * change_severity)
Where:
- module_importance: 1-10 based on criticality
- change_severity: 1-5 based on change depth
```

## Compliance Enforcement
1. **Pre-Action Check**: Calculate predicted score
2. **Threshold Enforcement**: 
   - Score < 50: Require user approval
   - Score < 30: Refuse execution
3. **Post-Action Verification**: Confirm actual score matches prediction